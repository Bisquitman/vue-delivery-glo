<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-box">
        <router-link to="./" class="footer-logo logo">
          <img src="../assets/img/logo.svg" alt="Логотип сайта">
        </router-link>

        <div class="footer-nav">
          <ul>
            <li><router-link to="./rest" class="nav-link">Ресторанам</router-link></li>
            <li><router-link to="./rest" class="nav-link">Курьерам</router-link></li>
            <li><router-link to="./rest" class="nav-link">Пресс-центр</router-link></li>
            <li><router-link to="./rest" class="nav-link">Контакты</router-link></li>
          </ul>
        </div>

        <div class="footer-social">
          <ul>
            <li>
              <a href="https://instagram.com" class="social-link" target="_blank" rel="noopener noreferrer">
                <img src="../assets/img/social/s-insta.svg" alt="Instagram">
              </a>
            </li>
            <li>
              <a href="https://facebook.com" class="social-link" target="_blank" rel="noopener noreferrer">
                <img src="../assets/img/social/s-fb.svg" alt="Facebook">
              </a>
            </li>
            <li>
              <a href="https://vk.com" class="social-link" target="_blank" rel="noopener noreferrer">
                <img src="../assets/img/social/s-vk.svg" alt="VK">
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
/* Footer */

.footer {
  display: flex;
  align-items: center;
  min-height: 156px;
  background-color: #fff;
  padding: 60px 0;
}

.footer-box {
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 35px;
}

.footer-logo {
}

.footer-nav {
  flex-grow: 1;
}

.footer-nav ul {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 15px;
}

.nav-link {
  color: #595959;
  -webkit-transition: color 0.2s;
  -moz-transition: color 0.2s;
  -ms-transition: color 0.2s;
  -o-transition: color 0.2s;
  transition: color 0.2s;
}

.nav-link:hover {
  color: #000;
}

.footer-social ul {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 20px;
}
</style>