<script>

    import Board from "./Board.svelte";

    let user_name = "Yurii"; // info about user

    const date = new Date() // for Date
    const day = date.getDate()
    const month = date.getMonth() + 1
    const year = date.getFullYear()
    let date_str = `${day}/${month}/${year}`

    // task object
    let task = {
        title: "Title of Task",
        description: "Here will be detalis about this task and other information",
        date: "20/3/2023",
        finished: "",
        type: "investing"
    }

    let year_priorities = ["Стоїцизм", "Англійська", "Програмування"]
</script>



<h1> Welcome back, {user_name}! </h1>




<h2>
    Priorities in the year    
</h2>

<ol>
    <li>{year_priorities}</li>    
</ol>

<Board/>


{#if date_str === "17/3/2023"}
<h2>Today`s task-list</h2>
<ul>
    <li><del>Delete all games</del></li>    
    <li><del>Clean laptop</del></li>
    <li><del>Workout</del></li>
    <li><del>Find way to pay for hosting</del></li>
    <li><del>Cut hair</del></li>
    <li><del>Learn Svelte</del></li>
    <li>Create +2 lessons for UkrGe</li>
</ul>
{/if}

{#if date_str === "18/3/2023"}
<h2>Today`s task-list</h2>
<ul>
    <li>Learn Svelte</li>
    <li>To pay for hosting</li>
    <li>Create +2 lessons for UkrGe</li>
    <li>See information about Alberta</li>
</ul>
{/if}