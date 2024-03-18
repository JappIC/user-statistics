<script>
    export const contactList = [
        {
            url: "https://www.google.com",
            name: "Messages",
            avatar: "https://static-00.iconduck.com/assets.00/person-icon-256x256-vioef687.png"
        },
        {
            url: "https://www.google.com",
            name: "Notification",
            avatar: "https://static-00.iconduck.com/assets.00/person-icon-256x256-vioef687.png"
        },
        {
            url: "https://www.google.com",
            name: "Friends",
            avatar: "https://static-00.iconduck.com/assets.00/person-icon-256x256-vioef687.png"
        },
        {
            url: "https://www.google.com",
            name: "Calendar",
            avatar: "https://static-00.iconduck.com/assets.00/person-icon-256x256-vioef687.png"
        },
        {
            url: "https://www.google.com",
            name: "Users",
            avatar: "https://static-00.iconduck.com/assets.00/person-icon-256x256-vioef687.png"
        },
        {
            url: "https://www.google.com",
            name: "Top charts",
            avatar: "https://static-00.iconduck.com/assets.00/person-icon-256x256-vioef687.png"
        }
    ]
</script>

<div class="contact-list">
    <h2>Dashboards</h2>
    <ul>
        {#each contactList as { url, name, avatar}}
        <li>
            <a href={url} title={name}>
                <img src={avatar} alt={name}> {name}
            </a>
        </li>
        {/each}
    </ul>
</div>

<style>
    .contact-list{
        grid-area: contact-list;
        height: max-content;
        align-self: start;
        padding: var(--mp-m);
        font-weight: bold;

        & h2{
            margin-bottom: var(--mp-m);
            font-size: var(--font-size-s);
            color: var(--c-scale-3);
        }

        & ul{
            display: grid;
            gap: var(--mp-s);

            & li{
                margin-bottom: 5px;

                & a{
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    position: relative;
                    

                    &::before{
                        content: "";
                        width: 8px;
                        height: 8px;
                        background-color: var(--c-company);
                        border-radius: 50%;
                        border: 3px solid var(--c-text); 
                        position: absolute;
                        left: 22px;
                        top: 0;
                    }

                    & img{
                        width: 30px;
                        border-radius: 50%;
                        background-color: var(--c-company);
                        
                    }

                }
            }
        }
        
    }
</style>