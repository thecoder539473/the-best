<script>
  window.onload = () => {
    const savedUser = localStorage.getItem("rememberedUser");
    if (savedUser) {
      document.getElementById("username").value = savedUser;
      document.getElementById("rememberMe").checked = true;
    }
  };

  function login() {
    const user = document.getElementById("username").value;
    const pass = document.getElementById("password").value;
    const remember = document.getElementById("rememberMe").checked;

    let users = JSON.parse(localStorage.getItem("users")) || {
      admin: "1234" // default account
    };

    if (users[user] && users[user] === pass) {
      sessionStorage.setItem("loggedIn", "true");

      if (remember) localStorage.setItem("rememberedUser", user);
      else localStorage.removeItem("rememberedUser");

      window.location.href = "dashboard.html";
    } else {
      msg.innerText = "ACCESS DENIED";
    }
  }
