# Повторне імпортування бібліотеки після скидання середовища
from pathlib import Path

# Шлях до файлу
html_file_path = Path("/mnt/data/index_final.html")

# HTML-код з новою email-адресою
html_content = """
<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>HelpTech – Ремонт техніки у Плзені</title>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f4f7fa;
      margin: 0;
      padding: 0;
      color: #333;
    }
    header {
      background: linear-gradient(135deg, #005bbb, #003f7f);
      color: white;
      padding: 30px 20px;
      text-align: center;
    }
    .section {
      padding: 40px 20px;
      max-width: 900px;
      margin: auto;
    }
    .section h2 {
      color: #005bbb;
      margin-bottom: 10px;
    }
    .services ul {
      list-style: none;
      padding: 0;
    }
    .services li::before {
      content: '🔧';
      margin-right: 8px;
    }
    .card, .form {
      background: #fff;
      border-radius: 12px;
      padding: 25px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.05);
      margin-bottom: 30px;
    }
    input, textarea, button {
      width: 100%;
      padding: 12px;
      margin-top: 10px;
      margin-bottom: 20px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 16px;
    }
    button {
      background-color: #005bbb;
      color: white;
      border: none;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #004499;
    }
    .telegram {
      font-weight: bold;
      color: #0088cc;
    }
    footer {
      text-align: center;
      padding: 20px;
      background-color: #e6e6e6;
      font-size: 14px;
    }
    @media (max-width: 600px) {
      .section {
        padding: 20px 15px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>HelpTech – Ремонт техніки у Плзені</h1>
    <p>📞 +420 607 181 450 | 🕙 10:00 – 19:00 | Павло</p>
    <p>📩 Email: <a href="mailto:helptechofficial24@gmail.com" style="color:white;">helptechofficial24@gmail.com</a></p>
    <p>💬 Telegram: <a class="telegram" href="https://t.me/HelpTechCZ">@HelpTechCZ</a></p>
  </header>

  <div class="section services card">
    <h2>Наші послуги</h2>
    <ul>
      <li>Ремонт телефонів – екрани, батареї, роз'єми</li>
      <li>Ремонт комп’ютерів та ноутбуків – чистка, апгрейд, Windows</li>
      <li>Ремонт побутової техніки – пральні машини, мікрохвильовки</li>
      <li>Переупаковка акумуляторів електротранспорту</li>
    </ul>
  </div>

  <div class="section contact card">
    <h2>Контактна інформація</h2>
    <p>Місто: Плзень</p>
    <p>Телефон: <a href="tel:+420607181450">+420 607 181 450</a></p>
    <p>Графік роботи: з 10:00 до 19:00 щодня</p>
  </div>

  <div class="section form">
    <h2>Залишити заявку</h2>
    <form action="mailto:helptechofficial24@gmail.com" method="POST" enctype="text/plain">
      <label for="name">Ваше ім’я:</label>
      <input type="text" id="name" name="name" required>

      <label for="phone">Ваш телефон:</label>
      <input type="tel" id="phone" name="phone" required>

      <label for="device">Що потрібно відремонтувати?</label>
      <textarea id="device" name="device" rows="4" required></textarea>

      <button type="submit">Відправити заявку</button>
    </form>
  </div>

  <footer>
    &copy; 2025 HelpTech | Створено з ❤️ у Плзені
  </footer>
</body>
</html>
"""

# Зберегти файл
html_file_path.write_text(html_content, encoding="utf-8")

html_file_path.name
