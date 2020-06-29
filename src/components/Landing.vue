<template>
    <div>
        <Chessboard></Chessboard>
        <div class="alert">
        <span class="closebtn" onclick="this.parentElement.style.display='none';">&times;</span> 
        <strong>Danger!</strong> Indicates a dangerous or potentially negative action.
        </div>
    </div>
</template>

<script>
import Chessboard from './Chessboard';

export default {
    name: "Landing",
    compoents: {
        Chessboard,
    }
}
</script>