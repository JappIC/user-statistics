<script>
    export const optionList = [
        {
            url: "https://www.google.com",
            title: "Messages"
        },
        {
            url: "https://www.google.com",
            title: "Notification"
        },
        {
            url: "https://www.google.com",
            title: "Friends"
        },
        {
            url: "https://www.google.com",
            title: "Calendar"
        },
        {
            url: "https://www.google.com",
            title: "Users"
        },
        {
            url: "https://www.google.com",
            title: "Top charts"
        }
    ]
</script>

<div class="nav-options">
    <h2>Dashboards</h2>
    <ul>
        {#each optionList as { url, title}}
        <li>
            <a href={url} {title}>
                {title}
            </a>
        </li>
        {/each}
    </ul>
</div>

<style>
    .nav-options{
        padding: var(--mp-m);
        font-weight: bold;

        & h2{
            margin-bottom: var(--mp-m);
            font-size: var(--font-size-s);
        }

        & ul{
            display: grid;
            gap: var(--mp-s);
        }
        
    }
</style>