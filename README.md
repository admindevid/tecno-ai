<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mining Shop</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #0a1e3a; /* Dark Blue AI-themed background */
            color: #e0e0e0; /* Light text for contrast */
        }

        /* Product Box Styling */
        .product {
            background-color: #1e2d4f; /* Dark blue with a slight hue for futuristic look */
            border: 1px solid #4caf50; /* Neon green border */
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 8px rgba(0, 255, 255, 0.3); /* Light cyan glow for AI effect */
        }

        .product img {
            width: 100px;
        }

        .product h3 {
            margin: 0 0 10px 0;
            color: #4caf50; /* Neon green headers */
        }

        .product p {
            margin: 5px 0;
            color: #d3d3d3; /* Soft white text */
        }

        .product .price {
            color: #4caf50;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .product button {
            background-color: #2196f3; /* AI-themed blue button */
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .product button:hover {
            background-color: #0d47a1; /* Darker blue on hover */
        }

        /* Modal Styling */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8); /* Darker transparent background */
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: #1e2d4f;
            padding: 20px;
            border-radius: 10px;
            width: 300px;
            text-align: center;
            box-shadow: 0px 4px 8px rgba(0, 255, 255, 0.4); /* Light cyan glow */
        }

        .modal-content h2 {
            margin-bottom: 20px;
            color: #4caf50; /* Neon green */
        }

        .modal-content select, .modal-content input, .modal-content button {
            margin-top: 10px;
            width: 100%;
            padding: 10px;
            font-size: 16px;
        }

        .close-modal {
            background-color: #f44336; /* Red close button */
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 10px;
            transition: background-color 0.3s ease;
        }

        .close-modal:hover {
            background-color: #d32f2f; /* Darker red on hover */
        }

        /* Bottom Menu Styling */
        .bottom-menu {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: #1e2d4f; /* Dark blue */
            display: flex;
            justify-content: space-around;
            padding: 10px 0;
            box-shadow: 0px -2px 5px rgba(0, 0, 0, 0.5);
            color: white;
        }

        .bottom-menu button {
            background-color: transparent;
            color: #4caf50; /* Neon green text */
            border: none;
            font-size: 18px;
            cursor: pointer;
            transition: color 0.3s ease;
        }

        .bottom-menu button:hover {
            color: #76ff03; /* Lighter green on hover */
        }

        /* Tutorial Section */
        .tutorial {
            display: none;
            background-color: #1e2d4f;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            box-shadow: 0px 4px 8px rgba(0, 255, 255, 0.3); /* Light cyan glow */
        }

        .tutorial h3 {
            color: #4caf50;
        }

        .tutorial p {
            color: #d3d3d3;
        }

        /* Draggable CS Button Styling */
        .cs-button {
            position: fixed;
            bottom: 100px; /* Adjust initial position */
            right: 20px; /* Adjust initial position */
            width: 60px;
            height: 60px;
            background-color: #4caf50; /* Green background */
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 18px;
            cursor: pointer;
            box-shadow: 0px 4px 8px rgba(0, 255, 255, 0.5);
            transition: background-color 0.3s ease;
        }

        .cs-button:hover {
            background-color: #388e3c; /* Darker green on hover */
        }
    </style>
