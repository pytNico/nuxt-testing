<template>
  <header>
    <div>
      <b-navbar toggleable="lg" type="dark" variant="dark">
        <b-navbar-brand to="/">Nuxt-Testing</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item
              to="/"
              exact
              active-class="active"
              exact-active-class="active"
            >
              Home
            </b-nav-item>
            <b-nav-item
              to="/Deck"
              exact
              active-class="active"
              exact-active-class="active"
            >
              Deck
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style></style>
