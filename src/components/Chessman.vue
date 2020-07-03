<template>
    <div class="chessman" v-bind:class="{hidden:chessmanHidden, white:whiteturn, black:blackturn}" v-on:click="showhidden()"></div>
</template>

<script>
export default {
    name: 'Chessman',
    data: function() {
            return {
                chessmanHidden: true,
                whiteturn: false,
                blackturn: true
                //show: false,
            }
        },
    methods: {
        showhidden: function() {
            if(this.chessmanHidden) {
                this.chessmanHidden = false;
            } else {
                this.chessmanHidden = true;
            }
            //alert("works");
        }
    }
}

</script>

<style>
.chessman {
    width: 42px;
    height: 42px;
    border-radius: 42px;
    margin: 8% 8%;
    position: absolute;
    z-index: 99;
    box-shadow: 3px 3px 6px black;
}
.hidden {
    opacity: 0;
}
.white {
    background: radial-gradient(circle at 65% 15%, rgb(240, 239, 239) 3px, rgb(227, 228, 228) 3%, rgb(252, 252, 252) 60%, rgb(112, 111, 111) 100%); 
}
.black {
    background: radial-gradient(circle at 65% 15%, rgb(116, 117, 117) 3px, rgb(116, 117, 117) 3%, black 60%, rgb(54, 54, 54) 100%);  
}
</style>