<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mèo Đen | Personal Archive</title>
<style>
*{box-sizing:border-box}
body{
  margin:0;
  background:#09080e;
  color:#eeeaf7;
  font-family:Arial,sans-serif;
  padding:28px 16px;
}
main{max-width:650px;margin:auto}
header,.card,.quote{
  background:linear-gradient(145deg,#191522,#100e17);
  border:1px solid #30263d;
  border-radius:24px;
  padding:24px;
  margin-bottom:18px;
}
header{text-align:center;padding:32px 20px}
.avatar{
  width:125px;height:125px;
  border-radius:50%;
  object-fit:cover;
  border:3px solid #b99aff;
  padding:4px;
  background:#21182d;
}
h1{font-size:30px;letter-spacing:2px;margin:18px 0 8px}
.sub{color:#b7a5ce;margin:0}
.tag{
  display:inline-block;
  margin-top:18px;
  padding:8px 14px;
  border:1px solid #4b385e;
  border-radius:30px;
  color:#d5baff;
  font-size:13px;
}
h2{font-size:19px;margin:0 0 14px}
p{color:#c5bdcf;line-height:1.8;margin-bottom:0}
.symbol{font-size:25px;margin-bottom:15px}
.quote{
  text-align:center;
  color:#d9c5f5;
  font-family:Georgia,serif;
  font-style:italic;
  font-size:19px;
  line-height:1.8;
}
footer{text-align:center;color:#746a80;font-size:12px;padding:18px}
</style>
</head>
<body>
<main>

<header>
  <img class="avatar" src="avatar.jpg" alt="Ảnh đại diện Mèo Đen">
  <h1>MÈO ĐEN</h1>
  <p class="sub">personal archive ✦</p>
  <span class="tag">☾ A little mysterious</span>
</header>

<section class="card">
  <div class="symbol">🌑</div>
  <h2>Về tớ</h2>
  <p>
    Chào mừng đến với góc nhỏ của Mèo Đen.
    Một chút trầm lặng, một chút bí ẩn,
    và những câu chuyện mang màu sắc riêng.
  </p>
</section>

<section class="card">
  <div class="symbol">🐈‍⬛</div>
  <h2>Tớ thích</h2>
  <p>
    Mèo đen, tông màu tối, thế giới kỳ ảo,
    những câu chuyện thú vị và các cuộc trò chuyện vui vẻ.
  </p>
</section>

<section class="card">
  <div class="symbol">⛔</div>
  <h2>Lưu ý khi tương tác</h2>
  <p>
    Tôn trọng ranh giới của nhau nhé.
    Nếu có điều gì không thoải mái,
    cứ nói thẳng và lịch sự.
  </p>
</section>

<div class="quote">
  “Có những điều không cần phô bày —
  một chút bí ẩn cũng đủ tạo nên dấu ấn.”
</div>

<footer>© MÈO ĐEN · PERSONAL ARCHIVE ✦</footer>

</main>
<div id="particles-container" style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: -1;"></div>

<script>
function createParticle() {
    const container = document.getElementById('particles-container');
    const particle = document.createElement('div');
    
    // Tự động tạo kích thước và vị trí ngẫu nhiên
    const size = Math.random() * 4 + 1;
    particle.style.width = size + 'px';
    particle.style.height = size + 'px';
    particle.style.background = Math.random() > 0.5 ? '#a855f7' : '#ffffff'; // Màu tím hoặc trắng
    particle.style.position = 'absolute';
    particle.style.borderRadius = '50%';
    particle.style.top = '100%';
    particle.style.left = Math.random() * 100 + '%';
    particle.style.opacity = Math.random();
    particle.style.transition = 'all ' + (Math.random() * 4 + 4) + 's linear';
    
    container.appendChild(particle);
    
    // Tạo hiệu ứng bay lên và mờ dần
    setTimeout(() => {
        particle.style.top = '-10%';
        particle.style.left = (parseFloat(particle.style.left) + (Math.random() * 20 - 10)) + '%';
        particle.style.opacity = '0';
    }, 100);
    
    // Xóa hạt sau khi bay xong
    setTimeout(() => { particle.remove(); }, 8000);
}
// Cứ mỗi 300ms tạo 1 hạt
setInterval(createParticle, 300);
</script>
<!-- Nút bấm phát nhạc cố định ở góc dưới bên phải -->
<div id="music-player" onclick="toggleMusic()" style="position: fixed; bottom: 20px; right: 20px; width: 45px; height: 45px; background: rgba(255,255,255,0.1); backdrop-filter: blur(5px); border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; border: 1px solid rgba(255,255,255,0.2); z-index: 9999; transition: transform 0.3s;">
  <span id="music-icon" style="font-size: 20px; color: #fff;">🎵</span>
</div>

<!-- Thẻ audio ẩn (Thay link mp3 của bài bạn thích vào chỗ src) -->
<audio id="bg-audio" loop src="https://soundhelix.com"></audio>

<script>
let isPlaying = false;
function toggleMusic() {
    const audio = document.getElementById('bg-audio');
    const icon = document.getElementById('music-icon');
    const button = document.getElementById('music-player');
    
    if (!isPlaying) {
        audio.play();
        icon.innerText = '⏸️';
        button.style.animation = 'spin 4s linear infinite'; // Xoay vòng như đĩa nhạc
    } else {
        audio.pause();
        icon.innerText = '🎵';
        button.style.animation = 'none';
    }
    isPlaying = !isPlaying;
}
</script>

<style>
@keyframes spin { 100% { transform: rotate(360deg); } }
</style>

</body>
</html>

