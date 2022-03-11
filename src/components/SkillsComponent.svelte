<script>
    let skills = [
        {
            id: 1,
            name: 'ReactJs'
        },
        {
            id:2,
            name: 'SvelteJs'
        },
        {
            id:3,
            name: 'Javascript'
        }
    ]
</script>

<style>
    .SkillsComponent{
        display: flex;
        align-items: center;
        justify-content: center;
    }

    ul{
        margin: 0;
        padding: 0;
        list-style: none;
    }

    li {
        display: inline;
        margin: 0 0 0 .4em;
    }
</style>

<div class="SkillsComponent">

    <h3>Habilidades</h3>

    <ul>
        <!--Desestructurar el name-->
        {#each skills as {name}, i}
            <li>{name}</li>
        {/each}
    </ul>
</div>
