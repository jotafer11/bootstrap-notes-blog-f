<template>
  <header class="header">
    <b-navbar class="p-0" toggleable="md" type="light">
        <b-navbar-brand>
        <g-link class="logo-home logo-desktop ml-3" to="/">{{ $static.metadata.siteName }}</g-link>
        <g-link class="logo-home logo–mobile" to="/"><img class="logo-image" alt="logo" src="../assets/images/logo.png"></g-link>
      </b-navbar-brand>
        <b-navbar-nav class="ml-auto mr-3">
          <h3>
            <a href="https://jotafer11.github.io" target="_blank">            
              <i class="bi bi-globe2 ml-3"></i>
            </a>

            <a href="https://github.com/jotafer11" target="_blank">
                <i class="bi bi-github ml-3"></i> 
            </a>               
          </h3>        
        </b-navbar-nav>
    </b-navbar>
  </header>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style lang="scss" scoped>
nav {
  width: 100%;
  padding-top: 1rem;
  background-color: #0a0a23;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

a, i {
  color: white;
}

.logo-home {
  font-size: 24px;
  max-width: 75%;
  font-weight: bold;
  &:hover {
    text-decoration: none;
  }
}

.logo-desktop {
  @media(max-width: 419px) {
    display: none;
  }
  @media (min-width: 420px) {
    display: default;
  }
}

.logo–mobile {
  @media(max-width: 419px) {
    display: default;
  }
  @media (min-width: 420px) {
    display: none;
  }
}

.logo-image {
  width: 40px;
}

.nav--link {
  margin-left: 20px;
  @media (max-width: 419px) {
    margin: 0;
    padding: 15px 10px 10px 0;
  }
}

.active--exact {
  font-weight: bold;
}
</style>
