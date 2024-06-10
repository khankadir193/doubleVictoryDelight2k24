<template>
    <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description="leaderDescription" />
    <div v-for="user in content" :key="user.id">
        <!-- <div class="col4 top1" v-if="user.busUserId === '5017266'">
            <div class="rank-top3">
            </div>
            <div class="user-profile">
                <button class="profile-Imgbg">
                    <img :src="user.userAvatar" alt="" class="user-profile-img">
                </button>
                <span class="user-name">{{ user.userName }}</span>
            </div>
            <div class="left-align">
                <img src="../assets/images/beansIcon.png" alt="beansIcon" />
                <span class="beans-amount">1M</span>
            </div>
            <div class="center-align">
                22K
            </div>
        </div> -->

        <!-- <div class="col4 top2" v-if="user.busUserId === '5017268'">
            <div class="rank-top3">
            </div>
            <div class="user-profile">
                <button class="profile-Imgbg">
                    <img :src="user.userAvatar" alt="" class="user-profile-img">
                </button>
                <span class="user-name">{{ user.userName }}</span>
            </div>
            <div class="left-align">
                <img src="../assets/images/beansIcon.png" alt="beansIcon" />
                <span class="beans-amount">1M</span>
            </div>
            <div class="center-align">
                22K
            </div>
        </div> -->
        <div :class="getClassByUserId(user.busUserId)">
            <p v-if="user.busUserId === '5017271'" class="User">6</p>
            <p v-else-if="user.busUserId === '5017305'" class="User">7</p>
            <div v-else class="rank-top3">
            </div>
            <div class="user-profile">
                <button class="profile-Imgbg">
                    <img :src="user.userAvatar" alt="" class="user-profile-img">
                </button>
                <span class="user-name">{{ user.userName }}</span>
            </div>
            <div class="left-align">
                <img src="../assets/images/beansIcon.png" alt="beansIcon" />
                <span class="beans-amount">1M</span>
            </div>
            <div class="center-align">
                22K
            </div>
        </div>

    </div>

</template>

<script>
import LeaderBoardDesc from './LeaderBoardDesc.vue';

export default {
    name: 'OverAllComp',
    components: {
        LeaderBoardDesc
    },
    data() {
        return {
            showLeaderBoard: true,
            leaderBoardTitle: "OverAll",
            leaderDescription: " The Top 5 Rebate Card users with most beans get extra rewards.",
            content: null,
            loading: true,
            error: null
        }
    },
    mounted() {
        this.fetchData();
    },
    methods: {
        async fetchData() {
            try {
                const response = await fetch('http://voice-cluster-314173693.cn-northwest-1.elb.amazonaws.com.cn:8090/oyetalk-marketing/activity/ranking?activityCode=rebate_20240611&rankingRuleId=1297&size=10');
                console.log('response..', response);
                if (!response.ok) {
                    throw new Error('Network response was not ok.');
                }
                const response2 = await response.json();
                console.log('response2222...????', response2);
                this.content = response2.data;
            } catch (error) {
                this.error = 'Failed to load data';
            } finally {
                this.loading = false;
            }
        },
        getClassByUserId(busUserId) {
            const classMap = {
                '5017266': 'col4 top1',
                '5017268': 'col4 top2',
                '5017269': 'col4 top3',
                '5017272': 'col4 top4',
                '5017273': 'col4 top5',
                '5017271': 'col4 top6',
                '5017305': 'col4 top7',
                // Add more mappings as needed
            };
            return classMap[busUserId] || 'col4 default-class'; // Provide a default class if needed
        },
    }
}

</script>

<style scoped>
.top1 {
    background-image: url('../assets/images/picture_top1.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

.top2 {
    background-image: url('../assets/images/picture_top2.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

.top3 {
    background-image: url('../assets/images/picture_top3.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

.top4 {
    background-image: url('../assets/images/picture_top4.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

.top5 {
    background-image: url('../assets/images/picture_top5.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

.top6 {
    /* background-image: url('../assets/images/picture_star_top1.png'); */
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background: linear-gradient(0deg, rgba(255, 237, 201, .7019607843137254), rgba(253, 242, 231, .7019607843137254));
}

.top7 {
    /* background-image: url('../assets/images/picture_star_top1.png'); */
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background: linear-gradient(0deg, rgba(255, 237, 201, .7019607843137254), rgba(253, 242, 231, .7019607843137254));
}

.col4 {
    display: grid;
    grid-template-columns: 8% 46% 15% 24%;
    width: 90vw;
    margin: 0 auto;
    font-size: 3.73vw;
    font-family: Roboto-Regular;
    font-weight: 400;
    color: #8d211a;
    column-gap: 2%;
    /* padding: 2.13vw; */
    margin-bottom: 2.8vw;
    align-items: center;
    /* background: linear-gradient(0deg, rgba(255, 237, 201, .7019607843137254), rgba(253, 242, 231, .7019607843137254)); */
    border-radius: 2.13vw;
}

rank-top3 {
    width: 7.46vw;
    height: 6.13vw;
}

.user-profile {
    text-align: center;
    font-weight: 500;
    display: flex;
    align-items: center;
    color: #8d211a;
    font-family: Roboto-Regular;

    span {
        text-overflow: ellipsis;
        white-space: nowrap;
        width: 2.7rem;
        overflow: hidden;
        text-align: left;
        margin-left: .08rem;
        color: #8d211a;
    }
}

.user-profile-img {
    height: 10.66vw;
    width: 10.66vw;
    border-radius: 50%;
    margin-right: 1.5vw;
}

.left-align {
    align-items: start;
}

.center-align,
.left-align {
    display: flex;
    justify-content: flex-start;
    color: #8d211a;
    font-family: Roboto-Regular;
}

.center-align {
    align-items: center;
    width: 1.46667rem;
    margin-left: auto;
}

.User{
    margin-left: 1rem;
}
</style>