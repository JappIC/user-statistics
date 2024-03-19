<script>
    export let  navActive = false;
    
    const list = [
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-solid fa-house"
        },
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-solid fa-table-cells"
        },
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-regular fa-message"
        },
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-regular fa-calendar"
        },
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-solid fa-user"
        },
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-solid fa-user-group"
        },
        {
            url: "http://www.google.com",
            title: "Home",
            icon: "fa-regular fa-image"
        },
    ]
</script>
    
<nav>
    <ul>
        {#each list as { url, title, icon }}
        <li>
            <a href={url} {title}>
                <i class={icon}></i>
            </a>
        </li>
        {/each}
    </ul>
    
</nav>

<style>
    nav {
        display: grid;
        padding: var(--mp-m);
        align-items: center;
        
        & ul{
            list-style: none;
            padding: 0;
            display: grid;
            gap: 40px;

            & li {
                
                & a {
                    text-align: center;
                    width: 30px;
                    display: block;
                    font-size: var(--font-size-m);
                }
            }
        }
    }

    @media (max-width: 1250px) {
        nav{
            padding: var(--mp-s);
        }

        nav ul {
            gap: 20px;
        }

        nav ul li a{
            width: 20px;
            font-size: var(--font-size-s);
        }
    }
</style>