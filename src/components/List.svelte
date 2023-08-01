<script>
    import Item from "./Item.svelte";
    import { data } from "./stores.js";
    import axios from 'axios';

    axios.get('http://10.0.2.2:8080/api/promotions').then(res=>{
        data.set(res.data);
    });
</script>

<ul>
    {#each $data as row}
        <Item id={row.id_prom} title={row.name_prom} />
    {/each}
</ul>

<style>
    ul {
        list-style: none;
        display: flex;
        flex-direction: column;
        gap: 15px;
        width: 100%;
    }
</style>
