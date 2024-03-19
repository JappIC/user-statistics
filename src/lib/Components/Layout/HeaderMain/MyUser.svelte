<div class="my-user">
    <i class="fa-solid fa-bell"></i>
    <div>
        <img src="./assets/img/avatar.webp" alt="">
        <span>Name User</span>
    </div>
    <i class="fa-solid fa-chevron-down"></i>
</div>

<style>
    .my-user{
        display: flex;
        align-items: center;
        gap: var(--mp-m);

        & svg{
            font-size: 1rem;
        }

        & div{
            display: flex;
            align-items: center;
            gap: var(--mp-s);

            & img{
                width: 35px;
                border-radius: 50%;
                background-color: var(--c-company);
            }
        }
        
    }
</style>