<template>
    <div class="box">
        <p class="">　　窗外寒意袭人，尊耀汇使您暖意浓浓，在这岁末年终的特别时刻，为了感谢客户对尊耀汇一如既往的支持和厚爱，我们在春节到来之际开展“感恩相伴，新春回馈”活动倾情答谢客户。我们以最诚挚的心声与您相邀开启一场激情的财富之旅。</p>
        <ul>
            <li>
                <p>活动对象：</p>
                <p>所有活动期间认购产品的客户</p>
            </li>
            <li>
                <p>活动时间：</p>
                <p>2018年2月1日-2018年3月31日</p>
            </li>
            <li>
                <p>活动规则：</p>
                <p>　　   活动期间根据认购金额排行榜，取前88名发放现金及商城积分奖励。若认购金额相同，按照认购时间先后顺序排名。</p>
            </li>
        </ul>
        <p class="info">　　我们是商海中彼此信任的朋友，我们是经济浪潮下并肩作战的战友，我们曾一起为我们的梦想努力，我们也将一起迎接最美的朝阳。感谢您对尊耀汇的继续关注和支持，春节将至，尊耀汇全体员工祝您：财运旺旺，尊享一生！</p>
        <p class="center">本次活动的最终解释权归公司所有。</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            }
        },
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
    ul {
        padding-top: 30px;
        margin-bottom: 30px;
    }
    ul li{
        padding-left: 60px;
    }
    ul li:nth-child(1){
        background: url("../assets/images/obj.png") no-repeat top left;
    }
    ul li:nth-child(2){
        background: url("../assets/images/date.png") no-repeat top left;
    }
    ul li:nth-child(3){
        background: url("../assets/images/rule.png") no-repeat top left;
    }
    .info{
        margin:30px;
    }
    .center{
        text-align: center;
    }
</style>