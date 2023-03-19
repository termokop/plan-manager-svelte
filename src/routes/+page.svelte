<script>

    import Board from "./Board.svelte";
    import Welcome from "./Welcome.svelte";
    import Priorities from "./Priorities.svelte";

    let user_name = "Yurii"; // info about user

    const date = new Date() // for Date
    const day = date.getDate()
    const month = date.getMonth() + 1
    const year = date.getFullYear()
    let date_str = `${day}/${month}/${year}`

    // alert(Date.parse('2023-05-05'))

    // task object
    ////////////////////// here will be fetch to get tasks what is not done (from server for this month)
    // server side will not send tasks with wrong month
    let tasks = [
        {
        title: "Title of Task 1",
        description: "Here will be detalis about this task and other information",
        date: "20/3/2023",
        finished: false,
        type: "money"
        },
        {
        title: "Fly in Canada",
        description: "Here will be detalis about this task and other information",
        date: "21/3/2023",
        finished: false,
        type: "family"
        },
        {
        title: "Title of Task 1",
        description: "Here will be detalis about this task and other information",
        date: "20/3/2023",
        finished: false,
        type: "work"
        },
        {
        title: "Title of Task 1",
        description: "Here will be detalis about this task and other information",
        date: "20/3/2023",
        finished: false,
        type: "community"
        },
        {
        title: "Title of Task 1",
        description: "Here will be detalis about this task and other information",
        date: "20/3/2023",
        finished: false,
        type: "myself"
        },
        {
        title: "Title of Task 1",
        description: "Here will be detalis about this task and other information",
        date: "20/6/2023",
        finished: false,
        type: "work"
        },
    ]

    let priorities = ["Стоїцизм", "Англійська", "Програмування"]
</script>



<Welcome {user_name} />

<Priorities {priorities} />

<Board {tasks} />


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