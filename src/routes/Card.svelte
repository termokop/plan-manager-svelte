<script>
    export let color = "green";
</script>

<div class="card" style="background-color: {color};">
    <h3>
        This is title of card
    </h3>
    <p>
        Here is description for the task
    </p>
    <div class="btn">
        <button on:click={() => console.log(color)}>
            Done!
        </button>
    </div>
</div>

<style>
    * {
        margin: 0;
        padding: 0;
    }
    .card {
        width: 180px;
        margin: 5px auto;
        border: 1px solid black;
        border-radius: 10px;
        height: 100px;
    }
    h3 {
        margin: auto;
        width: fit-content;
        font-size: 16px;
    }
    p {
        padding: 5px;
    }
    .btn {
        width: 75%;
        margin: auto;
    }
    button {
        width: 100%;
    }
</style>

