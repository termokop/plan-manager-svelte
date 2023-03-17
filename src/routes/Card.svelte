<script>
    console.log('I am card')
    export let color = "green"
</script>

<div class="card" style="background-color: {color};">
    <h3>This is title of card</h3>
</div>

<style>
    .card {
        width: 180px;
        margin: 5px auto;
        border: 1px solid black;
        border-radius: 10px;
        height: 100px;

    }
</style>