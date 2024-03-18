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
        background: var(--c-scale-1);
        color: var(--c-text);
        display: grid;
        grid-template-columns: auto 1fr;
        gap: var(--mp-l);
        min-height: 100vh;
        font-family: var(--font-text);
        font-size: var(--font-size-m);
    }

    .theme main{
        display: grid;
        gap: var(--mp-l);
    }

</style>