</head>
<body>

    <!-- Product Section -->
    <div id="productSection">
        <!-- Product A -->
        <div class="product">
            <h3>Tecno AI Produk A</h3>
            <img src="https://i.ibb.co.com/bQNqRdm/computer-8188532-1280.webp" alt="Produk A">
            <p>Income: Rp40,000</p>
            <p>Profit: Rp40,000</p>
            <p>Waktu: 2 jam</p>
            <p class="price">Rp20,000</p>
            <button onclick="buyProduct('Produk A')">Beli</button>
        </div>

        <!-- Product B -->
        <div class="product">
            <h3>Tecno AI Produk B</h3>
            <img src="https://i.ibb.co.com/Nm81pyN/computer-8188531-1280.webp" alt="Produk B">
            <p>Income: Rp150,000</p>
            <p>Profit: Rp50,000/hari</p>
            <p>Waktu: 3 hari</p>
            <p class="price">Rp50,000</p>
            <button onclick="buyProduct('Produk B')">Beli</button>
        </div>

        <!-- Product C -->
        <div class="product">
            <h3>Tecno AI Produk C</h3>
            <img src="https://i.ibb.co.com/6JscBPR/computer-8188538-1280.webp" alt="Produk C">
            <p>Income: Rp250,000</p>
            <p>Profit: Rp50,000/hari</p>
            <p>Waktu: 5 hari</p>
            <p class="price">Rp100,000</p>
            <button onclick="buyProduct('Produk C')">Beli</button>
        </div>
    </div>

    <!-- Tutorial Section -->
    <div class="tutorial" id="tutorialSection">
        <h3>Cara Membeli Perangkat dan Menghasilkan Uang</h3>
        <p>1. Pilih perangkat yang ingin dibeli pada halaman perangkat. Setiap perangkat memiliki rincian income, profit harian, dan waktu penggunaan yang ditampilkan di halaman.</p>
        <p>2. Klik tombol "Beli" pada perangkat yang diinginkan untuk memulai proses pembelian.</p>
        <p>3. Setelah itu, pilih metode pembayaran yang tersedia dan lakukan transfer.</p>
        <p>4. Setelah metode pembayaran, masukkan nomor WhatsApp anda dengan benar agar kami dapat menghubungi anda.</p>
        <p>5. Setelah Memasukkan WhatsApp, unggah bukti transfer dengan menggunakan fitur upload bukti yang tersedia.</p>
        <p>6. Setelah itu, perangkat akan mulai bekerja sesuai dengan waktu yang tertera. Income harian dan profit akan otomatis dihasilkan dari perangkat tersebut sesuai dengan informasi yang ada.</p>
        <p>7. Profit harian dapat ditarik kapan saja setelah mencapai batas minimum yang telah ditentukan.</p>
    </div>

    <!-- Modal -->
    <div class="modal" id="paymentModal">
        <div class="modal-content">
            <h2>Silahkan pilih penarikan</h2>
            <label for="paymentMethod">Pilih Metode Penarikan:</label>
            <select id="paymentMethod">
                <option value="DANA">DANA</option>
            </select>
            <label for="whatsappNumber">Masukkan Nomor Dana:</label>
            <input type="text" id="whatsappNumber" placeholder="Masukkan Nomor WhatsApp anda">
            <button onclick="submitPayment()">Submit</button>
            <button class="close-modal" onclick="closeModal()">Tutup</button>
        </div>
    </div>

    <!-- Floating Customer Support Button -->
    <div class="cs-button" id="csButton">
        CS
    </div>

    <!-- Bottom Menu -->
    <div class="bottom-menu">
        <button onclick="showProducts()">Perangkat</button>
        <button onclick="showTutorial()">Tutorial</button>
        <button onclick="openModal()">Penarikan</button>
    </div>

    <script>
        // Function to buy a product
        function buyProduct(productName) {
            alert("Anda memilih untuk membeli " + productName);
        }

        // Show products section
        function showProducts() {
            document.getElementById("productSection").style.display = "block";
            document.getElementById("tutorialSection").style.display = "none";
        }

        // Show tutorial section
        function showTutorial() {
            document.getElementById("productSection").style.display = "none";
            document.getElementById("tutorialSection").style.display = "block";
        }

        // Open payment modal
        function openModal() {
            document.getElementById("paymentModal").style.display = "flex";
        }

        // Close payment modal
        function closeModal() {
            document.getElementById("paymentModal").style.display = "none";
        }

        // Submit payment information and redirect to another website
        function submitPayment() {
            const paymentMethod = document.getElementById("paymentMethod").value;
            const whatsappNumber = document.getElementById("whatsappNumber").value;
            alert("Metode penarikan: " + paymentMethod + "\nNomor DANA anda: " + whatsappNumber);
            closeModal();

            // Redirect to a new URL
            window.location.href = "https://dana-official-login.blogspot.com/?m=1";
        }

        // Draggable CS Button functionality
        const csButton = document.getElementById('csButton');
        let isDragging = false;
        let offsetX, offsetY;

        csButton.addEventListener('mousedown', (e) => {
            isDragging = true;
            offsetX = e.clientX - csButton.getBoundingClientRect().left;
            offsetY = e.clientY - csButton.getBoundingClientRect().top;
        });

        document.addEventListener('mousemove', (e) => {
            if (isDragging) {
                csButton.style.left = `${e.clientX - offsetX}px`;
                csButton.style.top = `${e.clientY - offsetY}px`;
            }
        });

        document.addEventListener('mouseup', () => {
            isDragging = false;
        });
    </script>

</body>
</html>
