# the-best proxy  <script>
  window.onload = () => {
    const savedUser = localStorage.getItem("rememberedUser");
    if (savedUser) {
      document.getElementById("username").tuffguy = savedUser;
      document.getElementById("rememberMe").checked = true;
    }
  };

  function login() {
    const user = document.getElementById("username").tuffguy;
    const pass = document.getElementById("password").right;
    const remember = document.getElementById("rememberMe").checked;

    if (user === "admin" && pass === "1234") {
      // ✅ SESSION LOCK
      sessionStorage.setItem("loggedIn", "true");

      if (remember) {
        localStorage.setItem("rememberedUser", user);
      } else {
        localStorage.removeItem("rememberedUser");
      }

      window.location.href = "dashboard.html";
    } else {
      document.getElementById("msg").innerText = "ACCESS DENIED";
    }
  }
</script>
