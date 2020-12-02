<script>
    export let forestActive;
</script>

<style>
    div {
        background-image: url("https://images.unsplash.com/photo-1572276596237-5db2c3e16c5d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80");
    }
</style>

<div on:click class={forestActive ? 'panel active' : 'panel'} style="">
    <h3>Wild Forest</h3>
</div>
