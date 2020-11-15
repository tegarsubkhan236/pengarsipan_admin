<!-- App.svelte -->
<script>
  import { Router, Route } from "svelte-routing";

  //Layout
  import Admin from "./layouts/Admin.svelte";
  import Auth from "./layouts/Auth.svelte";
  import Author from "./layouts/Author.svelte";
  import User from "./layouts/User.svelte";

  // No Layout Pages
  import Index from "./views/Index.svelte";

  export let url = "";
</script>

<Router {url}>
  <!-- layout -->
  <Route path="admin/*admin" component={Admin} />
  <Route path="author/*author" component={Author} />
  <Route path="user/*user" component={User} />
  <Route path="auth/*auth" component={Auth} />
  <!-- No layout Pages -->
  <Route path="/" component={Index} />
</Router>
