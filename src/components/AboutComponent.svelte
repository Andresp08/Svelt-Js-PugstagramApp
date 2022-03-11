<script>
    /*Logica*/

import ButtonComponent from "./ButtonComponent.svelte";

    let job = `Backend Developer at My House jeje`;
    let count = 0;
    let styles = {darkMode: false}

    function handleClick () {
        count ++;
    }

    function toogleTheme () {
        console.log('ivocado');
        styles.darkMode = !styles.darkMode;
        window.document.body.classList.toggle('dark-mode');
    }

</script>

<style>
    p{
        color: var(--theme-color);
    }
</style>


<div class="AboutComponent">
    <!---->
    
    {#if !styles.darkMode}
        <p>{job}</p>
    {:else}
        <p>
            Hello World
        </p>
    {/if}
        

    <ButtonComponent 
        text='Click' 
        count={count}
        on:click={handleClick}
    />

    <!--<ButtonComponent text='DarkMode' on:click{toogleTheme}/>-->

    <button on:click={handleClick}>Click {count === 0 ? '' : count } </button>
    <button on:click={toogleTheme}>DarkMode</button>
</div>