<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-purple mb-3">
    <a class="navbar-brand" href="#">Multitaskr</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <NuxtLink class="nav-link" to="/">Dashboard <span class="sr-only">(current)</span></NuxtLink>
        </li>
        <li class="nav-item">
          <b-link class="nav-link" to="/leads">Leads in</b-link>
        </li>
        <li class="nav-item">
          <button class="btn btn-green-nav btn-sm">
            New Deal
          </button>
        </li>
      </ul>
      <ul class="navbar-nav flex-row ml-md-auto d-none d-md-flex">
        <li class="nav-item">
          <button type="button" class="btn btn-purple-ligth btn-circle">
            <fa icon="calendar-alt"/>
          </button>
        </li>
        <li class="nav-item">
          <button type="button" class="btn btn-purple-ligth btn-circle">
            <fa icon="bell"/>
          </button>
        </li>
        <li class="nav-item">
          <button type="button" class="btn btn-green btn-circle">
            JH
          </button>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script>
  
</script>
<style>

</style>