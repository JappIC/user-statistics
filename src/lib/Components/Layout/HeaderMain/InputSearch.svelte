<div class="search">
    <i class="fa-solid fa-magnifying-glass"></i>
    <input type="search" placeholder="Search messages">
</div>

<style>
    div{
        padding: 0 var(--mp-l);
        display: flex;
        align-items: center;
        border-left: var(--border);

        & svg{
            font-size: 1rem;
        }
        
        & input{
            background-color: transparent;
            border: none;
            margin-left: var(--mp-s);
            color: var(--c-text);
            padding: 5px;

            &::placeholder {
                color: var(--c-scale-3);
            }
        }
    }

    /* NO PUEDO ANIDAR CSS DENTRO DE UNA MEDIA QUERIES PORQUE EL COMPILADOR DE SVELTE NO LO SOPORTA EN ESTA VERSIÓN */
    @media (max-width: 1250px) {

        div{
            padding: 0;
            border: none;
        }

    }
</style>