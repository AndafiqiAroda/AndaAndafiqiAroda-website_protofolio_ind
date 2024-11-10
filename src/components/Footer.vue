<script setup>

</script>

<template>
  <footer class="py-4 mt-auto">
    <div class="container px-5">
      <div class="row align-items-center justify-content-between flex-column flex-sm-row">
        <div class="col-auto"><div class="small m-0">&copy; {{new Date().getFullYear()}} <a href="https://www.linkedin.com/in/andafiqi/" class="text-decoration-none text-body ms-2 fs-6" target="_blank">@andafiqi</a></div></div>
        <div class="col-auto mt-2 mt-md-0">
          <template v-if="$route.path !== '/'">
            <RouterLink to="/" class="small text-decoration-none text-body">Beranda</RouterLink>
            <span class="mx-1">&middot;</span>
          </template>
          <template v-if="$route.path !== '/resume'">
            <RouterLink to="/resume" class="small text-decoration-none text-body">Resume</RouterLink>
            <span class="mx-1">&middot;</span>
          </template>
          <template v-if="$route.path !== '/project'">
            <RouterLink to="/project" class="small text-decoration-none text-body">Projek</RouterLink>
            <span v-if="$route.path !== '/contact'" class="mx-1">&middot;</span>
          </template>
          <template v-if="$route.path !== '/contact'">
            <RouterLink to="/contact" class="small text-decoration-none text-body">Kontak</RouterLink>
          </template>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>

</style>