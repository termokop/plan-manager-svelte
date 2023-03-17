<script>
    console.log("this is board")

    import Card from './Card.svelte'
</script>

<div class="board">
    <div class="title">
        <h2>
            Board of month
        </h2>
    </div>
    <div class="board_type">
        <h3>Family</h3>
        <Card color="red"/>
    </div>
    <div class="board_type">
        <h3>Work</h3>
        <Card color="pink"/>
    </div>
    <div class="board_type">
        <h3>Community</h3>
        <Card color="lightblue"/>
    </div>
    <div class="board_type">
        <h3>Investing</h3>
        <Card color="green"/>
    </div>
    <div class="board_type">
        <h3>Myself</h3>
        <Card color="yellow"/>
        <Card color="yellow"/>
        <Card color="yellow"/>
    </div>
</div>

<style>
    .board {
        width: 1010px;
        margin: auto;
        border: 1px solid black;
        height: 300px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        align-content: flex-start;
        overflow-y: hidden;
    }
    h2, h3 {
        width: fit-content;
        margin: auto;
        padding: 5px;
    }
    .title {
        width: 100%;
        height: fit-content;
    }
    .board_type {
        width: 200px;
        /* height: 100%; */
        border: 1px solid blue;
    }
</style>