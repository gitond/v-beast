<script setup>
    /*
        the game is played in a 25y40x grid
    */
    let gamestate = [];
    // filling the gamestate with empty tiles
    for (let i = 0; i<25; i++){
        gamestate.push([]);
        for (let j = 0; j<40; j++){
            gamestate[i].push("e");
        }
    }

    // test & debug area
    // --- //
    //gamestate[13][19] = "p";
    //console.log(gamestate);
    //<span v-for="n in 1000">{{ gamestate[n] }}</span>
</script>

<template>
    <div class="gamescene">
        <table>
            <caption>Placeholder</caption>
            <tbody>
                <tr v-for="row in gamestate">
                    <td v-for="j in 40">{{ row[j] }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<style scoped></style>