# Creating a ready ZIP file containing the clickable business card (index.html)
from pathlib import Path
import zipfile

content = """<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Dr Munawar Ali Mahar Clinic</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: linear-gradient(135deg, #f4f4f9, #e3f2fd);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .card {
      width: 340px;
      background: #fff;
      border-radius: 20px;
      box-shadow: 0px 8px 20px rgba(0,0,0,0.15);
      overflow: hidden;
      text-align: center;
      transition: transform 0.3s ease;
    }
    .card:hover {
      transform: translateY(-8px);
    }
    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-bottom: 2px solid #eee;
    }
    .card-content {
      padding: 20px;
    }
    .card h2 {
      margin: 10px 0 5px;
      font-size: 22px;
      color: #222;
    }
    .card p {
      margin: 0;
      font-size: 14px;
      color: #555;
    }
    .buttons {
      margin-top: 20px;
      display: flex;
      justify-content: space-around;
      gap: 10px;
    }
    .btn {
      flex: 1;
      text-align: center;
      padding: 12px;
      border-radius: 10px;
      color: white;
      text-decoration: none;
      font-size: 14px;
      font-weight: bold;
      transition: 0.3s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
    }
    .call {
      background: linear-gradient(135deg, #1e90ff, #007BFF);
    }
    .whatsapp {
      background: linear-gradient(135deg, #25D366, #128C7E);
    }
    .btn:hover {
      opacity: 0.9;
      transform: scale(1.05);
    }
    @media (max-width: 420px) {
      .card { width: 90%; }
      .card img { height: 140px; }
    }
  </style>
</head>
<body>

  <!-- Clinic Clickable Card -->
  <div class="card">
    <img src="https://cdn-icons-png.flaticon.com/512/2966/2966486.png" alt="Clinic Logo">
    <div class="card-content">
      <h2>Dr Munawar Ali Mahar Clinic</h2>
      <p>Contact us for appointments and medical consultations.</p>

      <div class="buttons">
        <a href="tel:+923009674800" class="btn call">📞 Call</a>
        <a href="https://wa.me/923009674800?text=Hello%20I%20want%20to%20book%20an%20appointment" 
           class="btn whatsapp" target="_blank">💬 WhatsApp</a>
      </div>
    </div>
  </div>

</body>
</html>


# Show result path for user to download
zip_path_str = str(zip_path)
zip_path_str

