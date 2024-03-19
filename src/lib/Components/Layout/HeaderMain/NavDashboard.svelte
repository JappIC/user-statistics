<nav>
    <ul>
        <li><a href="http://www.google.com">Panel 1</a></li>
        <li><a href="http://www.google.com">Panel 2</a></li>
        <li><a href="http://www.google.com">Panel 3</a></li>
        <li><a href="http://www.google.com">Panel 3</a></li>
    </ul>
</nav>

<style>
    nav{
        display: grid;
        align-items: center;

        & ul{
            display: flex;
            gap: var(--mp-m);
            
        }
    }

    /* NO PUEDO ANIDAR CSS DENTRO DE UNA MEDIA QUERIES PORQUE EL COMPILADOR DE SVELTE NO LO SOPORTA EN ESTA VERSIÓN */
    @media (max-width: 1250px) {

        nav > ul{
            flex-direction: column;
        }

    }
</style>