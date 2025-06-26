<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Secure App Download</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .login-box {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      width: 300px;
      text-align: center;
    }
    input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      width: 100%;
      padding: 10px;
      background-color: #28a745;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .download-box {
      display: none;
      margin-top: 20px;
    }
    .error {
      color: red;
      font-size: 0.9em;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>App Login</h2>
    <input type="text" id="username" placeholder="Enter username">
    <input type="password" id="password" placeholder="Enter password">
    <button onclick="verifyLogin()">Login</button>
    <div class="error" id="error-msg"></div>
    <div class="download-box" id="download-box">
      <p>Login successful! Download your app:</p>
      <a href="https://example.com/app.apk" download>📥 Download App (APK)</a>
    </div>
  </div>  <script>
    const credentials = {
      username: "user123",
      password: "pass123"
    };

    function verifyLogin() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;
      const errorMsg = document.getElementById("error-msg");
      const downloadBox = document.getElementById("download-box");

      if (user === credentials.username && pass === credentials.password) {
        errorMsg.textContent = "";
        downloadBox.style.display = "block";
      } else {
        errorMsg.textContent = "Invalid username or password.";
        downloadBox.style.display = "none";
      }
    }
  </script></body>
</html>
