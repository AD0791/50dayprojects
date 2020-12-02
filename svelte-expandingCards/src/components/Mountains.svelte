<script>
    export let mountainActive;
</script>

<style>
    div {
        background-image: url("https://images.unsplash.com/photo-1549880338-65ddcdfd017b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80");
    }
</style>

<div on:click class={mountainActive ? 'panel active' : 'panel'}>
    <h3>Mountains - Clouds</h3>
</div>
