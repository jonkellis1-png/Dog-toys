<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>3D Dog Toys</title>
<style>
  * { box-sizing: border-box; }

  body {
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
    overflow-x: hidden;
  }

  /* NAV BAR */
  .nav-container {
    width: 100%;
    background-color: #111;
    position: fixed;
    top: 0;
    z-index: 1000;
  }

  .nav {
    max-width: 900px; /* aligns with page content */
    width: 100%;
    display: flex;
    justify-content: space-between; /* links left, logo right */
    align-items: center;
    padding: 0 20px;
    height: 60px;
    margin: auto;
  }

  .nav-links {
    display: flex;
    gap: 20px;
  }

  .nav-links a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    cursor: pointer;
  }

  .nav-links a:hover {
    text-decoration: underline;
  }

  .logo {
    font-size: 1.4em;
    font-weight: bold;
    color: white;
  }

  /* PAGE SECTIONS */
  .page { display: none; min-height: 100vh; padding-top: 80px; width: 100%; }
  .active { display: block; }

  /* HOME */
  #home {
    background: linear-gradient(135deg, #00ffd5, #00bfff);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
  }
  #home h1 { font-size: 5em; letter-spacing: 4px; margin: 0; }

  /* INVENTORY */
  #inventory { background-color: #f2f6f8; padding: 100px 20px; }
  #inventory h1 { text-align: center; margin-bottom: 40px; }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    max-width: 900px;
    margin: auto;
  }

  .card {
    background: white;
    padding: 30px;
    text-align: center;
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    font-size: 1.2em;
    font-weight: bold;
  }

  /* ABOUT */
  #about { background-color: white; padding: 100px 20px; }
  #about .content {
    max-width: 800px;
    margin: auto;
    line-height: 1.7;
    font-size: 1.1em;
  }
  #about h1 { margin-bottom: 20px; }
</style>
</head>
<body>

  <!-- NAV BAR -->
  <div class="nav-container">
    <div class="nav">
      <div class="nav-links">
        <a onclick="showPage('home')">Home</a>
        <a onclick="showPage('inventory')">Inventory</a>
        <a onclick="showPage('about')">About Me</a>
      </div>
      <div class="logo">3D Dog Toys</div>
    </div>
  </div>

  <!-- HOME PAGE -->
  <div id="home" class="page active">
    <h1>DOG TOYS</h1>
  </div>

  <!-- INVENTORY PAGE -->
  <div id="inventory" class="page">
    <h1>Inventory</h1>
    <div class="grid">
      <div class="card">TPU Bone</div>
      <div class="card">TPU Fish Bone</div>
      <div class="card">Customizable PLA Dog Bowl</div>
    </div>
  </div>

  <!-- ABOUT PAGE -->
  <div id="about" class="page">
    <div class="content">
      <h1>About Me</h1>
      <p>
        My name is Jonathan Kellis, I'm 13 years old, and I go to Dexter Southfield
        School. I speak 3 languages including Greek, French, and English.
      </p>
      <p>
        I just recently got a dog named Pooka and she is only 2 months old.
        She gave me the idea to make this project.
      </p>
      <p>
        You can contact me to buy the dog toys at 857 *** 1983 or at
        30kellijo@dextersouthfield.org.
      </p>
    </div>
  </div>

  <!-- PAGE SWITCHING SCRIPT -->
  <script>
    function showPage(pageId) {
      const pages = document.querySelectorAll('.page');
      pages.forEach(page => page.classList.remove('active'));
      document.getElementById(pageId).classList.add('active');
      window.scrollTo(0, 0);
    }
  </script>

</body>
</html>
