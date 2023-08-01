<script>
    import { count, data } from "./stores.js";
    let form = {};

    function handleAdd() {
        $count++;
        data.set([{ id: $count, ...form }, ...$data]);
        form = {};
    }
</script>

<form on:submit|preventDefault={handleAdd}>
    <input type="text" placeholder="Title" bind:value={form.title} />
    <button class="btn" type="submit">Add</button>
</form>

<style>
    form {
        display: flex;
        justify-content: space-between;
        gap: 20px;
        margin-bottom: 20px;
        width: 100%;
    }
    input{
        border-radius: 5px;
        border: none;
        outline: none;
        padding: 5px 10px;
        width: 80%;
    }
    button{
        background-color: rgb(34, 116, 34);
    }
</style>
