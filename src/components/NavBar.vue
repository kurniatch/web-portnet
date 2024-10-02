<script>
export default {
  name: "NavBar",
  data() {
    return {
      brand: "",
      options: [
        { name: "Help", link: "/admin/help" },
        { name: "Logout", link: "/" }, // Redirects to home page.
      ],
    };
  },
};
</script>

<template>
  <div class="nvbar">
    <div class="nvbar-brand">
      <img src="@/assets/logo-portnet.png" alt="Logo" class="logo" />
      {{ brand }}
    </div>
    <ol class="nv-list">
      <li v-for="opt in options" :key="opt.name">
        <router-link :to="opt.link">{{ opt.name }}</router-link>
      </li>
    </ol>
  </div>
</template>

<style scoped>
.nvbar {
  display: flex;
  align-items: center;
}

.nvbar-brand {
  display: flex;
  align-items: center;
  padding: 0 0;
  margin: 0;
}

.logo {
  width: 200px;
  height: auto;
  margin-left: 20px;
}
</style>
