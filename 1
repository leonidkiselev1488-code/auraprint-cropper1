<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Auraprint — кадрирование фото</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
    rel="stylesheet"
  />
  <link
    href="https://cdnjs.cloudflare.com/ajax/libs/cropperjs/1.5.13/cropper.min.css"
    rel="stylesheet"
  />
  <style>
    body {
      background: #121212;
      color: #fff;
      text-align: center;
      padding: 20px;
      font-family: "Inter", sans-serif;
    }
    h1 {
      font-weight: 700;
      margin-bottom: 10px;
    }
    img {
      max-width: 100%;
      display: block;
      margin: 0 auto;
      border-radius: 10px;
    }
    #preview {
      margin-top: 20px;
      border: 2px dashed #444;
      border-radius: 10px;
      padding: 10px;
    }
    .btn-format {
      margin: 5px;
      border-radius: 10px;
      font-weight: 500;
    }
  </style>
</head>
<body>
  <h1>🎞 Auraprint</h1>
  <p>Выбери фото и кадрируй под нужный формат:</p>
  <div class="mb-3">
    <button class="btn btn-outline-light btn-format" data-ratio="2/3">📸 10×15 (2:3)</button>
    <button class="btn btn-outline-light btn-format" data-ratio="1/1">🟦 10×10 (1:1)</button>
  </div>

  <input type="file" id="fileInput" accept="image/*" class="form-control mb-3">

  <div id="cropContainer" style="display:none;">
    <img id="image" alt="Фото для кадрирования">
    <button id="cropBtn" class="btn btn-success w-100 mt-2">✅ Отправить в бота</button>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/cropperjs/1.5.13/cropper.min.js"></script>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <script>
    const tg = window.Telegram.WebApp;
    tg.expand();

    const fileInput = document.getElementById('fileInput');
    const image = document.getElementById('image');
    const cropContainer = document.getElementById('cropContainer');
    const cropBtn = document.getElementById('cropBtn');
    const formatBtns = document.querySelectorAll('.btn-format');

    let cropper;
    let aspectRatio = 2 / 3; // формат по умолчанию

    formatBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        formatBtns.forEach(b => b.classList.remove('btn-primary'));
        btn.classList.add('btn-primary');
        aspectRatio = eval(btn.dataset.ratio);
        if (cropper) cropper.setAspectRatio(aspectRatio);
      });
    });

    fileInput.addEventListener('change', (e) => {
      const file = e.target.files[0];
      if (!file) return;
      const url = URL.createObjectURL(file);
      image.src = url;
      cropContainer.style.display = 'block';

      if (cropper) cropper.destroy();
      cropper = new Cropper(image, {
        aspectRatio,
        viewMode: 1,
        background: false,
        autoCropArea: 1,
      });
    });

    cropBtn.addEventListener('click', () => {
      const canvas = cropper.getCroppedCanvas({
        width: 900,
        height: Math.round(900 / aspectRatio),
      });
      canvas.toBlob((blob) => {
        const reader = new FileReader();
        reader.onloadend = () => {
          const base64 = reader.result;
          tg.sendData(base64); // Отправляем кадр обратно в Telegram-бот
          tg.close();
        };
        reader.readAsDataURL(blob);
      });
    });
  </script>
</body>
</html>
