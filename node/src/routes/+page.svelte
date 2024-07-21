<script>
    import Button from "$lib/comp/Button.svelte";
</script>

<div id="main">
    <div id="create">
        <Button name="Create" color="#22929e" textc='wheat'/>
    </div>
    <div id="join">
        <Button name="Join" color="#FFC7C7" textc='#7D5A50'/>
    </div>
</div>

<style lang="scss">
    #main{
        display: flex;
        height: calc(100vh - 80px);
        justify-content: center;
        align-items: center;
        div {
            margin: 0px 20px;
        }
    }
</style>