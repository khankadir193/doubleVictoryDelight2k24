<template>
    <div class="howtoplay">
        <div class="mask">
            <div class="content">
                <div class="title">
                    <div class="tx" v-if="language == 1">
                        <div class="icon"></div>
                        <div class="text">Rules</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" v-if="language == 2">
                        <div class="icon"></div>
                        <div class="text">قواعد</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" style="font-weight: bold" v-if="language == 3">
                        <div class="icon"></div>
                        <div class="text">नियम</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" style="font-weight: bold; font-size: 0.4rem" v-if="language == 4">
                        <div class="icon"></div>
                        <div class="text">নিয়ম</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" v-if="language == 5">
                        <div class="icon"></div>
                        <div class="text">Mga tuntunin</div>
                        <div class="icon"></div>
                    </div>
                </div>
                <!-- <div class="rule_text" v-if="language == 1"> -->
                <div class="rule_text" v-if="language == 1">
                    <div class="rTag" data-v-f914f79e="">The event is divided into three parts:</div>
                    <div class="text" data-v-f914f79e=""> 1. Introduction to the Rebate Card feature<br
                            data-v-f914f79e="">2. Daily &amp; Overall leaderboard<br data-v-f914f79e="">3. Rebate
                        card mission </div>
                    <div class="rTag">1. What is the Rebate Card?</div>
                    <div class="text"> Exclusively available for OyeTalk Royal Pattern users, the
                        Rebate Card is a premium in-game item. If you don't win a game <b data-v-f914f79e="">(by not
                            betting on the winning seat)</b>, using the Rebate Card guarantees a 5% bean rebate to
                        reduce your losses. </div>
                    <div class="rTag">2. Leaderboard</div>
                    <div class="text"><b data-v-f914f79e="">Daily Leaderboard:</b><br>
                        <ul>
                            <li>Users will be ranked based on the daily rebate beans during the
                                event period after using the Rebate Card.</li>
                            <li>Top 1 from the leaderboard will be rewarded.</li>
                        </ul><b>Overall Leaderboard:</b>
                        <ul>
                            <li>Users will be ranked based on the total rebate beans during the
                                event period after using the Rebate Card.</li>
                            <li>Top 5 from the leaderboard will be rewarded.</li>
                        </ul>
                    </div>
                    <div class="rTag">3. Rebate Card Mission:</div>
                    <div class="text">User can receive extra rewards by purchasing different
                        numbers of rebate cards during the event.</div>
                </div>

                <div class="rule_text" v-if="language == 2">
                    <div class="rTag">Ye event 3 parts mein divided hai</div>
                    <div class="text"> 1. Introduction to the Rebate Card feature<br>2. Daily &amp; Overall leaderboard
                        <br>3. Rebate
                        card mission
                    </div>
                    <div class="rTag">1. Rebate Card kya hai?</div>
                    <div class="text"> Rebate Card aik premium in-game item hai jo khas tor pe
                        OyeTalk Royal Pattern users ke liye available hai. Agar ap koi game nahi jeet'te hain <b
                            data-v-f914f79e="">(winning seat pe bet na laga ke)</b>, to Rebate card istemal karne pe
                        ap 5% beans rebate kar ke apne nuksan ko kam kar sakte hain. </div>
                    <div class="rTag">2. Leaderboard</div>
                    <div class="text"><b>Daily Leaderboard:</b><br>
                        <ul>
                            <li>Users ki ranking rebate card istemal karne ke bad event ke doran
                                rebate beans ke mutabiq ho gi.</li>
                            <li>Leaderboard pe se TOP 1 ko reward diye jaen ge.</li>
                        </ul><b>Overall Leaderboard:</b>
                        <ul>
                            <li>Users ki ranking rebate card istemal karne ke bad event ke doran
                                tamam rebate beans ke mutabiq ho gi.</li>
                            <li>Leaderboard pe se Top 5 ko rewards diye jaen ge.</li>
                        </ul>
                    </div>
                    <div class="rTag">3. Rebate Card Mission:</div>
                    <div class="text">User ko event ke doran muktalif numbers ke rebate cards
                        khareedne pe extra rewards diye jaen ge.</div>
                </div>

                <div class="rule_text" v-if="language == 3">
                    <div class="rTag" data-v-f914f79e="">आयोजन को तीन भागों में बांटा गया है:</div>
                    <div class="text" data-v-f914f79e=""> 1. रिबेट कार्ड सुविधा का परिचय<br data-v-f914f79e="">2.
                        दैनिक एवं समग्र लीडरबोर्ड<br data-v-f914f79e="">3. रिबेट कार्ड मिशन </div>
                    <div class="rTag" data-v-f914f79e="">1. रिबेट कार्ड क्या है?</div>
                    <div class="text" data-v-f914f79e=""> ओएटॉक रॉयल पैटर्न यूजर के लिए विशेष रूप से उपलब्ध, रिबेट
                        कार्ड एक प्रीमियम इन-गेम आइटम है। यदि आप कोई गेम नहीं जीतते हैं <b data-v-f914f79e="">(जीतने
                            वाली सीट पर दांव न लगाकर)</b>, तो रिबेट कार्ड का उपयोग करने से आपके नुकसान को कम करने के
                        लिए 5% सेम छूट की गारंटी मिलती है। </div>
                    <div class="rTag" data-v-f914f79e="">2. लीडरबोर्ड</div>
                    <div class="text" data-v-f914f79e=""><b data-v-f914f79e="">दैनिक लीडरबोर्ड:</b><br
                            data-v-f914f79e="">
                        <ul data-v-f914f79e="">
                            <li data-v-f914f79e="">रिबेट कार्ड का उपयोग करने के बाद इवेंट अवधि के दौरान दैनिक छूट
                                बीन्स के आधार पर यूजर को रैंक किया जाएगा।</li>
                            <li data-v-f914f79e="">लीडरबोर्ड से शीर्ष 1 को पुरस्कृत किया जाएगा।</li>
                        </ul><b data-v-f914f79e="">समग्र लीडरबोर्ड:</b>
                        <ul data-v-f914f79e="">
                            <li data-v-f914f79e="">रिबेट कार्ड का उपयोग करने के बाद इवेंट अवधि के दौरान कुल छूट
                                बीन्स के आधार पर यूजर को रैंक किया जाएगा।</li>
                            <li data-v-f914f79e="">लीडरबोर्ड से शीर्ष 5 को पुरस्कृत किया जाएगा।</li>
                        </ul>
                    </div>
                    <div class="rTag" data-v-f914f79e="">3. रिबेट कार्ड मिशन:</div>
                    <div class="text" data-v-f914f79e="">इवेंट के दौरान यूजर अलग-अलग संख्या में छूट कार्ड खरीदकर
                        अतिरिक्त पुरस्कार प्राप्त कर सकते हैं।</div>
                </div>

                <div class="rule_text" v-if="language == 4">
                    <div class="rTag" data-v-f914f79e="">অনুষ্ঠানটি তিনটি ভাগে বিভক্ত:</div>
                    <div class="text" data-v-f914f79e=""> 1. রিবেট কার্ড বৈশিষ্ট্যের পরিচিতি<br data-v-f914f79e="">2.
                        দৈনিক এবং সামগ্রিক লিডারবোর্ড<br data-v-f914f79e="">3. রিবেট কার্ড মিশন </div>
                    <div class="rTag" data-v-f914f79e="">1. রিবেট কার্ড কি?</div>
                    <div class="text" data-v-f914f79e=""> OyeTalk রয়্যাল প্যাটার্ন ব্যবহারকারীদের জন্য একচেটিয়াভাবে
                        উপলব্ধ, রিবেট কার্ডটি একটি প্রিমিয়াম ইন-গেম আইটেম। যদি আপনি একটি খেলা না জিতেন <b
                            data-v-f914f79e="">(বিজয়ী আসনে বাজি না রেখে)</b>, রিবেট কার্ড ব্যবহার করে আপনার ক্ষতি কমাতে
                        5% শিম ছাড়ের নিশ্চয়তা দেয়। </div>
                    <div class="rTag" data-v-f914f79e="">2. লিডারবোর্ড</div>
                    <div class="text" data-v-f914f79e=""><b data-v-f914f79e="">দৈনিক লিডারবোর্ড:</b><br
                            data-v-f914f79e="">
                        <ul data-v-f914f79e="">
                            <li data-v-f914f79e="">ব্যবহারকারীদের দৈনিক রিবেট বিন্স উপর ভিত্তি করে র্যাঙ্ক করা হবেরিবেট
                                কার্ড ব্যবহার করার পরে ইভেন্টের সময়কালে।</li>
                            <li data-v-f914f79e="">লিডারবোর্ড থেকে শীর্ষ 1 পুরস্কৃত করা হবে.</li>
                        </ul><b data-v-f914f79e="">সামগ্রিক লিডারবোর্ড:</b>
                        <ul data-v-f914f79e="">
                            <li data-v-f914f79e="">ব্যবহারকারীদের মোট রিবেট বিন্স উপর ভিত্তি করে র্যাঙ্ক করা হবেরিবেট
                                কার্ড ব্যবহার করার পরে ইভেন্টের সময়কালে।</li>
                            <li data-v-f914f79e="">লিডারবোর্ড থেকে সেরা 5 জনকে পুরস্কৃত করা হবে।</li>
                        </ul>
                    </div>
                    <div class="rTag" data-v-f914f79e="">3. রিবেট কার্ড মিশন:</div>
                    <div class="text" data-v-f914f79e="">ব্যবহারকারী বিভিন্ন ক্রয় করে অতিরিক্ত পুরষ্কার পেতে
                        পারেনসংখ্যা ইভেন্ট চলাকালীন রিবেট কার্ডের।</div>
                </div>

                <div class="rule_text" v-if="language === 5">
                    <div class="rTag" data-v-f914f79e="">Ang kaganapan ay nahahati sa tatlong bahagi:</div>
                    <div class="text" data-v-f914f79e=""> 1. Panimula sa tampok na Rebate Card<br data-v-f914f79e="">2.
                        Pang-araw-araw at Pangkalahatang leaderboard<br data-v-f914f79e="">3. Misyon ng rebate card
                    </div>
                    <div class="rTag" data-v-f914f79e="">1. Ano ang Rebate Card?</div>
                    <div class="text" data-v-f914f79e=""> Eksklusibong available para sa mga user ng OyeTalk Royal
                        Pattern, ang Rebate Card ay isang premium na in-game item. Kung hindi ka nanalo sa isang laro <b
                            data-v-f914f79e="">(sa pamamagitan ng hindi pagtaya sa panalong upuan)</b>, ang paggamit ng
                        Rebate Card ay ginagarantiyahan ang isang 5% bean rebate upang mabawasan ang iyong mga
                        pagkatalo. </div>
                    <div class="rTag" data-v-f914f79e="">2. Leaderboard</div>
                    <div class="text" data-v-f914f79e=""><b data-v-f914f79e="">Pang-araw-araw na Leaderboard:</b><br
                            data-v-f914f79e="">
                        <ul data-v-f914f79e="">
                            <li data-v-f914f79e="">Ira-rank ang mga user batay sa araw-araw na rebate beans sa panahon
                                ng event pagkatapos gamitin ang Rebate Card.</li>
                            <li data-v-f914f79e="">Ang nangungunang 1 mula sa leaderboard ay gagantimpalaan.</li>
                        </ul><b data-v-f914f79e="">Pangkalahatang Leaderboard:</b>
                        <ul data-v-f914f79e="">
                            <li data-v-f914f79e="">Iraranggo ang mga user batay sa kabuuang rebate beans sa panahon ng
                                event pagkatapos gamitin ang Rebate Card.</li>
                            <li data-v-f914f79e="">Ang nangungunang 5 mula sa leaderboard ay gagantimpalaan.</li>
                        </ul>
                    </div>
                    <div class="rTag" data-v-f914f79e="">3. Misyon ng Rebate Card:</div>
                    <div class="text" data-v-f914f79e="">Maaaring makatanggap ang user ng mga karagdagang reward sa
                        pamamagitan ng pagbili ng iba't ibang bilang ng mga rebate card sa panahon ng kaganapan.</div>
                </div>
                <div class="closeBtn" @click="closeMask">
                    <img src="../assets/images/close.png" alt="" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { ref, onMounted } from "vue";
