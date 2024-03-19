<div>
    <nav>
        <ul>
            <li><a href="http://www.google.es">Today</a></li>
            <li><a href="http://www.google.es">Week</a></li>
            <li><a href="http://www.google.es">Month</a></li>
            <li><a href="http://www.google.es">Quarter</a></li>
            <li><a href="http://www.google.es">Year</a></li>
        </ul>
    </nav>
    <input type="date">
</div>

<style>
    div{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: var(--mp-s);

        & nav{ 
            
            & ul{
                display: flex;

                & li{

                    & a{
                        border: var(--border);
                        padding: var(--mp-s);
                        border-right: 0;
                    }

                    &:nth-child(1) a{
                        border-radius: 20px 0 0 20px;
                        padding-left: var(--mp-m);
                    }

                    &:nth-child(5) a{
                        border-radius: 0 20px 20px 0;
                        border-right: var(--border);
                        padding-right: var(--mp-m);
                    }
                }
            }
        }

        & input{
            border: var(--border);
            padding: var(--mp-s) var(--mp-m);
            border-radius: 20px;
            background-color: transparent;
            color: var(--c-scale-3);
        }
    }

    /* NO PUEDO ANIDAR CSS DENTRO DE UNA MEDIA QUERIES PORQUE EL COMPILADOR DE SVELTE NO LO SOPORTA EN ESTA VERSIÓN */
    @media (max-width: 1250px) {
        div{
            flex-direction: column;
            gap: var(--mp-m);
        }
    }
</style>