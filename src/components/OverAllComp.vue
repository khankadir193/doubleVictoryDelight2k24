<template>
    <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description="leaderDescription"/>
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
            data:null,
            loading:true,
            error:null
        }
    },
    mounted(){
        this.fetchData();
    },
    methods:{
        async fetchData(){
            try{
                const response = await fetch('http://voice-cluster-314173693.cn-northwest-1.elb.amazonaws.com.cn:8090/oyetalk-marketing/activity/ranking?activityCode=rebate_20240611&rankingRuleId=1297&size=10');
                console.log('response..',response);
                if(!(await response).ok){
                    throw new Error('Network response was not ok.');
                }
                const data = (await response).json();
                this.data = data;
            }catch(error){
                this.error = 'Failed to load data';
            }finally {
                this.loading = false;
            }
        }
    }
}

</script>

<style scoped>
h1 {
    color: black;
}
</style>