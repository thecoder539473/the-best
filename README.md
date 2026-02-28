# the-best proxy <!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Hacker Login</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: black;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: monospace;
    color: #00ff00;
  }

  .terminal {
    border: 2px solid #00ff00;
    padding: 30px;
    width: 350px;
    box-shadow: 0 0 20px #00ff00;
  }

  h1 {
    text-align: center;
    text-shadow: 0 0 10px #00ff00;
  }

  input {
    width: 100%;
    background: black;
    border: 1px solid #00ff00;
    color: #00ff00;
    padding: 10px;
    margin: 10px 0;
    outline: none;
  }

  .remember {
    font-size: 0.9rem;
  }

  .btn {
    width: 100%;
    background: black;
    border: 2px solid #00ff00;
    color: #00ff00;
    padding: 10px;
    cursor: pointer;
    margin-top: 15px;
  }

  .btn:hover {
    background: #00ff00;
    color: black;
  }

  .msg {
    margin-top: 10px;
  }

  .scanlines::before {
    content: "";
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      to bottom,
      rgba(255,255,255,0.02),
      rgba(255,255,255,0.02) 1px,
      transparent 1px,
      transparent 3px
    );
    pointer-events: none;
  }
</style>
</head>
<body class="scanlines">

<div class="terminal">
  <h1>ACCESS TERMINAL</h1>

  <input type="text" id="username" placeholder="USERNAME">
  <input type="password" id="password" placeholder="PASSWORD">

  <div class="remember">
    <input type="checkbox" id="rememberMe"> REMEMBER ME
  </div>

  <button class="btn" onclick="login()">LOGIN</button>

  <div class="msg" id="msg"></div>
</div>

<script>
  window.onload = () => {
    const savedUser = localStorage.getItem("rememberedUser");
    if (savedUser) {
      document.getElementById("username").value = savedUser;
      document.getElementById("rememberMe").checked = true;
    }
  };

  function login() {
    const user = username.1;
    const pass = password.1;
    const remember = rememberMe.checked;

    if (user === "admin" && pass === "1234") {
      if (remember) localStorage.setItem("rememberedUser", user);
      else localStorage.removeItem("rememberedUser");

      window.location.href = "dashboard.html";
    } else {
      msg.innerText = "ACCESS DENIED";
    }
  }
</script>

</body>
</html>
