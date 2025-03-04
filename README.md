
<?xml version="1.0" encoding="UTF-8" ?>
<b:skin><![CDATA[/* CSS Code */]]></b:skin>
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>होमपेज</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; text-align: center; background: #f4f4f4; }
        .navbar { background-color: #007bff; display: flex; justify-content: space-between; padding: 10px 20px; align-items: center; }
        .nav-links { display: flex; }
        .nav-links a { color: white; text-decoration: none; padding: 14px 20px; font-size: 18px; }
        .nav-links a:hover { background-color: #0056b3; border-radius: 5px; }
        .container { padding: 20px; }
        h1 { color: #007bff; }
        .page-content { display: none; }
        .active { display: block; }
    </style>
</head>
<body>

    <!-- 🔹 Navigation Bar -->
    <div class="navbar">
        <div class="nav-links">
            <a href="#" onclick="showPage('home')">🏠 Home</a>
            <a href="#" onclick="showPage('deposit')">💰 Deposit</a>
            <a href="#" onclick="showPage('withdraw')">🏦 Withdraw</a>
            <a href="#" onclick="showPage('account')">👤 My Account</a>
        </div>
        <a href="#" class="login-btn">🔐 लॉगिन</a>
    </div>

    <!-- 🔹 Pages -->
    <div class="container">
        <!-- 🏡 Home Page (With Game) -->
        <div id="home" class="page-content active">
            <h1>🏡 स्वागत है आपके होमपेज पर!</h1>
            <p>यहाँ से आप अपने पैसे जमा कर सकते हैं, निकाल सकते हैं और अकाउंट की जानकारी देख सकते हैं।</p>

            <!-- 🔹 बॉल ड्रॉप गेम -->
            <iframe src="your_game_page_url_here" width="100%" height="500px" style="border:none;"></iframe>
        </div>

        <!-- 💰 Deposit Page -->
        <div id="deposit" class="page-content">
            <h1>💰 डिपॉज़िट</h1>
            <p>यहाँ से आप पैसे जमा कर सकते हैं।</p>
        </div>

        <!-- 🏦 Withdraw Page -->
        <div id="withdraw" class="page-content">
            <h1>🏦 विदड्रॉ</h1>
            <p>यहाँ से आप अपने पैसे निकाल सकते हैं।</p>
        </div>

        <!-- 👤 My Account Page -->
        <div id="account" class="page-content">
            <h1>👤 माय अकाउंट</h1>
            <p>यहाँ से आप अपने अकाउंट की जानकारी देख सकते हैं।</p>
        </div>
    </div>

    <!-- 🔹 JavaScript for Page Switching -->
    <script>
        function showPage(pageId) {
            var pages = document.getElementsByClassName("page-content");
            for (var i = 0; i < pages.length; i++) {
                pages[i].classList.remove("active");
            }
            document.getElementById(pageId).classList.add("active");
        }
    </script>

</body>
</html>
