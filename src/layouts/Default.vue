<template>
  <div class="layout">
      <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-light fixed-top" id="mainNav">
      <div class="container">
        <g-link class="navbar-brand" to="/post/">blog logo</g-link>
        <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
          Menu
          <i class="fas fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <g-link class="nav-link"  to="/" >Journal</g-link>
            </li>
            <li class="nav-item">
              <g-link class="nav-link" to="/contact/">Say Hi</g-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
      <slot/>


  </div>
</template>
