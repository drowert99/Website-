<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Клевер</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<header class="header">
  <div class="logo">🍀 Клевер</div>
  <div class="search">
    <input type="text" placeholder="Поиск">
  </div>
  <div class="profile-mini">
    <img src="https://i.pravatar.cc/40" alt="">
  </div>
</header>

<div class="layout">

  <aside class="sidebar glass">
    <nav>
      <a href="#">🏠 Главная</a>
      <a href="#">📰 Новости</a>
      <a href="#">💬 Сообщения</a>
      <a href="#">👥 Друзья</a>
      <a href="#">📷 Фото</a>
      <a href="#">⚙ Настройки</a>
    </nav>
  </aside>

  <main class="feed">
    <div class="create-post glass">
      <img src="https://i.pravatar.cc/45" alt="">
      <input type="text" id="postInput" placeholder="Что нового?">
      <button onclick="addPost()">Опубликовать</button>
    </div>

    <div id="posts"></div>
  </main>

  <aside class="rightbar glass">
    <h3>Онлайн</h3>
    <div class="friend">
      <img src="https://i.pravatar.cc/30?img=1"> Иван
    </div>
    <div class="friend">
      <img src="https://i.pravatar.cc/30?img=2"> Мария
    </div>
    <div class="friend">
      <img src="https://i.pravatar.cc/30?img=3"> Алексей
    </div>
  </aside>

</div>

<script src="script.js"></script>
</body>
</html>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap');

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background: linear-gradient(135deg, #1e1e2f, #2e7d32);
  color: #fff;
}

/* Header */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  backdrop-filter: blur(20px);
  background: rgba(255,255,255,0.05);
  position: sticky;
  top: 0;
}

.logo {
  font-size: 22px;
  font-weight: 600;
}

.search input {
  padding: 8px 15px;
  border-radius: 20px;
  border: none;
  outline: none;
}

.profile-mini img {
  border-radius: 50%;
}

/* Layout */
.layout {
  display: flex;
  gap: 20px;
  padding: 30px;
  max-width: 1400px;
  margin: auto;
}

/* Glass Effect */
.glass {
  background: rgba(255,255,255,0.07);
  backdrop-filter: blur(20px);
  border-radius: 16px;
  padding: 20px;
  box-shadow: 0 8px 32px rgba(0,0,0,0.2);
}

/* Sidebar */
.sidebar {
  width: 220px;
}

.sidebar nav {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.sidebar a {
  text-decoration: none;
  color: white;
  padding: 10px;
  border-radius: 10px;
  transition: 0.3s;
}

.sidebar a:hover {
  background: rgba(255,255,255,0.1);
}

/* Feed */
.feed {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.create-post {
  display: flex;
  gap: 10px;
  align-items: center;
}

.create-post img {
  border-radius: 50%;
}

.create-post input {
  flex: 1;
  padding: 12px;
  border-radius: 25px;
  border: none;
  outline: none;
}

.create-post button {
  padding: 10px 18px;
  border-radius: 25px;
  border: none;
  background: #4caf50;
  color: white;
  cursor: pointer;
  transition: 0.3s;
}

.create-post button:hover {
  background: #66bb6a;
}

/* Post */
.post {
  padding: 20px;
  border-radius: 16px;
  background: rgba(255,255,255,0.08);
  animation: fadeIn 0.4s ease;
}

.post strong {
  display: block;
  margin-bottom: 8px;
}

@keyframes fadeIn {
  from {opacity: 0; transform: translateY(10px);}
  to {opacity: 1; transform: translateY(0);}
}

/* Rightbar */
.rightbar {
  width: 220px;
}

.friend {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-top: 10px;
}

.friend img {
  border-radius: 50%;
}
