<template>
  <div>
    <aside id="sidebar-wrapper">
      <div class="sidebar-brand">
        <a href="index.html">Stisla</a>
      </div>
      <div class="sidebar-brand sidebar-brand-sm">
        <a href="index.html">St</a>
      </div>
      <ul class="sidebar-menu">
        <li class="active">
          <nuxt-link to="/sandbox"
            ><i class="far fa-square"></i> <span>Blank Page</span></nuxt-link
          >
        </li>
      </ul>

      <div class="mt-4 mb-4 p-3 hide-sidebar-mini">
        <a
          href="https://getstisla.com/docs"
          class="btn btn-primary btn-lg btn-block btn-icon-split"
        >
          <i class="fas fa-rocket"></i> Documentation
        </a>
      </div>
    </aside>
  </div>
</template>
<script>
export default {};
</script>