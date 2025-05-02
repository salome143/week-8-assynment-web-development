function toggleAuthForms() {
    const authSection = document.getElementById("authSection");
    authSection.style.display = authSection.style.display === "none" ? "block" : "none";
  }
  
  function showSection(sectionId) {
    const allSections = document.querySelectorAll(".content-section");
    allSections.forEach(section => section.style.display = "none");
  
    const target = document.getElementById(sectionId);
    if (target) target.style.display = "block";
  }
  
  // Registration logic
  function validateRegisterForm() {
    const name = document.getElementById("fullName").value.trim();
    const email = document.getElementById("email").value.trim();
    const phone = document.getElementById("phone").value.trim();
    const password = document.getElementById("password").value.trim();
  
    if (!name || !email || !phone || !password) {
      alert("Please fill in all fields.");
      return false;
    }
  
    const existingUser = localStorage.getItem(email);
    if (existingUser) {
      alert("This email is already registered.");
      return false;
    }
  
    localStorage.setItem(email, JSON.stringify({ name, email, phone, password }));
    alert("Registration successful!");
    return false;
  }
  
  // Login logic
  function validateLoginForm() {
    const email = document.getElementById("loginEmail").value.trim();
    const password = document.getElementById("loginPassword").value.trim();
  
    const userData = localStorage.getItem(email);
    if (!userData) {
      alert("Email not registered.");
      return false;
    }
  
    const user = JSON.parse(userData);
    if (user.password !== password) {
      alert("Incorrect password.");
      return false;
    }
  
    alert("Login successful!");
    document.getElementById("authSection").style.display = "none";
    document.getElementById("logoutLink").style.display = "inline";
    return false;
  }
  
  function logout() {
    document.getElementById("authSection").style.display = "block";
    document.getElementById("logoutLink").style.display = "none";
  }
  
