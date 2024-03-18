<!--
@component
Layout app:
Layout principal de la app 
-->
<script>
    // Hoja de estilos principal
    import '$lib/styles.css'

    import Header from "$lib/Components/Layout/Header/Header.svelte";
    
</script>

<!-- Contenedor principal de la plantilla -->
<div class="theme">

    <Header />

    <main>
        <slot></slot>
    </main>
  
</div>

<style>
    .theme {
        display: grid;
        grid-template-columns: auto 1fr;
        gap: var(--mp-l);
        min-height: 100vh;
    }

    .theme main{
        display: grid;
        gap: var(--mp-l);
    }

</style>