<!DOCTYPE html>
<html lang="ar">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تحميل تطبيق AnManga</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background: #333;
      color: white;
      position: relative;
    }

    /* الخلفية المتحركة */
    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('https://media1.giphy.com/media/tTmyoOKxqYD2zB8sDN/giphy.gif?cid=6c09b9528tqi5y4g5y2qpvsodv51r8kua0jdjou0wpht24ss&ep=v1_internal_gif_by_id&rid=giphy.gif&ct=g') center center/cover no-repeat;
      opacity: 0.25;
      z-index: -2;
      animation: move 20s infinite linear;
    }

    /* تنسيق النصوص الرئيسية مع الظلال */
    .header {
      padding: 20px;
      z-index: 1;
      position: relative;
      color: white;
    }

    .header h1,
    .header p {
      text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.8);
      /* إضافة الظلال */
    }

    /* صورة التطبيق */
    .app-image {
      width: 150px;
      height: 150px;
      margin: 20px auto;
      background-image: url('https://drive.google.com/uc?export=view&id=1-035b4HDDWwwe4_13jVmQK9o6CjSRyP3');
      background-size: cover;
      display: inline-block;
      border-radius: 50%;
      position: relative;
      top: -30px;
      /* تعديل للموقع ليتناسب مع النص */
    }

    .container {
      padding: 20px;
      z-index: 1;
      position: relative;
    }

    .features {
      text-align: left;
      margin: 20px auto;
      max-width: 600px;
      color: white;
    }

    /* زر تحميل APK مع تأثيرات اللون */
    .download-button {
      background-color: #4CAF50;
      color: white;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      cursor: pointer;
      text-decoration: none;
      border-radius: 5px;
      transition: background-color 0.3s ease;
    }

    .download-button:hover {
      background-color: #d32f2f;
      /* اللون الأحمر عند المرور */
      color: white;
    }

    /* شريط الحقوق السفلي مع تأثير اللون */
    .footer {
      background-color: #4CAF50;
      color: white;
      padding: 10px;
      position: fixed;
      width: 100%;
      bottom: 0;
      z-index: 1;
      text-align: center;
      transition: background-color 0.3s ease;
    }

    .footer:hover {
      background-color: #d32f2f;
      /* اللون الأحمر عند المرور */
    }

    /* تأثير السحب للأسفل */
    .scroll-down {
      position: absolute;
      bottom: 30px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 24px;
      color: #fff;
      cursor: pointer;
      animation: bounce 1.5s infinite;
    }

    @keyframes bounce {

      0%,
      20%,
      50%,
      80%,
      100% {
        transform: translateY(0);
      }

      40% {
        transform: translateY(-10px);
      }

      60% {
        transform: translateY(-5px);
      }
    }
  </style>
</head>

<body>

  <!-- الخلفية المتحركة -->
  <div class="background"></div>

  <div class="header">
    <!-- صورة التطبيق فوق النص "مرحبًا بك في AnManga" -->
    <div class="app-image"></div>
    <h1>مرحبًا بك في AnManga!</h1>
    <p>تطبيقك المفضل لمتابعة أحدث المانجا والمانهوا.</p>
  </div>

  <!-- مؤشر السحب للأسفل -->
  <div class="scroll-down" onclick="scrollToContent()">👇 اسحب لأسفل لقراءة المزيد</div>

  <div class="container" id="content">
    <h2>لماذا تطبيق AnManga؟</h2>
    <p>يعتبر AnManga تطبيقًا شاملًا ومميزًا لعشاق المانجا والمانهوا. تمتع بتجربة تصفح سلسة مع واجهة مستخدم بسيطة، واطلع على مجموعة واسعة من القصص المثيرة والمليئة بالتشويق.</p>

    <!-- قسم مميزات التطبيق -->
    <div class="features">
      <h3>مميزات التطبيق:</h3>
      <ul>
        <li>مجموعة ضخمة من المانجا والمانهوا الشهيرة.</li>
        <li>واجهة سهلة الاستخدام ومناسبة لجميع الأعمار.</li>
        <li>إمكانية حفظ الفصول للقراءة بدون اتصال.</li>
        <li>تحديثات مستمرة لأحدث الفصول.</li>
        <li>إشعارات للتحديثات الجديدة.</li>
      </ul>
    </div>

    <h2>تحميل تطبيق AnManga الآن</h2>
    <p>استمتع بتجربة قراءة سلسة لجميع المانجا والمانهوا على جهازك الأندرويد. قم بتحميل التطبيق الآن واكتشف عوالم جديدة من القصص المثيرة!</p>

    <!-- زر تحميل APK -->
    <a href="https://drive.google.com/uc?export=download&id=1-3dkLrib79D6O0MTuspd168_8jkWs3U5" class="download-button" download>تحميل الآن</a>
  </div>

  <!-- شريط الحقوق السفلي -->
  <div class="footer">
    <p>© 2024 AniGo. جميع الحقوق محفوظة. | تطوير: kamal</p>
  </div>

  <script>
    // وظيفة السحب للأسفل
    function scrollToContent() {
      document.getElementById("content").scrollIntoView({
        behavior: "smooth"
      });
    }
  </script>

</body>

</html>
