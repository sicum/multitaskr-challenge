<template>
  <div>
    <NavBar/>
    <Nuxt />
  </div>
</template>

<style>
  html {
    font-family:
      'Source Sans Pro',
      -apple-system,
      BlinkMacSystemFont,
      'Segoe UI',
      Roboto,
      'Helvetica Neue',
      Arial,
      sans-serif;
    font-size: 16px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
  }

  *,
  *::before,
  *::after {
    box-sizing: border-box;
    margin: 0;
  }
  h1 {
    font-weight: bold;
  }
  .bg-purple {
    background-color: #4813B0;
  }
  .navbar-light .navbar-brand {
    color:#fff;
  }
  .navbar-light .navbar-brand:hover {
    color:#fff;
  }
  .navbar-purple .navbar-brand {
    color:#fff;
  }
  .navbar-purple .navbar-brand:hover {
    color:#fff;
  }
  .navbar-brand {
    display: inline-block;
    padding-top: 0.3125rem;
    padding-bottom: 0.3125rem;
    margin-right: 1rem;
    font-size: 1.25rem;
    line-height: inherit;
    white-space: nowrap;
  }
  .navbar-light .navbar-nav .show > .nav-link, .navbar-light .navbar-nav .active > .nav-link, .navbar-light .navbar-nav .nav-link.show, .navbar-light .navbar-nav .nav-link.active {
    color: #fff;
    font-weight: bold;
  }
  .navbar-light .navbar-nav .nav-link:hover, .navbar-light .navbar-nav .nav-link:focus {
    color: #E8E8E8;
  }
  .navbar-light .navbar-nav .nav-link {
    color: #fff;
  }
  .navbar-light .navbar-nav .nav-link :hover {
    color: #E8E8E8;
  }

  .btn-green {
    color: #4813B0;
    font-weight: bold;
    background-color: #58FA82;
    border-color: #58FA82;
  }
  .btn-green:hover {
    color: #4813B0;
    font-weight: bold;
    background-color: #01DFA5;
    border-color: #58FA82;
  }
  .btn-purple-ligth {
    margin-left: 0.3rem;
    margin-right: 0.3rem;
    color: #4813B0;
    font-weight: bold;
    background-color: #AE88F9;
    border-color: #AE88F9;
  }
  .btn-purple-ligth:hover {
    margin-left: 0.3rem;
    margin-right: 0.3rem;
    color: #4813B0;
    font-weight: bold;
    background-color: #AE88F9;
    border-color: #AE88F9;
  }
  .btn-green-nav {
    margin-top: 4px;
    color: #4813B0;
    font-weight: bold;
    background-color: #58FA82;
    border-color: #58FA82;
  }
  .btn-green-nav:hover {
    margin-top: 4px;
    color: #4813B0;
    font-weight: bold;
    background-color: #01DFA5;
    border-color: #01DFA5;
  }
  .btn-circle.btn-xl {
      width: 70px;
      height: 70px;
      padding: 10px 16px;
      border-radius: 35px;
      font-size: 24px;
      line-height: 1.33;
  }

  .btn-circle {
      width: 30px;
      height: 30px;
      padding: 6px 0px;
      border-radius: 15px;
      text-align: center;
      font-size: 12px;
      line-height: 1.42857;
  }
</style>
