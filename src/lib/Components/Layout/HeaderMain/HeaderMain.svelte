<script>
	import InputSearch from "./InputSearch.svelte";
	import MyUser from "./MyUser.svelte";
    import NavDashboard from "./NavDashboard.svelte";

    let navMainActive = false;

    const btnNavMainActive = ()=>{
        navMainActive = !navMainActive;
    }
</script>

<header>
    <div class:navMainActive>
        <NavDashboard/>
        <InputSearch/>
        <MyUser/>
    </div>
    
    <div>
        <label>
            <input type="checkbox" id="dark-mode-button" />
            <svg  
                xmlns='http://www.w3.org/2000/svg' 
                width='20' height='20' 
                viewBox="0 0 24 24"
            >
                <title>sun</title>
                <g id="sun_line" fill='none' fill-rule='nonzero'>
                    <path d='M24 0v24H0V0h24ZM12.593 23.258l-.011.002-.071.035-.02.004-.014-.004-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01-.017.428.005.02.01.013.104.074.015.004.012-.004.104-.074.012-.016.004-.017-.017-.427c-.002-.01-.009-.017-.017-.018Zm.265-.113-.013.002-.185.093-.01.01-.003.011.018.43.005.012.008.007.201.093c.012.004.023 0 .029-.008l.004-.014-.034-.614c-.003-.012-.01-.02-.02-.022Zm-.715.002a.023.023 0 0 0-.027.006l-.006.014-.034.614c0 .012.007.02.017.024l.015-.002.201-.093.01-.008.004-.011.017-.43-.003-.012-.01-.01-.184-.092Z'/>
                    <path fill='currentColor' d='M12 19a1 1 0 0 1 1 1v1a1 1 0 1 1-2 0v-1a1 1 0 0 1 1-1Zm6.364-2.05.707.707a1 1 0 0 1-1.414 1.414l-.707-.707a1 1 0 0 1 1.414-1.414Zm-12.728 0a1 1 0 0 1 1.497 1.32l-.083.094-.707.707a1 1 0 0 1-1.497-1.32l.083-.094.707-.707ZM12 6a6 6 0 1 1 0 12 6 6 0 0 1 0-12Zm0 2a4 4 0 1 0 0 8 4 4 0 0 0 0-8Zm-8 3a1 1 0 0 1 .117 1.993L4 13H3a1 1 0 0 1-.117-1.993L3 11h1Zm17 0a1 1 0 1 1 0 2h-1a1 1 0 1 1 0-2h1ZM4.929 4.929a1 1 0 0 1 1.32-.083l.094.083.707.707a1 1 0 0 1-1.32 1.497l-.094-.083-.707-.707a1 1 0 0 1 0-1.414Zm14.142 0a1 1 0 0 1 0 1.414l-.707.707a1 1 0 1 1-1.414-1.414l.707-.707a1 1 0 0 1 1.414 0ZM12 2a1 1 0 0 1 1 1v1a1 1 0 1 1-2 0V3a1 1 0 0 1 1-1Z'/>
                </g>
            </svg>
            
            <svg  
                xmlns='http://www.w3.org/2000/svg' 
                width='20' height='20' 
                viewBox="0 0 24 24"
            >
                <title>moon</title>
                <g id="moon_stars_line" fill='none' fill-rule='evenodd'>
                    <path d='M24 0v24H0V0h24ZM12.593 23.258l-.011.002-.071.035-.02.004-.014-.004-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01-.017.428.005.02.01.013.104.074.015.004.012-.004.104-.074.012-.016.004-.017-.017-.427c-.002-.01-.009-.017-.017-.018Zm.265-.113-.013.002-.185.093-.01.01-.003.011.018.43.005.012.008.007.201.093c.012.004.023 0 .029-.008l.004-.014-.034-.614c-.003-.012-.01-.02-.02-.022Zm-.715.002a.023.023 0 0 0-.027.006l-.006.014-.034.614c0 .012.007.02.017.024l.015-.002.201-.093.01-.008.004-.011.017-.43-.003-.012-.01-.01-.184-.092Z'/>
                    <path fill='currentColor' d='M12.477 4.546c-.335-.747.307-1.548 1.097-1.409A9 9 0 0 1 12 21c-4.434 0-8.118-3.206-8.863-7.426-.14-.79.662-1.432 1.409-1.097a6 6 0 0 0 7.931-7.931Zm2.404 1.072a8 8 0 0 1-9.263 9.263A7.002 7.002 0 0 0 19 12.001a7.002 7.002 0 0 0-4.12-6.383ZM5.565 7.716l.064.14a3.26 3.26 0 0 0 1.237 1.363l.1.059a.068.068 0 0 1 0 .118l-.1.058a3.26 3.26 0 0 0-1.237 1.364l-.064.14a.071.071 0 0 1-.13 0l-.064-.14a3.26 3.26 0 0 0-1.237-1.364l-.1-.058a.068.068 0 0 1 0-.118l.1-.059A3.26 3.26 0 0 0 5.37 7.855l.064-.14a.071.071 0 0 1 .13 0Zm2.832-4.859c.04-.09.166-.09.206 0l.102.222a5.189 5.189 0 0 0 1.97 2.172l.157.092a.108.108 0 0 1 0 .189l-.158.092a5.189 5.189 0 0 0-2.07 2.394.113.113 0 0 1-.207 0l-.102-.222a5.189 5.189 0 0 0-1.97-2.172l-.158-.092a.108.108 0 0 1 0-.189l.158-.092a5.189 5.189 0 0 0 1.97-2.172l.102-.222Z'/>
                </g>
            </svg>
        </label>
        <button on:click={btnNavMainActive}>
            <i class="fa-solid fa-bars"></i>
        </button>
    </div>
