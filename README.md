- 👋 Hi, I’m @kietdeptraivc
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
kietdeptraivc/kietdeptraivc is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cửa Hàng Trực Tuyến</title>
    <style>
        /* Thiết lập các style chung */
        body {
            font-family: Arial, sans-serif;
            background-color: #f7f7f7;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px 0;
            text-align: center;
            font-size: 1.8em;
        }

        .container {
            width: 90%;
            margin: 30px auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 20px;
        }

        /* Các style cho sản phẩm */
        .product {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            width: 30%;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.3s ease;
        }

        .product:hover {
            transform: scale(1.05);
        }

        .product img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .product h3 {
            color: #333;
            font-size: 1.2em;
            margin-bottom: 10px;
        }

        .product p {
            color: #555;
            font-size: 2.0em;
            margin-bottom: 10px;
        }

        .product .price {
            font-size: 1.4em;
            color: #e74c3c;
            margin-bottom: 15px;
        }

        .product button {
            background-color: #27ae60;
            color: white;
            border: none;
            padding: 10px 20%;
            cursor: pointer;
            font-size: 1em;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .product button:hover {
            background-color: #2ecc71;
        }

        /* Giỏ hàng */
        .cart {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            width: 30%;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            margin-top: 30px;
        }

        .cart h2 {
            color: #333;
            font-size: 1.5em;
            margin-bottom: 15px;
        }

        .cart .cart-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            border-bottom: 1px solid #ddd;
            padding-bottom: 10px;
        }

        .cart .cart-item p {
            font-size: 1em;
            color: #555;
        }

        .cart .total {
            font-size: 1.5em;
            color: #e74c3c;
            margin-top: 20px;
            text-align: right;
        }

        .cart button {
            width: 100%;
            background-color: #3498db;
            color: white;
            border: none;
            padding: 15px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .cart button:hover {
            background-color: #2980b9;
        }

        /* Thanh thông báo */
        #notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #27ae60;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            display: none;
            font-size: 1em;
        }
    </style>
</head>
<body>

<header>
    Cửa Hàng Trai Đẹp 
</header>

<div class="container">
    <!-- Sản phẩm 1 -->
    <div class="product" data-id="1">
        <img src="https://kenh14cdn.com/203336854389633024/2023/4/21/photo-3-16820399628461606778534.jpg" alt="Sản phẩm 1">
        <h3>Hiếu Thứ 2</h3>
        <p>Miêu tả về sản phẩm 1. Chất lượng cao và giá cả phải chăng.</p>
        <p class="price">200,000 VNĐ</p>
        <button onclick="addToCart('Sản phẩm 1', 200000, 'https://via.placeholder.com/300')">Thêm vào giỏ hàng</button>
    </div>

    <!-- Sản phẩm 2 -->
    <div class="product" data-id="2">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQighTIuddbTaxwd8TALZPDtc7pYiU5ugZBcQ&s" alt="Sản phẩm 2">
        <h3>Sơn Tùng </h3>
        <p>Miêu tả về sản phẩm 2. Đảm bảo độ bền lâu dài.</p>
        <p class="price">150,000 VNĐ</p>
        <button onclick="addToCart('Sản phẩm 2', 150000, 'https://via.placeholder.com/300')">Thêm vào giỏ hàng</button>
    </div>

    <!-- Sản phẩm 3 -->
    <div class="product" data-id="3">
        <img src="https://scontent.fsgn1-1.fna.fbcdn.net/v/t1.6435-9/73000717_821483854935391_7350769766132350976_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=a5f93a&_nc_eui2=AeGA01hF0KB4JGQPmr0kKAOpZMS9WG5Sw0ZkxL1YblLDRgyZqS9SKIXb1SG23CI63XbsBMRMld7JM3fdGFa5511E&_nc_ohc=F5DMqVvxetcQ7kNvgGMBKNS&_nc_zt=23&_nc_ht=scontent.fsgn1-1.fna&_nc_gid=AcrwkOydib2FRp9OYm23s85&oh=00_AYCUmoTRs3DAe9rpo21soucNUon_IVZ13IoKmV2CCPkbmA&oe=677B6F1B" alt="Sản phẩm 3">
        <h3>anh quỳnh phong đẹp trai vc </h3>
        <p>Miêu tả là anh quỳnh phong rất là đẹp trai ga lăng nhưng mà bị ...... .</p>
        <p class="price">350,000 VNĐ</p>
        <button onclick="addToCart('Sản phẩm 3', 350000, 'https://scontent.fsgn1-1.fna.fbcdn.net/v/t39.30808-1/438242174_1931291410621291_6972906449352919030_n.jpg?stp=dst-jpg_s200x200_tt6&_nc_cat=110&ccb=1-7&_nc_sid=0ecb9b&_nc_eui2=AeGObwpZZAdzu3lO5d8oQKsSpw2E3_AMjKynDYTf8AyMrHyydBufj4DniIqQe62vqJz2Y9mielqg2djZfF9BUdVq&_nc_ohc=odBVqjzMJR8Q7kNvgFM9qIp&_nc_zt=24&_nc_ht=scontent.fsgn1-1.fna&_nc_gid=AVdZoWixO3ssUDhLENpVzHs&oh=00_AYDPhnQwejfmKw9P-9ZRlTAENhraXt9FTxG3MvWDbYlJBw&oe=6759B7FC')">Thêm vào giỏ hàng</button>
    </div>
