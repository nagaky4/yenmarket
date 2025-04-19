<template>
  <header class="header">
    <div class="header__left">
      <div class="logo"><NuxtImg src="/images/logo.png" /></div>
    </div>
    <div class="header__right">
      <nav>
        <ul>
          <li
            v-for="menu in menuList"
            :key="menu.text"
            class="menu"
            @click="navigateTo(menu.link)"
          >
            {{ menu.text }}
          </li>
        </ul>
      </nav>
      <div class="language">
        <NuxtImg
          src="/icons/flag-vi.svg"
          :class="{ active: isLang === 'VI' }"
          @click="isLang = 'VI'"
        />
        <NuxtImg
          src="/icons/flag-en.svg"
          :class="{ active: isLang === 'EN' }"
          @click="isLang = 'EN'"
        />
      </div>
    </div>
  </header>
  <div class="line"></div>
</template>

<script setup lang="ts">
interface IMenu {
  text: string;
  link: string;
}
const menuList = ref<Array<IMenu>>([
  {
    text: "Home",
    link: "/",
  },
  {
    text: "Products",
    link: "/products",
  },
]);

const isLang = ref<"VI" | "EN">("VI");
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
  padding: 1rem 2rem;
  background: #f8f9fa;

  &__left {
    flex-shrink: 0;
  }

  &__right {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    gap: 2rem;
    ul {
      display: flex;
      justify-content: center;
      align-items: flex-end;
      gap: 2rem;
      list-style: none;

      li.menu {
        font-size: 1.8rem;
        color: #4c4c4c;
        cursor: pointer;
        &:hover {
          color: #7b7575;
        }
      }
    }

    .language {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      gap: 0.8rem;
      cursor: pointer;
      img {
        opacity: 0.6;
        &.active {
          opacity: 1;
        }
      }
    }
  }
}

.line {
  background: #ca2628;
  height: 3.6rem;
  width: 100%;
}
</style>