</header>

<style>
    header{
        display: grid;
        grid-template-columns: 1fr auto;
        background-color: var(--c-scale-2);
        border-bottom: var(--border);
        padding: 0 var(--mp-l);

        & > div:nth-child(1){
            display: grid;
            grid-template-columns: auto 1fr auto;
            gap: var(--mp-l);
            font-weight: bold;
        }

        & > div:nth-child(2){
            display: flex;
            align-items: center;
            justify-self: end;
            gap: var(--mp-s);
            margin-left: var(--mp-l);
            

            & button{
                
                & svg{
                    font-size: 1rem;
                }
            }

            & label {
                display: grid;
                align-items: center;
                cursor: pointer;
                color: var(--c-text);

                & :hover{
                    color: var(--c-scale-4);
                }
            
                & svg {
                    height: 25px;
                    width: 25px;
                    transition: var(--transition);
                }
            
                & #dark-mode-button {
                    display: none;
            
                    @media (prefers-color-scheme: light) {
                        & ~ svg:has(#sun_line) {
                            display: none;
                        }
                
                        &:checked {
                            & ~ svg:has(#sun_line) {
                                display: block;
                            }
                        
                            & ~ svg:has(#moon_stars_line) {
                                display: none;
                            }
                        }
                    }
            
                    @media (prefers-color-scheme: dark) {
                        & ~ svg:has(#moon_stars_line) {
                            display: none;
                        }
                        
                        &:checked {
                            & ~ svg:has(#moon_stars_line) {
                                display: block;
                            }
                        
                            & ~ svg:has(#sun_line) {
                                display: none;
                            }
                        }
                    }
                }
            } 
        }
    }

    /* NO PUEDO ANIDAR CSS DENTRO DE UNA MEDIA QUERIES PORQUE EL COMPILADOR DE SVELTE NO LO SOPORTA EN ESTA VERSIÓN */
    @media (max-width: 1250px) {

        header > div:nth-child(1){
            display: grid;
            grid-template-columns: 1fr;
            background-color: var(--c-scale-2);
            position: absolute;
            top: 70px;
            left: 5px;
            width: min-content;
            border: var(--border);
            padding: var(--mp-m);
            gap: var(--mp-m);
        }
        
    }

    

    .navMainActive{
        display: none !important;
    }

    
</style>