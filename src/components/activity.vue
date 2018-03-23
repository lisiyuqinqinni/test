<template>
    <div>
        <div class="banner">
            <img src="../assets/images/banner.jpg" alt="">
        </div>
        <div class="main">
            <div class="main-left">
                <img src="../assets/images/lantern.png" alt="">
            </div>
            <div class="titles">
                <ul>
                    <li v-for="title,index in titles" :class="{ active: isActive==index }" @click="changActive(index)">{{title}}</li>
                </ul>
                <div class="content">
                    <div :is="isItem"></div>
                </div>
            </div>
            <div class="main-right">
                <img src="../assets/images/lantern.png" alt="">
            </div>
            
        </div>
        
    </div>
</template>

<script>
    import item0 from "./activity_item0"
    import item1 from "./activity_item1"
    import item2 from "./activity_item2"
    export default {
        components: {
            item0,
            item1,
            item2
        },
        data() {
            return {
                titles:["流水排行","活动介绍","活动奖励"],
                isActive: "0",
                isItem: "item0"
            }
        },
        methods: {
            changActive (index) {
                this.isActive = index
                this.isItem = "item" + index
            }
        }
    }
</script>

<style scoped>
    .banner img{
        width:100%;
        vertical-align:middle;
    }
    .main{
        display: flex;
        justify-content:space-between;
        background: url("../assets/images/spring_bg.png")
    }
    .titles{
        width: 820px;
    }
    .titles ul{
        display: flex;
        justify-content:space-between;
        width: 100%;
        height: 38px;
        margin-bottom: 20px;
    }
    .main-left{
        padding-left: 100px;
    }
    .main-right{
        padding-right: 100px;
    }
    .titles ul li{
        color: #860406;
        background-image: url("../assets/images/arrow_left_red.png"),url("../assets/images/arrow_right_red.png");
        background-repeat: no-repeat;
        background-position: left,right;
        line-height: 26px;
        padding: 6px 16px;
        width: 100px;
        cursor: pointer;
        text-align: center;
    }
    .titles ul li.active{
        background-image: url("../assets/images/arrow_left_yellow.png"),url("../assets/images/arrow_right_yellow.png");
        color:#FEF8A0;
    }
    .titles ul li:hover{
        color:#FEF8A0;
    }
    .content {
        background-image: url("../assets/images/corner_yellow_lt.png"),url("../assets/images/corner_yellow_rt.png"),url("../assets/images/corner_yellow_lb.png"),url("../assets/images/corner_yellow_rb.png");
        background-repeat: no-repeat;
        background-position: left top,right top,left bottom,right bottom;
        padding:20px 29px 23px 30px;
    }
    @media screen and (max-width: 1000px){
        .main-left{
            display: none;
        }
        .main-right{
            display: none;
        }
        .content{
            box-sizing: border-box;
            width: 100%;
        }
        .titles{
            width: 100%;
        }
    }
    @media screen and (max-width: 627px){
        .content{
            padding: 0;
            background: none;
        }
    }
</style>