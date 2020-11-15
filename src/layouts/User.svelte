<script>
    import { Router, Route } from "svelte-routing";
    import Landing from "../views/User/Landing.svelte";

    //
</script>

<Router url="user">
    <Route path="landing" component={Landing} />
</Router>
