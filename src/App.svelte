<script>
  import Home from "./Component/Home/Home.svelte";
  import Header from "./Component/Header/Header.svelte";
  import Router from "svelte-spa-router";
  import Contact from "./Component/Contact/Contact.svelte";
  import Todo from "./Component/Todo/Todo.svelte";
  import ReactiveSum from "./Component/ReactiveSum/ReactiveSum.svelte";
  import SideBar from "./Component/Sidebar/SideBar.svelte";

  const routes = {
    "/": Home,
    "/Contact1": Contact,
    "/Contact2/:test": Contact,
    "/Todo": Todo,
    "/ReactiveSum": ReactiveSum,
  };
</script>

<header>
  <Header />
  <SideBar />
</header>
<main>
  <Router {routes} />
</main>

<style>
  main {
    margin-left: 250px;
    margin-top: 55px;
  }
</style>
