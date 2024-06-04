<template>
    <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description="leaderDescription" />
    <div class="col4 top1" v-for="user in content" :key="user.id">
        <div class="rank-top3">
        </div>
        <div class="user-profile">
            <button class="profile-Imgbg">
                <!-- <img src="https://d1zkuggdb17jjb.cloudfront.net/avatar/2023-08-21/6435b677-b947-4a39-95a0-ae05bb8b3e0f.jpeg"
                    alt="" class="user-profile-img"> -->
                    {{ user.userName }}
            </button>
            <span class="user-name">Mαήnατ.�</span>
        </div>
        <div class="left-align">
            <!-- <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAWCAMAAAD3n0w0AAAChVBMVEUAAADzrCnfSwPygBzZoA/0rBzfUQP47bH9ngT5qBH6zAz37a353l36kwP5sBf2jQj6yyP8qg3pbwj0ngzugwbskgP0gAXqfwT6zwby8JbvkQfy5XLorRb3txvyigzy8JjlrxX1hgfkVQj6xybqmBLnYgr7thfnxTH50QbzoAjx6oD02En10Sbueg7pZhLzlhbxuyTyjBjdlSDtngr5wiTx3kr3zgHyyQv/////55P/4oL/23P/mhL/nAv/nwT/8sX/5I//lRf/nxb/jRP/lxD/oQ//kA//mQj9hQbsegDncgDrbwDXZwDdZgDlYgDdWwDMNgD5/P/3+P/7+vX//fP/++r/+Nn/77L/7Kr/76j/6pz/4pL/2H//1WT+3GL/11f/z0//vk7/yUz/tTD/qCb/nSD9qxr/mRr/nBb/wxX/mxL/rQ3/mg31hQ3+kgj/sgfpcwH7kwD4kADwiQDvggDidADXbQDaaADgZADiYgDcYgDhWQDMVADRTgDVTQDZSwDSPgD8///8/vv38uj/+uX/9OH/98/588zz6Mj/8b3/8LT96rT/8a/2467/7Kb/7KT/6aP97Jf/6Jfw0Iv/2or/6Ib/33//5Hv/3Hn51Xn/1Xbyy3b/znD/1m7/027842z/3mv/yWv/0mP/yWH/xWH/xFj/yVX+3E//uET7xEH/vz/ztz//tjz3tzf/rzD/wy30qi3/qiX/syH+myD/rx/zqh//tx7/tRzymhzzoBf6kxf5ixb+uhP/yA7/kw32fgz4nAr/qQf3lAf+lgL/twD/nQD+kgD/igDwhgDnggDkfgDddgDhbgDnbQDjZgDaYADQXwDhWwDhVgDUVgDgUgDJTwDYQADEZIu5AAAAOHRSTlMACb06Kxr6+O7o5OPh4eDg3NfU09HPzcfFwLm4t7Wxq6urqKakoJ+Nh399cG1raWNiYVtDQTIyBdbwFFEAAAGISURBVBjTYoADEzVBDl45QwYkwKi8Jz/brrDES4gZLsYqkHkk/6Bd4QlPv0swUUauvZnRU7KPFhV7el9hY4QISiyPS7Bo3b7pkKe3X/U1PbCYxkSLSfFzk7Ylby7wq65vUAKJmc236FpgnZCUnJGaW3mxPoAJJMgTEjndyjp2WYpNuvM5/zqwoE5TyFRLK+tFiSk2jm5ngYKqDAzm7BY9UUDBxSucbFzyvKpqG3QZGLQbQyP7La3mLVlna5OT5+Vb688KGAMDt0VbeJ/ltDmJrrY5dkWl5ZfFGRhMgy3COiMsYxZutM1ytys+7XPGmIFBK9CixT7CIWaNbZaL++FTZeWiQLvlAy1C7SdEL3XNcNnnXlLmc5IFKCgZZBEWHjUrzSndzc3D50KpJsjl0kHB9g4Oq1xTHZ09fGt8pcD+Vm9v7p4Ru8UJKFZx9bwIJIBY4jp6Z65M27V7f2VNlRgjNCwV4ifPXr11R653RYEiIiZk1q/dsPPAseP8+sjxYyDLxymsYoQQAADdj329WC5UbAAAAABJRU5ErkJggg=="
                alt="" class="beans"> -->
            second data
            <span class="beans-amount">1M</span>
        </div>
        <div class="center-align">
            <!-- <img alt="" class="beans reward-img"
                data-src="https://sem-activity.s3.cn-northwest-1.amazonaws.com.cn/yB0q5DlgzySOCc6sOGR8q.png"
                src="https://sem-activity.s3.cn-northwest-1.amazonaws.com.cn/yB0q5DlgzySOCc6sOGR8q.png" lazy="loaded"> -->
            22K
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
        }
    }
}

</script>

<style scoped>
.top1 {
    background-image: url('../assets/images/picture_top1.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
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
    padding: 2.13vw;
    margin-bottom: 2.8vw;
    align-items: center;
    background: linear-gradient(0deg, rgba(255, 237, 201, .7019607843137254), rgba(253, 242, 231, .7019607843137254));
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
</style>