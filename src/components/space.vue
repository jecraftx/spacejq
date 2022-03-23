<template>
    <div class="space">
        <img class="ship" src="../assets/ship.png" alt="">
        <img class="bullets" src="../assets/bullet.png" alt="">
        <img class="aliens" src="../assets/alien.png" alt="">
    </div>
</template>


<script>
import $ from 'jquery'

export default {
    name: "Space",
    mounted() {
        var posX = null;
        var posY = null;
        
                
        window.addEventListener('keydown', function(event) {
            if(event.keyCode == 65) {
                posX -= 5;
                $('.ship').css('left', posX)
                console.log(posX)
            } else if(event.keyCode == 68) {
                posX += 5;
                $('.ship').css('left', posX)
                console.log(posX)
            } else if(event.keyCode == 83) {
                posY += 5;
                $('.ship').css('top', posY)
                console.log(posY)
            } else if(event.keyCode == 87) {
                posY -= 5;
                $('.ship').css('top', posY)
                console.log(posY)
            } else if(event.keyCode == 13) {
                posY -=10;
                $('.bullets').css('top', posY)
                console.log(posY)
            }
        });       
    }
}
</script>