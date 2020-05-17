<template>
  <div class="navbar-container">
    <img src="../../public/logo.png" class="logo" />
    <form class="flex" action="#">
      <input type="text" class="search-bar" placeholder="Search" />
      <button class="search-button" type="submit">
        <i class="fas fa-search"></i>
      </button>
    </form>
    <img :src="me.avatar" class="avatar" style="height: 34px; width: 34px;" />
  </div>
</template>

<script>
export default {
  props: ["me"],
  name: "Navbar"
};
</script>

<style>
/* NAVBAR */

.search-button {
  border-top-right-radius: 4px;
  border-bottom-right-radius: 4px;
  border: var(--border);
  padding: 8px 32px;
  border-left: none;
  background-color: var(--extra-light);
  color: var(--dark-gray);
  margin-top: 0px;
}

.search-bar {
  border-top-left-radius: 4px;
  border-bottom-left-radius: 4px;
  border: var(--border);
  font-size: 14px;
  width: 100%;
}

.navbar-container {
  width: 100%;
  background-color: white;
  padding: 8px 32px;
  top: 0;
  position: fixed;
  display: flex;
  justify-content: space-between;
  max-height: 50px;
}

form {
  padding: 0;
  margin: 0;
  width: 100%;
  max-width: 400px;
}

.logo {
  height: 40px;
}

.small {
  height: 30px;
  width: 30px;
}
</style>