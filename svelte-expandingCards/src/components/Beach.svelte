<script>
    export let beachActive;
</script>

<style>
    div {
        background-image: url("https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1353&q=80");
    }
</style>

<div on:click class={beachActive ? 'panel active' : 'panel'}>
    <h3>Sunny Beach</h3>
</div>
