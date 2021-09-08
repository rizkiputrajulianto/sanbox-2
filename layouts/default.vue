<template>
  <div id="app">
    <div class="main-wrapper">
      <partials-navbar />
      <div class="main-sidebar">
        <partials-sidebar />
      </div>

      <!-- Main Content -->
      <div class="main-content">
        <section class="section">
          <div class="section-header">
            <h1>Blank Page</h1>
          </div>

          <div class="section-body"></div>
          <nuxt />
        </section>
      </div>
      <partials-footer />
    </div>
  </div>
</template>