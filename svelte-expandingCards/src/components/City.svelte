<script>
    export let cityActive;
</script>

<style>
    div {
        background-image: url("https://images.unsplash.com/photo-1551009175-8a68da93d5f9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1351&q=80");
    }
</style>

<div on:click class={cityActive ? 'panel active' : 'panel'}>
    <h3>City on Winter</h3>
</div>
