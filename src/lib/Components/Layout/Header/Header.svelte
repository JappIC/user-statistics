<script>
	import Nav from "$lib/Components/Layout/Header/Nav.svelte";
	import ButtonNav from "./ButtonNav.svelte";
	import ContactList from "./ContactList.svelte";
	import NavOptions from "./NavOptions.svelte";
	import TitleApp from "./TitleApp.svelte";

    let navActive = false;

    // Funcion para ocultar o mostrar el navegador de opciones usando condicionales.
    const btnNavActive = ()=>{
        navActive = !navActive;
    }
</script>

<header>
    <div class="nav">
        <ButtonNav on:click={btnNavActive}/>
        <Nav/>
    </div>
    <div class="nav-options-user" class:navActive>
        <TitleApp/>
        <NavOptions/>
        <ContactList/>
    </div>
    
</header>

<style>

    header{
        display: grid;
        grid-template-columns: auto auto;

        & > div{
            display: grid;
            grid-template-columns: 1fr;
        }

        & .nav{
            grid-template-rows: 60px 1fr;
            border-right: var(--border);
        }

        & .nav-options-user{
            grid-template-rows: 60px auto auto;
            align-content: start;
            border-right: var(--border);
        }
    }

    .navActive{
        display: none;
    }

    
</style>
