# the-best proxy <!DOCTYPE html>
<html>
<head>
<title>Hacker Dashboard</title>
<style>
  body {
    margin: 0;
    background: black;
    color: #00ff00;
    font-family: monospace;
  }

  .topbar {
    border-bottom: 2px solid #00ff00;
    padding: 15px;
    text-shadow: 0 0 10px #00ff00;
  }

  .content {
    padding: 20px;
  }

  .box {
    border: 1px solid #00ff00;
    padding: 15px;
    margin: 15px 0;
    box-shadow: 0 0 10px #00ff00;
  }

  button {
    background: black;
    color: #00ff00;
    border: 1px solid #00ff00;
    padding: 8px 15px;
    cursor: pointer;
  }

  button:hover {
    background: #00ff00;
    color: black;
  }
</style>
</head>
<body>

<div class="topbar">
  ROOT ACCESS GRANTED
</div>

<div class="content">
  <div class="box">🌐 Proxy Status: ONLINE</div>
  <div class="box">🧠 AI Core: ACTIVE</div>
  <div class="box">📡 Network Scan: READY</div>

  <button onclick="logout()">LOGOUT</button>
</div>

<script>
  function logout() {
    window.location.href = "login.html";
  }
</script>

</body>
</html>
