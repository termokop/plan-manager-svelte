<script>
    export let priorities;
</script>

<h2>
    Priority of the year
</h2>

<ol>
    {#each priorities as priority}
        <li>{priority}</li>
    {/each}
    
</ol>