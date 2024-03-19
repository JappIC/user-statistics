<script>
	import NavFilter from "./NavFilter.svelte";
</script>

<div>
    <h2><i class="fa-solid fa-table-cells"></i> Dashboard</h2>
    <NavFilter/>
    <button>+ Add Widjet</button>
</div>

<style>
    div{
        display: grid;
        align-items: center;
        grid-template-columns: auto 1fr auto;

        & h2{
            color: var(--c-scale-4);
            
            & svg {
                margin-right: var(--mp-s);
                color: var(--c-scale-3);
            }
        }

        & button{
            border: var(--border);
            border-radius: 25px;
            padding: var(--mp-s) var(--mp-m);
        }
    }

    /* NO PUEDO ANIDAR CSS DENTRO DE UNA MEDIA QUERIES PORQUE EL COMPILADOR DE SVELTE NO LO SOPORTA EN ESTA VERSIÓN */
    @media (max-width: 1250px) {
        div{
            grid-template-columns: 1fr;
            gap: var(--mp-m);
        }
    }
</style>