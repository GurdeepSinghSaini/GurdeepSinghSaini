<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Your Name — Business Analytics Portfolio</title>
<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
  /* Reset & Base */
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Roboto', sans-serif; }
  body { background: #0f2027; color: #fff; overflow-x: hidden; }
  a { color: #00f0ff; text-decoration: none; }
  a:hover { color: #00ffa3; }

  /* Background animated dots */
  body::before {
    content: "";
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
    background-size: 50px 50px;
    z-index: -1;
    animation: moveBackground 30s linear infinite;
  }
  @keyframes moveBackground { 0% {background-position:0 0;} 100% {background-position:1000px 1000px;} }

  /* Container */
  .container { max-width: 1000px; margin: 0 auto; padding: 50px 20px; text-align: center; }

  /* Header */
  h1 { font-size: 3rem; margin-bottom: 20px; color: #00f0ff; }
  h2 { font-size: 1.5rem; margin-bottom: 40px; color: #fff; }

  /* Buttons */
  .btn {
    display: inline-block; padding: 12px 30px; margin: 10px;
    border: 2px solid #00f0ff; border-radius: 30px; color: #00f0ff;
    font-weight: bold; transition: 0.3s; cursor: pointer;
  }
  .btn:hover { background: #00f0ff; color: #0f2027; }

  /* Project Cards */
  .projects { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 40px; }
  .project-card {
    background: rgba(255,255,255,0.05); padding: 20px; border-radius: 15px;
    backdrop-filter: blur(10px); transition: transform 0.3s, box-shadow 0.3s;
  }
  .project-card:hover { transform: translateY(-10px); box-shadow: 0 10px 30px rgba(0,255,255,0.3); }

  .project-card h3 { margin-bottom: 10px; color: #00ffa3; }
  .project-card p { font-size: 0.95rem; color: #ddd; }
</style>
</head>
<body>
  <div class="container">
    <h1>Your Name</h1>
    <h2>Business Intelligence & Data Analytics | Python, SQL, Power BI</h2>
    <div>
      <a class="btn" href="mailto:you@example.com">Contact Me</a>
      <a class="btn" href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn</a>
      <a class="btn" href="https://github.com/your-username" target="_blank">GitHub</a>
    </div>

    <section class="projects">
      <div class="project-card">
        <h3>Retail Sales Dashboard</h3>
        <p>Interactive dashboards analyzing product demand, revenue growth, and marketing insights using Power BI & Python.</p>
        <a href="https://github.com/your-username/retail-dashboard" target="_blank">View Project</a>
      </div>
      <div class="project-card">
        <h3>Invoice Data Cleaner</h3>
        <p>Python scripts for ETL, validation, and automated reporting of invoice-level datasets for financial accuracy.</p>
        <a href="https://github.com/your-username/invoice-cleaner" target="_blank">View Project</a>
      </div>
      <div class="project-card">
        <h3>Sales Forecast Model</h3>
        <p>Machine learning-based predictive model to forecast sales and optimize inventory using Python & SQL.</p>
        <a href="https://github.com/your-username/sales-forecast" target="_blank">View Project</a>
      </div>
    </section>
  </div>
</body>
</html>
