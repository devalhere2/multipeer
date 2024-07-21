<script>
    import { goto } from "$app/navigation";
</script>

<nav>
    <div id="bar">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div id="name" on:click={() => goto('/')}>
            <div style="cursor: pointer; width: fit-content;">anonCall</div>
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div id="about" on:click={() => goto('/about')}>

            <div style="cursor: pointer; width: fit-content;">about_me</div>
        </div>
        <div id="support">
            <button on:click={()=> goto('/support')}>support</button>
        </div>
    </div>
</nav>
<slot />

<style lang="scss">
    nav {
        display: flex;
        height: 80px;
        align-items: center;
        justify-content: center;
        font-family: "Courier New", Courier, monospace;
        font-weight: bold;
        border-bottom: 5px solid gold;
        box-sizing: border-box;
       
        #bar {
            display: flex;
            width: 80%;
            align-items: center;
            #name {
                flex: 1;
                font-size: 30px;
                
            }
            #about {
                padding: 0px 50px;
            }
            #support {
                height: 40px;
                background-color: red;
                border-radius: 10px;
                width: 100px;
                position: relative;
                button {
                    position: absolute;
                    font-size: large;
                    font-family: "Courier New", Courier, monospace;
                    background-color: gold;
                    border-radius: 10px;
                    top: -4px;
                    left: -4px;
                    width: 100px;
                    height: 40px;
                    border: 2px solid black;
                    cursor: pointer;
                    transition: transform 100ms;
                    &:active {
                        transform: translate(4px, 4px);
                    }
                }
            }
        }
    }
</style>
