<script>
    export let name = "";
    export let color = '';
    export let textc = ''
</script>

<div id="whole">
    <div id="image">
        <img src="red.jpg" alt="" />
    </div>
    <button style="background-color: {color}; color:{textc}">{name}</button>
</div>

<style lang="scss">
    #whole{
        position: relative;
        width: 300px;
        height: 150px;

        #image{
            overflow: hidden;
            border-radius: 20px;
            border: 5px solid black;
            box-sizing: border-box;
            height: 100%;
        }
        button{
            position: absolute;
            width: 300px;
            height: 150px;
            top: -10px;
            left: -10px;
            font-size: 50px;
            border-radius: 20px;
            border: 5px solid black;
            transition: transform 200ms;
            font-style: italic;
            &:active{
                transform: translate(10px,10px);    
            }
        }
    }

</style>
