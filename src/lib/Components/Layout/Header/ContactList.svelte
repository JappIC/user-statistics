<script>
    export const contactList = [
        {
            url: "https://www.google.com",
            name: "Messages",
            avatar: "./assets/img/avatar.webp"
        },
        {
            url: "https://www.google.com",
            name: "Notification",
            avatar: "./assets/img/avatar.webp"
        },
        {
            url: "https://www.google.com",
            name: "Friends",
            avatar: "./assets/img/avatar.webp"
        },
        {
            url: "https://www.google.com",
            name: "Calendar",
            avatar: "./assets/img/avatar.webp"
        },
        {
            url: "https://www.google.com",
            name: "Users",
            avatar: "./assets/img/avatar.webp"
        },
        {
            url: "https://www.google.com",
            name: "Top charts",
            avatar: "./assets/img/avatar.webp"
        }
    ]
</script>

<div class="contact-list">
    <h2>Contacts</h2>
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
        padding: var(--mp-m);
        font-weight: bold;
        border-top: var(--border);
        height: min-content;

        & h2{
            margin-bottom: var(--mp-m);
            font-size: var(--font-size-s);
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
                        border: 3px solid var(--c-scale-4); 
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