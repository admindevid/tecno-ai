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
            <h3>EA Pile Produk A</h3>
            <img src="https://i.ibb.co.com/bQNqRdm/computer-8188532-1280.webp" alt="Produk A">
            <p>Income: Rp40,000</p>
            <p>Profit: Rp20,000/hari</p>
            <p>Waktu: 2 jam</p>
            <p class="price">Rp20,000</p>
            <button onclick="buyProduct('Produk A')">Beli</button>
        </div>

        <!-- Product B -->
        <div class="product">
            <h3>EA Pile Produk B</h3>
            <img src="https://i.ibb.co.com/Nm81pyN/computer-8188531-1280.webp" alt="Produk B">
            <p>Income: Rp150,000</p>
            <p>Profit: Rp50,000/hari</p>
            <p>Waktu: 3 hari</p>
            <p class="price">Rp50,000</p>
            <button onclick="buyProduct('Produk B')">Beli</button>
        </div>

        <!-- Product C -->
        <div class="product">
            <h3>EA Pile Produk C</h3>
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
        <p>4. Setelah pembayaran, unggah bukti transfer dengan menggunakan fitur upload bukti yang tersedia.</p>
        <p>5. Setelah konfirmasi, perangkat akan mulai bekerja sesuai dengan waktu yang tertera. Income harian dan profit akan otomatis dihasilkan dari perangkat tersebut sesuai dengan informasi yang ada.</p>
        <p>6. Profit harian dapat ditarik kapan saja setelah mencapai batas minimum yang telah ditentukan.</p>
    </div>

    <!-- Modal -->
    <div class="modal" id="paymentModal">
        <div class="modal-content">
            <h2>Silahkan Transfer</h2>
            <label for="paymentMethod">Pilih Metode Pembayaran:</label>
            <select id="paymentMethod">
                <option value="DANA">DANA - 083130783481 (RACHMAD FAREL RAMDHAN)</option>
                <option value="GOPAY">GOPAY - 083130783481 (MASAREL STORE)</option>
            </select>
            <label for="whatsappNumber">Masukkan Nomor WhatsApp Anda:</label>
            <input type="text" id="whatsappNumber" placeholder="Contoh: 6281234567890" required>
            <p>Sertakan screenshot bukti transfer!</p>
            <input type="file" id="screenshot" required>
            <button onclick="sendProof()">Kirim Bukti Transfer</button>
            <button class="close-modal" onclick="closeModal()">Batal</button>
        </div>
    </div>

    <!-- Bottom Menu -->
    <div class="bottom-menu">
        <button onclick="showProducts()">PERANGKAT</button>
        <button onclick="showTutorial()">TUTORIAL</button>
    </div>

    <!-- Draggable CS Button -->
    <div class="cs-button" id="csButton" onclick="openWhatsApp()">
        CS
    </div>

    <script>
        let selectedProduct = "";

        function buyProduct(productName) {
            selectedProduct = productName;
            document.getElementById("paymentModal").style.display = "flex";
        }

        function closeModal() {
            document.getElementById("paymentModal").style.display = "none";
        }

        function sendProof() {
            const paymentMethod = document.getElementById("paymentMethod").value;
            const whatsappNumber = document.getElementById("whatsappNumber").value;
            const screenshot = document.getElementById("screenshot").files[0];

            if (!whatsappNumber) {
                alert("Harap masukkan nomor WhatsApp!");
                return;
            }

            if (!screenshot) {
                alert("Harap upload bukti transfer!");
                return;
            }

            const formData = new FormData();
            formData.append('chat_id', '6235911819');
            formData.append('caption', `Pembelian ${selectedProduct}\nNomor WhatsApp: ${whatsappNumber}\nMetode Pembayaran: ${paymentMethod}`);
            formData.append('document', screenshot);

            fetch(`https://api.telegram.org/bot7142158232:AAFrUmsAZEcin86tEQY_3nKTGfp-XT-icXY/sendDocument`, {
                method: 'POST',
                body: formData
            })
            .then(response => response.json())
            .then(data => {
                if (data.ok) {
                    alert("Bukti transfer berhasil dikirim!");
                    closeModal();
                } else {
                    alert("Gagal mengirim bukti transfer. Silakan coba lagi.");
                }
            })
            .catch(error => {
                alert("Terjadi kesalahan: " + error.message);
            });
        }

        function showProducts() {
            document.getElementById("productSection").style.display = "block";
            document.getElementById("tutorialSection").style.display = "none";
        }

        function showTutorial() {
            document.getElementById("productSection").style.display = "none";
            document.getElementById("tutorialSection").style.display = "block";
        }

        // Initial state: Only products are visible, tutorial is hidden
        window.onload = function() {
            document.getElementById("productSection").style.display = "block";
            document.getElementById("tutorialSection").style.display = "none";
        }

        // Draggable CS Button
        const csButton = document.getElementById("csButton");

        csButton.onmousedown = function(event) {
            let shiftX = event.clientX - csButton.getBoundingClientRect().left;
            let shiftY = event.clientY - csButton.getBoundingClientRect().top;

            function moveAt(pageX, pageY) {
                csButton.style.left = pageX - shiftX + 'px';
                csButton.style.top = pageY - shiftY + 'px';
            }

            function onMouseMove(event) {
                moveAt(event.pageX, event.pageY);
            }

            document.addEventListener('mousemove', onMouseMove);

            csButton.onmouseup = function() {
                document.removeEventListener('mousemove', onMouseMove);
                csButton.onmouseup = null;
            };
        };

        csButton.ondragstart = function() {
            return false; // Prevent default drag behavior
        };

        function openWhatsApp() {
            window.open("https://wa.me/6283144282450", "_blank");
        }
    </script>

</body>
</html>
