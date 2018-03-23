<template>
    <div class="box">
        <p>本次活动分为现金奖励和积分奖励，其中：</p>
        <ul>
            <li class="money">
                <div>现金奖励</div>
                <p>
                    第一名: <span>8888现金；</span><br>
                    第一名: <span>6666现金；</span><br>
                    第一名: <span>55555现金；</span>
                </p>
            </li>
            <li class="coin">
                <div>积分奖励：</div>
                <p>从第4名开始计算，4-88名的认购排名客户均获赠积分奖励。我们将准备出<span>5888</span>积分构成奖励积分池，入围的85位VIP将按照自己认购的金额获赠相应额度的积分，积分可以直接兑换尊耀汇网站商城的礼品，也可以保留到下次使用。</p>
            </li>
            <p>积分奖励算法：个人奖励积分=奖励回馈总额/入围客户认购的流水总额×个人认购金额。</p>
        </ul>
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
        line-height: 36px;
        font-family: "Segoe UI","Lucida Grande",Helvetica,Arial,"Microsoft YaHei",FreeSans,Arimo,"Droid Sans","wenquanyi micro hei","Hiragino Sans GB","Hiragino Sans GB W3",FontAwesome,sans-serif;
        color: #ffb4b5;
        font-weight: 400;
    }
    ul li{
        margin-bottom: 30px;
    }
    ul li div{
        padding-left: 60px;
    }
    ul .money div{
        background:  url("../assets/images/cash.png") no-repeat top left;
    }
    ul .coin div{
        background:  url("../assets/images/coin.png") no-repeat top left;
    }
</style>