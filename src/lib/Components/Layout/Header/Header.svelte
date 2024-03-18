<script>
	import Nav from "$lib/Components/Layout/Header/Nav.svelte";
	import ButtonNav from "./ButtonNav.svelte";
	import ContactList from "./ContactList.svelte";
	import NavOptions from "./NavOptions.svelte";
	import TitleApp from "./TitleApp.svelte";
</script>

<header>
    <ButtonNav/>
    <TitleApp/>
    <Nav/>
    <div class="navs">
        <NavOptions/>
        <ContactList/>
    </div>
    
</header>

<style>

    header{
        display: grid;
        grid-template-areas:
            "button-nav title-app"
            "nav navs"
        ;

        grid-template-columns: auto auto;
        grid-template-rows: max-content;

        & .navs{
            grid-area: navs;
            border-left: var(--border);
            border-right: var(--border);
        }
    }

    
</style>
