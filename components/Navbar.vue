<template>
<header>
	<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container">
    <nuxt-link class="navbar-brand" to="/">MMA TOWN</nuxt-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/news-social" no-prefetch>News & Social</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/events" no-prefetch>Events</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/rankings" no-prefetch>Rankings</nuxt-link>
        </li>
		  <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/videos" no-prefetch>Videos</nuxt-link>
        </li>
		  <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/gyms" no-prefetch>Gyms</nuxt-link>
        </li>
		   <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/odds" no-prefetch>Odds</nuxt-link>
        </li>
          <li class="nav-item">
          <nuxt-link active-class="active" class="nav-link" to="/login" no-prefetch>Login</nuxt-link>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
	</nav>
</header>
</template>