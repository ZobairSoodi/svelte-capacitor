<script>
  import svelteLogo from "./assets/svelte.svg";
  import Add from "./components/Add.svelte";
  import List from "./components/List.svelte";
  import Counter from "./lib/Counter.svelte";
</script>

<div id="container">
  <div>
    <Add />
    <List />
  </div>
</div>

<style>
  #container {
    display: flex;
    justify-content: center;
    width: 100%;
    padding: 20px;
  }
  #container > div{
    display: flex;
    flex-direction: column;
    width: 100%;
  }
  @media(min-width: 1201px){
    #container > div{
      width: 60%;
    }
  }
  @media(max-width: 1200px){
    #container > div{
      width: 70%;
    }
  }
  @media(max-width: 1000px){
    #container > div{
      width: 80%;
    }
  }
  @media(max-width: 768px){
    #container > div{
      width: 90%;
    }
  }

  @media(max-width: 580px){
    #container > div{
      width: 100%;
    }
  }
</style>
