<template>
  <div class="header-container">
    <UContainer class="h-container">
      <div>
        <div class="header-logo">
          <UAvatar src="https://avatars.githubusercontent.com/u/739984?v=4" alt="Avatar" />
          <router-link to="/">jeffrey</router-link>
        </div>
      </div>
      <ul class="header-menu">
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/about">About</router-link>
        </li>
      </ul>
    </UContainer>
  </div>
</template>
<style scoped lang="scss">
.header-container {
  height: 64px;
  line-height: 64px;
  border-bottom: 1px solid #cccc;

  .h-container {
    display: flex;
    justify-content: space-between;

    .header-logo {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
    }
    .header-menu {
      display: flex;
      gap: 20px;
      font-size: 14px;
    }
  }

}
</style>