</div>

<div class="cart">
    <h2>Giỏ hàng của bạn</h2>
    <div id="cart-items">
        <p>Giỏ hàng của bạn chưa có sản phẩm nào.</p>
    </div>
    <div id="cart-total" class="total">
        Tổng cộng: 0 VNĐ
    </div>
    <button onclick="checkout()">Thanh toán</button>
</div>

<div id="notification">Sản phẩm đã được thêm vào giỏ hàng!</div>

<script>
    let cart = [];

    function addToCart(name, price, image) {
        // Thêm sản phẩm vào giỏ hàng
        cart.push({ name, price, image });

        // Hiển thị thông báo
        showNotification("Sản phẩm đã được thêm vào giỏ hàng!");

        // Cập nhật giỏ hàng
        renderCart();
    }

    function renderCart() {
        let cartItemsDiv = document.getElementById('cart-items');
        let cartTotalDiv = document.getElementById('cart-total');

        // Xóa nội dung giỏ hàng cũ
        cartItemsDiv.innerHTML = '';
        let total = 0;

        // Nếu giỏ hàng rỗng
        if (cart.length === 0) {
            cartItemsDiv.innerHTML = '<p>Giỏ hàng của bạn chưa có sản phẩm nào.</p>';
            cartTotalDiv.innerHTML = 'Tổng cộng: 0 VNĐ';
        } else {
            // Hiển thị các sản phẩm trong giỏ hàng
            cart.forEach((item, index) => {
                let itemDiv = document.createElement('div');
                itemDiv.classList.add('cart-item');
                itemDiv.innerHTML = `
                    <img src="${item.image}" alt="${item.name}" style="width: 50px; height: auto; margin-right: 10px;">
                    <p>${item.name}</p>
                    <p>${item.price.toLocaleString()} VNĐ</p>
                    <button onclick="removeFromCart(${index})">Xóa</button>
                `;
                cartItemsDiv.appendChild(itemDiv);
                total += item.price;
            });

            cartTotalDiv.innerHTML = `Tổng cộng: ${total.toLocaleString()} VNĐ`;
        }
    }

    function removeFromCart(index) {
        // Xóa sản phẩm khỏi giỏ hàng
        cart.splice(index, 1);
        renderCart();
    }

    function checkout() {
        if (cart.length === 0) {
            alert("Giỏ hàng của bạn trống. Vui lòng thêm sản phẩm vào giỏ hàng!");
        } else {
            alert("Cảm ơn bạn đã mua sắm! Đơn hàng của bạn đã được xác nhận.");
            cart = []; // Giỏ hàng trở về trạng thái ban đầu
            renderCart(); // Cập nhật giỏ hàng
        }
    }

    function showNotification(message) {
        let notification = document.getElementById('notification');
        notification.textContent = message;
        notification.style.display = 'block';

        setTimeout(() => {
            notification.style.display = 'none';
        }, 3000);
    }
</script>

</body>
</html>
