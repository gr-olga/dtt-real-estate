<template>
  <header class="header">
    <div class="header__container">
      <img
        class="header__img"
        src="@/assets/images/img_logo_dtt@3x.png"
        alt="DTT"
      />
      <div class="header__links">
        <RouterLink
          class="header__links-item"
          to="/"
          exact
          active-class="current"
        >
          Houses
        </RouterLink>
        <RouterLink
          class="header__links-item"
          to="/about"
          active-class="current"
          >About
        </RouterLink>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "@/assets/_colors.scss" as color;

.header {
  min-height: 90px;
  background-color: white;
  display: flex;

  &__container {
    width: 80%;
    display: flex;
    flex-direction: row;
    margin: auto;
    align-items: center;
    gap: 25px;
  }

  &__img {
    max-width: 150px;
  }

  &__links {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 20px;

    &-item {
      color: color.$tertiary-element-color2;
      text-decoration: none;
      margin-left: 40px;
      font-size: 18px;
    }
  }
}

.current {
  color: color.$primary-text-color;
  font-weight: bold;
}
</style>
