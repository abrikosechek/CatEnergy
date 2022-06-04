<template>
  <div class="navbar">
    <div class="container">
      <router-link to="/home" class="nav_logo">
        <img src="../assets/logo.svg" />
        <p><span>CAT</span> ENERGY</p>
      </router-link>
      <div class="nav_links">
        <router-link to="/home">Главная</router-link>
        <router-link to="/catalog">Каталог продукции</router-link>
        <router-link to="/programm">Подбор программы</router-link>
      </div>
      <button class="menu_button">
        <img src="../assets/menu.svg" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavigationBar",
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.navbar {
  position: absolute;
  top: 30px;
  left: 0;
  z-index: 30;
  width: 100%;

  background-color: transparent;

  & * {
    text-transform: uppercase;
  }
}

.navbar > .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav_logo {
  display: flex;
  gap: 20px;
  align-items: center;

  img {
    height: 60px;
    width: auto;
  }
  p {
    font-size: 22px;
    font-weight: 400;
    color: black;
    span {
      font-weight: 600;
    }
  }
}

.nav_links {
  display: flex;
  gap: 20px;

  a {
    font-size: 20px;
    font-weight: 400;
    color: white;
    &.active-link {
      border-bottom: 2px solid white;
    }
  }
}

.menu_button {
  display: none;
}

@media (max-width: 768px) {
  .navbar {
    position: fixed;
    top: 0;
    left: 0;
    padding: 10px 0;

    background-color: white;
  }

  .nav_logo {
    gap: 20px;

    img {
      height: 50px;
    }
    p {
      font-size: 22px;
      font-weight: 400;
      span {
        font-weight: 600;
      }
    }
  }

  .nav_links {
    display: none;
  }

  .menu_button {
    display: block;
    height: 100%;
    border: 0;
    background-color: transparent;
  }
}

@media (max-width: 480px) {
  .nav_logo {
    gap: 20px;

    img {
      height: 38px;
    }
    p {
      font-size: 18px;
      font-weight: 400;
      span {
        font-weight: 500;
      }
    }
  }
}
</style>
