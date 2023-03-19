<script>
    import Done from "./Done.svelte";
    import Details from "./Details.svelte"
    export let task;

    const color = () => {
        if (task.type === "family") return "#daf202bc"
        if (task.type === "work") return "#f26a02bc"
        if (task.type === "community") return "#2251fb9d"
        if (task.type === "money") return "#19b50eab"
        if (task.type === "myself") return "#ea4c1ca6"
    };
</script>

<div class="card" style="background-color: {color()};">
    <h3>
        {task.title}
    </h3>
    <p class="description">
        {task.description}
    </p>

    <p class="date">
        <code>Deadline: {task.date}</code>
    </p>
    <div class="btn">
        
        <button on:click={() => {
            alert("Open modal window with detalies") 
            ///////////////////////////////////////////////////////////////////// modal
            }}>
            <Details/>
        </button>
        <button on:click={() => {
            alert("Here will be fetch to send changing on the server") 
            ///////////////////////////////////////////////////////////////////// fetch
            }}>
            <Done/>
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
        border: 4px solid rgba(121, 126, 214, 0.243);
        border-radius: 10px;
        height: 130px;
        background-color: #ea4c1ca6
    }
    h3 {
        margin: auto;
        width: fit-content;
        font-size: 16px;
    }
    .description {
        overflow: hidden;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
    }
    .btn {
        width: 80%;
        margin: auto;
    }
    button {
        width: 70px;
        height: 50px;
        border-radius: 5px;
        border: none;
        background-color: transparent;
    }
</style>

