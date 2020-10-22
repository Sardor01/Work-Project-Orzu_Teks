<template>
  <b-navbar toggleable="lg" class="main__navbar">
    <div class="container-fluid py-2 px-1">
      <b-navbar-brand href="#" class="mr-auto ml-lg-5 ml-3">
        <img
          src="../assets/Logo/logo1.png"
          class="navbar__logo"
          alt="Logo"
          width="75px"
        />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="mr-auto">
          <b-nav-item class="nav__item ml-lg-5">
            <a href="#" class="nav__link">Главная</a>
          </b-nav-item>
          <b-nav-item class="nav__item">
            <a href="#" class="nav__link">О Нас</a>
          </b-nav-item>
          <b-nav-item class="nav__item">
            <a href="#" class="nav__link">Продукция</a>
          </b-nav-item>
          <b-nav-item class="nav__item">
            <a href="#" class="nav__link">Блог</a>
          </b-nav-item>
          <b-nav-item class="nav__item">
            <a href="#" class="nav__link">Медия</a>
          </b-nav-item>
          <b-nav-item class="nav__item">
            <a href="#" class="nav__link">Контакты</a>
          </b-nav-item>
        </b-navbar-nav>

        <div class="custom__select d-inline-block">
          <select>
            <option value="ru">RU</option>
            <option value="en">EN</option>
            <option value="uz">UZ</option>
          </select>
          <span class="custom__arrow">
            <b-icon icon="chevron-down" variant="dark"></b-icon>
          </span>
        </div>
      </b-collapse>
    </div>
  </b-navbar>
</template>

<script>
  export default {
    name: "Header",
  };
</script>

<style lang="scss" scoped>
</style>