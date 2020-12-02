<script>
    export let wordActive;
</script>

<style>
    div {
        background-image: url("https://images.unsplash.com/photo-1558979158-65a1eaa08691?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80");
    }
</style>

<div on:click class={wordActive ? 'panel active' : 'panel'}>
    <h3>Explore The World</h3>
</div>