export default {
    name: 'howToPlay',
    props: ["language"],
    setup(props, { emit }) {
        let _scrollTop = ref(0);
        function closeMask() {
            document.body.style.position = "";
            document.body.style.top = "";
            document.scrollingElement.scrollTop = _scrollTop.value;
            emit("closeMe");
        }
        onMounted(() => {
            _scrollTop.value = document.scrollingElement.scrollTop;
            document.body.style.position = "fixed";
            document.body.style.top = -_scrollTop.value + "px";
        });
        function nouse() { }
        return { closeMask, nouse };
    },
};
</script>

<style lang="less" scoped>
.paragraph_6 {
    width: 93%;
    // height: 416px;
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Regular;
    font-weight: normal;
    text-align: left;
    //   line-height: 15px;
    margin: 0 auto;

}

.text_1 {
    width: 256px;
    height: 26px;
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: left;
    white-space: nowrap;
    line-height: 39px;
    //   margin: 31px 0 0 39px;
}

.text-wrapper_1 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .paragraph_1 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.text_2 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: left;
    white-space: nowrap;
    line-height: 38px;
}

.text-wrapper_2 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .text_3 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }

    .paragraph_2 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 14px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.text_4 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: left;
    white-space: nowrap;
    line-height: 39px;
}

.text-wrapper_3 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .paragraph_3 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.text_5 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Bold;
    font-weight: 700;
    text-align: left;
    white-space: nowrap;
    line-height: 39px;
}


