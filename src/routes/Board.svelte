<script>
    import Card from './Card.svelte'

    export let tasks = [];

    let family = []
    let work = []
    let community = []
    let money = []
    let myself = []

    function sortTasks(tasks) {
        tasks.forEach(task => {
            if (task.type === "family") family.push(task)
            if (task.type === "work") work.push(task)
            if (task.type === "community") community.push(task)
            if (task.type === "money") money.push(task)
            if (task.type === "myself") myself.push(task)
        })
    }
    sortTasks(tasks)
    
</script>

<div class="board">
    <div class="title">
        <h2>
            Board of month
        </h2>
    </div>
    <div class="board_type">
        <h3>Family</h3>
        {#each family as task}
            <Card {task}/>
        {/each}
    </div>
    <div class="board_type">
        <h3>Work</h3>
        {#each work as task}
            <Card {task}/>
        {/each}
    </div>
    <div class="board_type">
        <h3>Community</h3>
        {#each community as task}
            <Card {task}/>
        {/each}
    </div>
    <div class="board_type">
        <h3>Investing</h3>
        {#each money as task}
            <Card {task}/>
        {/each}
    </div>
    <div class="board_type">
        <h3>Myself</h3>
        {#each myself as task}
            <Card {task}/>
        {/each}
    </div>
</div>

<style>
    .board {
        width: 1010px;
        margin: auto;
        border: 20px solid rgba(0, 0, 0, 0.315);
        border-radius: 25px;
        background-color: beige;
        height: 600px;
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
        border: none;
    }
</style>