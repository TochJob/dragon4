<template>
    <div class="games">
        <div class="game" v-for="(item, index) of games" :key="index">
            <h2 class="game__title">{{ item.title }}</h2>
            <p class="game__text">{{ item.players }}</p>
            <a href="" class="game__link">Запустить</a>
        </div>
    </div>
</template>
<script>

export default {
    name: 'gamesList',
    data() {
        return {
            games: [
                {
                    title: 'Double Game',
                    players: '75 игроков'
                },
                {
                    title: 'Dice',
                    players: '213 игроков'
                },
                {
                    title: 'Mines',
                    players: '168 игроков'
                },
                {
                    title: 'Crash Game',
                    players: '175 игроков'
                },
                {
                    title: 'Overgo',
                    players: '66 игроков'
                },
                {
                    title: 'Jackpot',
                    players: '194 игроков'
                },
                {
                    title: 'Raffle',
                    players: '102 игроков'
                },
                {
                    title: 'Nvuti',
                    players: '35 игроков'
                }
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
.games {
    display: flex;
    text-align: left;
    flex-wrap: wrap;
    gap: 20px;

    .game {
        background-color: #547AFF;
        box-shadow: 0px 1px 10px rgba(236, 222, 49, 0.2);
        border-radius: 10px;
        flex: 1 0 21%; /* explanation below */
        padding: 0 0 10px 10px;

        &__title {
            font-family: 'Arial';
            font-style: normal;
            font-weight: 700;
            font-size: 22px;
            line-height: 25px;
            color: #FFFFFF;
            padding: 10px 0 0 0;
        }

        &__text {

            font-family: 'Raleway';
            font-style: normal;
            font-weight: 300;
            font-size: 12px;
            line-height: 12px;
            color: #FFFFFF;
            padding: 0 0 39px 0;
            margin: 10px 0;
            display: flex;
            align-items: center;
            &::before{
                content: '';
                display: block;
                width: 10px;
                height: 10px;
                border-radius: 50%;
                background: #00FF00;
                margin: 0 8px 0 0;
            }
        }

        &__link {
            text-decoration: none;
            font-family: 'Arial';
            font-style: normal;
            font-weight: 700;
            font-size: 14px;
            line-height: 40px;
            color: #220F09;
            cursor: pointer;
            background: linear-gradient(270deg, #FFB309 0%, #EEA849 100%);
            border-radius: 8px;
            text-align: center;
            align-items: center;
            padding: 10px 20px;        
        }
    }
}
</style>