.text-wrapper_4 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .paragraph_4 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.paragraph_5 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 14px;
    font-family: Roboto-Regular;
    font-weight: normal;
    text-align: left;
}





// .rTag {
//     font-size: 12px;
//     font-weight: 500;
//     margin-top: 10px;
//     margin-bottom: -5px;
//     color: red;
//     font-family: "Roboto-Regular";
//     padding-left: 10px;
// }


//previous text design
.howtoplay {
    .dian_text {
        text-align: left;
        font-family: "Roboto-Regular";

        font-weight: 400;
        color: rgba(255, 255, 255, 0.6);
        line-height: 1.5;
        font-size: 11px;
        margin-top: 3px;
        position: relative;
    }

    .mask {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 9999;

        .text {
            font-size: 13px;
        }

        .content {
            font-family: "Roboto" !important;
            left: 50%;
            top: 50%;
            transform: translateX(-50%) translateY(-50%);
            position: relative;
            box-sizing: border-box;
            padding: 18px 15px 25px 8px;
            padding-right: 0;
            width: 300px;
            height: 400px;
            background: white;
            border: 1.5px solid #FFE898;
            border-radius: 15px;

            .title {
                width: 181px;
                height: 35px;
                position: absolute;
                text-align: center;
                display: flex;
                align-items: center;
                justify-content: center;
                left: 50%;
                top: 7px;
                transform: translateX(-50%) translateY(-55%);
                background: url("../assets/images/picture_title.png") no-repeat;
                background-size: 100% 100%;

                .tx {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    font-family: "BalooBhaina";


                    .text {
                        font-size: 15px;
                        color: #fff;
                        margin: 0 50px;
                        white-space: nowrap;
                        font-weight: 600;
                    }
                }
            }

            .rule_text {
                text-align: left;
                overflow: auto;
                height: 100%;
                padding-right: 16px;

                .topText {
                    text-align: left;
                    font-weight: 300;
                    line-height: 20px;
                    font-size: 13px;
                    margin-top: 10px;
                    font-family: "Roboto-Regular";
                    color: #fff;

                    .num {
                        display: inline-flex;
                        align-items: center;
                        justify-content: center;
                        width: 15px;
                        height: 15px;
                        background-color: rgba(0, 0, 0, 0.1);
                        border-radius: 50%;
                        color: #fff;
                    }
                }

                .text {
                    text-align: left;
                    // font-weight: lighter;
                    line-height: 20px;
                    font-size: 13px;
                    margin-top: 10px;
                    font-family: "Roboto-Regular";
                    color: red;
                    background-color: rgba(0, 0, 0, 0.1);

                    padding: 10px;
                    border-radius: 5px;
                }

                .tag {
                    border-radius: 5px;
                    display: inline-block;
                    // color: rgba(255, 255, 255, 0.6);
                    font-size: 11px;
                    margin-top: 10px;
                    color: #fff;
                }
            }

            .rTag {
                font-size: 12px;
                font-weight: 500;
                margin-top: 10px;
                margin-bottom: -5px;
                color: red;
                font-family: "Roboto-Regular";
                padding-left: 10px;
            }

            img {
                display: inline-block;
                margin: 20px 0 16px;
            }

            .noteText {
                .tag {
                    margin-top: 0;
                    font-family: "Roboto-Regular";
                }

                font-size: 11px !important;
                color: rgba(255, 255, 255, 0.6);
                padding: 10px;
                border-radius: 5px;
                padding-left: 0;
            }
        }

        .closeBtn {
            width: 28px;
            height: 28px;
            position: absolute;
            left: 50%;
            bottom: -25px;
            transform: translateX(-50%) translateY(0%);

            img {
                width: 100%;
                height: 100%;
            }
        }
    }
}
</style>