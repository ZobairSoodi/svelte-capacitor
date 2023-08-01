<script>
    import { data } from "./stores.js";
    export let title = "";
    export let id = "";

    function handleDelete(e) {
        console.log(e.target.getAttribute("data-id"));
        data.set(
            $data.filter(
                (item) =>
                    Number(item.id) != Number(e.target.getAttribute("data-id"))
            )
        );
    }
</script>

<li>
    <span>{title}</span>
    <button class="btn" data-id={id} on:click={handleDelete}>delete</button>
</li>

<style>
    li{
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: large;
        width: 100%;
    }
    li span{
        overflow-wrap: break-word;
        width: 80%;
    }
    button{
        font-size: medium;
        padding: 5px 10px;
        color: white;
        background-color: brown;
        border: none;
        border-radius: 5px;
    }
    @media(max-width: 580px){
        li span{
            max-width: 360px;
        }
    }
</style>