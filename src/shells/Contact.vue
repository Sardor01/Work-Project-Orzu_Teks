<template>
  <div class="container my-5 py-3">
    <div class="row">
      <div class="col-md-6 col-12">
        <h1 class="text-uppercase section__title">Контакты</h1>

        <div class="info mt-3">
          <div class="telephone__number">
            <small class="text-muted text-uppercase">Телефон</small>
            <div class="mt-1">+998 93 505 45 05</div>
          </div>

          <div class="address mt-3">
            <small class="text-muted text-uppercase">Адрес</small>
            <div class="mt-1">
              Узбекистан, г. Ташкент, Ул. Садыка Азимова, 68
            </div>
          </div>

          <div class="sm mt-3">
            <small class="text-muted text-uppercase">Социальные сети</small>
            <div class="mt-1">
              <a href="#"><i class="fab fa-telegram fa-2x mr-2"></i></a>
              <a href="#"><i class="fab fa-facebook fa-2x mr-2"></i></a>
              <a href="#"><i class="fab fa-instagram fa-2x"></i></a>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-12 mt-5 mt-md-0">
        <h1 class="text-uppercase section__title">Обратная связь</h1>

        <form>
          <div class="form__group mb-3">
            <input
              type="text"
              name="fullName"
              class="form__field"
              placeholder="ФИО"
            />
            <label for="fullName" class="form__label">ФИО</label>
          </div>

          <div class="form__group mb-3">
            <input
              type="text"
              name="phone"
              class="form__field"
              placeholder="Телефон"
            />
            <label for="phone" class="form__label">Телефон</label>
          </div>

          <div class="form__group mb-3">
            <textarea
              name="message"
              class="form__field"
              placeholder="Your Message"
              rows="5"
            ></textarea>
            <label for="message" class="form__label">Комментарий</label>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "ContactPage",
  };
</script>

<style lang="scss" scoped>
  .form__group {
    position: relative;
    padding: 15px 0 0;
    margin-top: 10px;
  }

  .form__field {
    font-family: inherit;
    width: 100%;
    border: 0;
    border-bottom: 1px solid #d2d2d2;
    outline: 0;
    font-size: 16px;
    color: #212121;
    padding: 7px 0;
    background: transparent;
    transition: border-color 0.2s;
  }

  .form__field::placeholder {
    color: transparent;
  }

  .form__field:placeholder-shown ~ .form__label {
    pointer-events: none;
    font-size: 16px;
    cursor: text;
    top: 20px;
  }

  label,
  .form__field:focus ~ .form__label {
    position: absolute;
    top: 0;
    display: block;
    transition: 0.2s;
    font-size: 12px;
    color: #9b9b9b;
  }

  .form__field:focus ~ .form__label {
    color: #0e19ae;
  }

  .form__field:focus {
    padding-bottom: 6px;
    border-bottom: 2px solid #0e19ae;
  }
</style>