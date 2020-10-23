<template>
  <div class="container">
    <div class="py-5 footer__nav">
      <div class="row justify-content-between align-items-center">
        <div
          class="col-lg-5 col-sm-6 col-12 py-3 d-flex justify-content-center align-items-center"
        >
          <a href="#" class="footer__brand">
            <img src="../assets/Logo/footerLogo.png" alt="Footer Logo" />
          </a>
        </div>
        <div
          class="col-lg-5 col-sm-6 col-12 py-3 d-flex justify-content-center align-items-center"
        >
          <div class="row justify-content-between">
            <div class="col-sm-5 col-6">
              <b-list-group class="footer__list__group text-uppercase">
                <b-list-group-item class="footer__list__group__item">
                  <a href="#" class="footer__link">Главная</a>
                </b-list-group-item>
                <b-list-group-item class="footer__list__group__item">
                  <a href="#" class="footer__link">О Нас</a>
                </b-list-group-item>
                <b-list-group-item class="footer__list__group__item">
                  <a href="#" class="footer__link">Продукция</a>
                </b-list-group-item>
              </b-list-group>
            </div>

            <div class="col-sm-5 col-6">
              <b-list-group class="footer__list__group text-uppercase">
                <b-list-group-item class="footer__list__group__item">
                  <a href="#" class="footer__link">Блог</a>
                </b-list-group-item>
                <b-list-group-item class="footer__list__group__item">
                  <a href="#" class="footer__link">Медия</a>
                </b-list-group-item>
                <b-list-group-item class="footer__list__group__item">
                  <a href="#" class="footer__link">Контакты</a>
                </b-list-group-item>
              </b-list-group>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="copyright-licences py-4">
      <div class="row justify-content-between align-items-center py-2">
        <div
          class="col-lg-5 col-md-6 col-sm-12 d-flex justify-content-center align-items-center"
        >
          <p>"Orzu Teks" Все права защищены</p>
        </div>
        <div
          class="col-lg-5 col-md-6 col-sm-12 mt-1 mt-md-0 d-flex justify-content-center align-items-center"
        >
          <p>
            &copy; Copyright {{ new Date().getFullYear() }} - Web developed by
            <a href="http://sos.uz" class="grey__link">SOS Group</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Footer",
  };
</script>

<style lang="scss" scoped>
  .footer__list__group__item {
    border: none !important;
  }

  .footer__link {
    font-weight: 500;
    font-size: 0.75rem;

    &:hover {
      color: #0e19ae;
      border-bottom: 2px solid #0e19ae;
    }
  }

  .copyright-licences {
    color: #a19baa;

    p {
      font-size: 0.875rem;
      padding: 0;
      margin: 0;
    }
  }
</style>