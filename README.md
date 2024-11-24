<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>أداة تحسين المحتوى الاحترافية</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f8f9fa;
      color: #333;
    }
    header {
      background-color: #007bff;
      color: white;
      padding: 20px;
      text-align: center;
      border-bottom: 2px solid #0056b3;
    }
    .container {
      max-width: 900px;
      margin: 20px auto;
      padding: 20px;
      background: white;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
    }
    .button {
      background-color: #007bff;
      color: white;
      padding: 12px 24px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      margin-top: 10px;
    }
    .button:hover {
      background-color: #0056b3;
    }
    .idea-box, .analysis-box {
      margin-top: 20px;
      padding: 10px;
      background-color: #f1f1f1;
      border-left: 4px solid #007bff;
      border-radius: 4px;
    }
    .link-button {
      background-color: #28a745;
      color: white;
      padding: 8px 16px;
      text-decoration: none;
      border-radius: 4px;
    }
    .link-button:hover {
      background-color: #218838;
    }
    .header-info {
      text-align: center;
      font-size: 1.2rem;
      color: #555;
    }
    footer {
      background-color: #343a40;
      color: white;
      text-align: center;
      padding: 10px;
      position: fixed;
      width: 100%;
      bottom: 0;
    }
  </style>
</head>
<body>

<header>
  <h1>أداة تحسين المحتوى الاحترافية</h1>
  <p class="header-info">ساعدك على تحسين محتواك وتنمية حساباتك على منصات التواصل الاجتماعي</p>
</header>

<div class="container">
  <h2>اقتراح أفكار جديدة</h2>
  <p>أدخل مجالك وسيتم اقتراح أفكار جذابة:</p>
  <input type="text" id="field" placeholder="مثل: الأزياء، الرياضة..." style="width: 100%; padding: 10px; font-size: 1rem; border: 1px solid #ccc; border-radius: 4px;">
  <button class="button" onclick="generateIdea()">توليد فكرة</button>

  <div id="ideaBox" class="idea-box" style="display:none;">
    <p id="idea"></p>
  </div>

  <h3>تحليل التفاعل:</h3>
  <p>سنقدم لك نصائح لتحسين تفاعلك مع المتابعين:</p>
  <button class="button" onclick="getAnalysis()">تحليل التفاعل</button>
  
  <div id="analysisBox" class="analysis-box" style="display:none;">
    <p id="analysis"></p>
    <a href="https://www.canva.com" class="link-button" target="_blank">استخدم Canva لتصميم صورك</a>
  </div>
</div>

<footer>
  <p>حقوق الطبع والنشر © 2024 <strong>يونس العمراوي</strong>. جميع الحقوق محفوظة.</p>
</footer>

<script>
  function generateIdea() {
    const field = document.getElementById('field').value;
    const ideas = {
      "الأزياء": ["نصائح تنسيق الألوان", "تصميم أزياء للمواسم", "أسرار الموضة العصرية"],
      "الرياضة": ["تمارين منزلية سهلة", "تحليل مباريات الأسبوع", "أفضل معدات اللياقة البدنية"],
      "التكنولوجيا": ["أحدث الهواتف الذكية", "مراجعات البرامج", "أدوات تسهل حياتك اليومية"],
      "السفر": ["أفضل وجهات السياحة لعام 2024", "نصائح السفر بأقل تكلفة", "أفضل أدوات السفر"]
    };

    const randomIdea = ideas[field] ? ideas[field][Math.floor(Math.random() * ideas[field].length)] : "أدخل مجالًا صحيحًا.";
    document.getElementById('idea').innerText = randomIdea;
    document.getElementById('ideaBox').style.display = 'block';
  }

  function getAnalysis() {
    const analysis = `
      1. حاول نشر المحتوى في أوقات الذروة مثل صباح الجمعة أو مساء السبت.
      2. استخدم هاشتاغات ذات صلة وشعبية.
      3. تفاعل مع متابعينك بشكل دوري لتزيد من التفاعل.
      4. انشر محتوى مرئي مثل الفيديوهات والصور عالية الجودة لجذب المزيد من المتابعين.
    `;
    document.getElementById('analysis').innerText = analysis;
    document.getElementById('analysisBox').style.display = 'block';
  }
</script>

</body>
</html>
