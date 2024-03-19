<!--
@component
Layout app:
Layout principal de la app 
-->
<script>
    // Hoja de estilos principal
    import '$lib/styles.css'

    import Header from "$lib/Components/Layout/Header/Header.svelte";
	import HeaderMain from '../lib/Components/Layout/HeaderMain/HeaderMain.svelte';
    import DashboarFilters from "$lib/Components/Layout/DashboarFilters/DashboarFilters.svelte";
    
</script>

<!-- Contenedor principal de la plantilla -->
<div class="theme">

    <Header />

    <main>
        <HeaderMain/>
        <div>
            <DashboarFilters/>
            <slot></slot>
        </div>
    </main>
  
</div>

<style>
    .theme {
        display: grid;
        grid-template-columns: auto 1fr;
        min-height: 100vh;

        & main{
            display: grid;
            grid-template-rows: 60px 1fr;
            
            & > div{
                padding: var(--mp-m);
            }
        }
    }

</style>