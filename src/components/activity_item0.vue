<template>
    <div class="box">
        <ul>
            <li class="header">
                <div v-for="title in titles">{{title}}</div>
            </li>
            <li v-for="(item,index) in arr">
                <div v-if="index =='0'">
                    <img src="../assets/images/first_cup.png" alt="">
                </div>
                <div v-else-if="index == '1'">
                    <img src="../assets/images/second_cup.png" alt="">
                </div>
                <div v-else-if="index == '2'">
                    <img src="../assets/images/third_cup.png" alt="">
                </div>
                <div v-else>
                    {{index+1}}
                </div>
                
                <div>{{item.n}}</div>
                <div>{{item.a}}</div>
                <div v-if="index == '0'">
                    8888元
                </div>
                <div v-else-if="index == '1'">
                    6666元
                </div>
                <div v-else-if="index == '2'">
                    5555元
                </div>
                <div v-else-if="2<index&&index <88">
                    {{item.i}}积分
                </div>
                <div v-else>
                    未上榜
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                titles:["活动排名","客户账号","认购金额","活动奖励"],
                arr:[]
            }
        },
        created() {
            $.getJSON("https://data.zunyaohui.com/?cb=?",{
                act:"201802",
                cls:"activity"
            }).then( res => {
                this.arr = res.rows
            })
        }
    }
</script>

<style scoped>
     .box{
        padding:20px;
        background-color:rgba(127,10,13,0.6);
        font-size: 16px;
        line-height: 28px;
        font-family: "Segoe UI","Lucida Grande",Helvetica,Arial,"Microsoft YaHei",FreeSans,Arimo,"Droid Sans","wenquanyi micro hei","Hiragino Sans GB","Hiragino Sans GB W3",FontAwesome,sans-serif;
        color: #ffb4b5;
        font-weight: 400;
    }
    ul li{
        display: flex;
        justify-content: space-between;
        box-sizing: border-box;
        margin-bottom: 10px;
    }
    ul li div{
        width: 25%;
        text-align: center;
    }
    ul .header div{
        background: url(../assets/images/money.png) no-repeat center center;
        background-origin:content-box;
    }
</style>