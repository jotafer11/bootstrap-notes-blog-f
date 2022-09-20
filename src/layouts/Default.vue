<template>
  <div class="layout">
    <div id="content-wrapper">
      <Header/>
      <slot/>
    </div>
    <Footer/>
  </div>
</template>

<script>
//import Footer from '../components/Footer'
import Header from '../components/Header'

export default {
  components: {
  //  Footer,
    Header,
  },
}
</script>


<style lang="scss">

@import url('https://code.jquery.com/jquery-3.2.1.slim.min.js');
@import url('https://cdn.jsdelivr.net/npm/popper.js@1.12.9/dist/umd/popper.min.js');
@import url('https://cdn.jsdelivr.net/npm/bootstrap@4.0.0/dist/js/bootstrap.min.js');



body, html {
  height: 100%;
}

body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
  background-color: #313146 !important;
  color: #dddee0 !important;
}

#app {
  display: flex;
  flex-direction: column;
  height: 100%;
}

#content-wrapper {
  flex: 1 0 auto;
  max-width: 100%;
  width: 100vw;
  margin: 0 auto;
}
</style>
