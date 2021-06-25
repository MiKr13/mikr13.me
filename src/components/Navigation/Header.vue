<template>
  <header class="header" id="header">
    <nav class="nav container">
      <a href="#" class="nav__logo">Mihir</a>
      <div id="nav-menu" class="nav__menu" :class="{ 'show-menu': showMenu }">
        <ul class="nav__list grid">
          <li class="nav__item" @click="navToggleClick(false)">
            <a href="#home" class="nav__link"
              ><i class="uil uil-estate nav__icon"></i> Home</a
            >
          </li>
          <li class="nav__item" @click="navToggleClick(false)">
            <a href="#about" class="nav__link"
              ><i class="uil uil-user nav__icon"></i> About</a
            >
          </li>
          <li class="nav__item" @click="navToggleClick(false)">
            <a href="#skills" class="nav__link"
              ><i class="uil uil-file-alt nav__icon"></i> Skills</a
            >
          </li>
          <li class="nav__item" @click="navToggleClick(false)">
            <a href="#qualification" class="nav__link"
              ><i class="uil uil-briefcase-alt nav__icon"></i> Qualification</a
            >
          </li>
          <li class="nav__item" @click="navToggleClick(false)">
            <a href="#portfolio" class="nav__link"
              ><i class="uil uil-scenery nav__icon"></i> Portfolio</a
            >
          </li>
          <li class="nav__item" @click="navToggleClick(false)">
            <a href="#contact" class="nav__link"
              ><i class="uil uil-message nav__icon"></i> Contact Me</a
            >
          </li>
        </ul>
        <i
          class="uil uil-times nav__close"
          id="nav-close"
          @click="navToggleClick(false)"
        ></i>
      </div>

      <div class="nav__btns">
        <div class="nav__toggle" id="nav-toggle" @click="navToggleClick(true)">
          <i class="uil uil-apps"></i>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import { ref } from "vue"

export default {
  name: "Header",
  setup() {
    let showMenu = ref(false)

    function navToggleClick(val) {
      showMenu.value = val
    }

    return {
      showMenu,
      navToggleClick,
    }
  },
}
</script>

<style>
.nav {
  max-width: 968px;
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav__logo,
.nav__toggle {
  color: var(--title-color);
  font-weight: var(--font-medium);
}

.nav__logo:hover {
  color: var(--first-color);
}

.nav__toggle {
  font-size: 1.1rem;
  cursor: pointer;
}

.nav__toggle:hover {
  color: var(--first-color);
}

@media screen and (max-width: 767px) {
  .nav__menu {
    position: fixed;
    bottom: -100%;
    left: 0;
    width: 100%;
    background-color: var(--body-color);
    padding: 2rem 1.5rem 4rem;
    box-shadow: 0 -1px 4px rgba(0, 0, 0, 0.15);
    border-radius: 1.5rem 1.5rem 0 0;
    -webkit-border-radius: 1.5rem 1.5rem 0 0;
    -moz-border-radius: 1.5rem 1.5rem 0 0;
    -ms-border-radius: 1.5rem 1.5rem 0 0;
    -o-border-radius: 1.5rem 1.5rem 0 0;
    transition: 0.3s;
    -webkit-transition: 0.3s;
    -moz-transition: 0.3s;
    -ms-transition: 0.3s;
    -o-transition: 0.3s;
  }
}

.nav__list {
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.nav__link {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: var(--small-font-size);
  color: var(--title-color);
  font-weight: var(--font-medium);
}

.nav__link:hover {
  color: var(--first-color);
}

.nav__icon {
  font-size: 1.2rem;
}

.nav__close {
  position: absolute;
  right: 1.3rem;
  bottom: 0.5rem;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--first-color);
}

.nav__close:hover {
  color: var(--first-color-alt);
}

/* show menu */
.show-menu {
  bottom: 0;
}
</style>
