<template>
  <div id="app">
    <img src="./assets/logo.png">
    {{#router}}
    <router-view></router-view>
    {{else}}
    <hello></hello>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import Hello from './components/Hello'{{#if_eq lintConfig "airbnb"}};{{/if_eq}}

{{/unless}}
export default {
  name: 'app'{{#router}}{{#if_eq lintConfig "airbnb"}},{{/if_eq}}{{else}},
  components: {
    Hello{{#if_eq lintConfig "airbnb"}},{{/if_eq}}
  }{{#if_eq lintConfig "airbnb"}},{{/if_eq}}{{/router}}
}{{#if_eq lintConfig "airbnb"}};{{/if_eq}}
</script>

<style{{#bootstrap}}lang="scss"{{/bootstrap}}>
  {{^bootstrap}}
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  {{/bootstrap}}
  {{#bootstrap}}
  // Core variables and mixins
  @import "scss/bootstrap/variables";
  @import "../node_modules/bootstrap/scss/mixins";

  // Reset and dependencies
  @import "../node_modules/bootstrap/scss/normalize";
  @import "../node_modules/bootstrap/scss/print";

  // Core CSS
  @import "../node_modules/bootstrap/scss/reboot";
  @import "../node_modules/bootstrap/scss/type";
  @import "../node_modules/bootstrap/scss/images";
  @import "../node_modules/bootstrap/scss/code";
  @import "../node_modules/bootstrap/scss/grid";
  @import "../node_modules/bootstrap/scss/tables";
  @import "../node_modules/bootstrap/scss/forms";
  @import "../node_modules/bootstrap/scss/buttons";

  // Components
  @import "../node_modules/bootstrap/scss/transitions";
  @import "../node_modules/bootstrap/scss/dropdown";
  @import "../node_modules/bootstrap/scss/button-group";
  @import "../node_modules/bootstrap/scss/input-group";
  @import "../node_modules/bootstrap/scss/custom-forms";
  @import "../node_modules/bootstrap/scss/nav";
  @import "../node_modules/bootstrap/scss/navbar";
  @import "../node_modules/bootstrap/scss/card";
  @import "../node_modules/bootstrap/scss/breadcrumb";
  @import "../node_modules/bootstrap/scss/pagination";
  @import "../node_modules/bootstrap/scss/badge";
  @import "../node_modules/bootstrap/scss/jumbotron";
  @import "../node_modules/bootstrap/scss/alert";
  @import "../node_modules/bootstrap/scss/progress";
  @import "../node_modules/bootstrap/scss/media";
  @import "../node_modules/bootstrap/scss/list-group";
  @import "../node_modules/bootstrap/scss/responsive-embed";
  @import "../node_modules/bootstrap/scss/close";

  // Components w/ JavaScript
  @import "../node_modules/bootstrap/scss/modal";
  @import "../node_modules/bootstrap/scss/tooltip";
  @import "../node_modules/bootstrap/scss/popover";
  @import "../node_modules/bootstrap/scss/carousel";

  // Utility classes
  @import "../node_modules/bootstrap/scss/utilities";

  // Contents
  // @import "scss/transitions";
  {{/bootstrap}}
</style>
