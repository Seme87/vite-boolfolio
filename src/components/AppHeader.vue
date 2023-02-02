<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header class="d-flex align-items-center">
    <div class="container ">
      <div class="d-flex align-items-center justify-content-between">
        <h2 class="m-0">Logo Boolean</h2>
        <nav class="d-flex align-items-center p-0 m-0">
          <ul class="d-flex m-0 p-0">
            <li>
              <router-link class="ms-link" :to="{ name: 'homepage' }">Home Page</router-link>
            </li>
            <li>
              <router-link class="ms-link" :to="{ name: 'about-us' }">About US</router-link>
            </li>
            <li>
              <router-link class="ms-link" :to="{ name: 'contact-us' }">Contattaci</router-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  background-color: antiquewhite;
  height: 100px;
  ul li {
    list-style: none;
    padding: 0 10px;
  }
  .ms-link {
    font-size: 15px;
    font-weight: 500;
    color: inherit;
    text-decoration: none;
  }
}
</style>
