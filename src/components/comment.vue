<template>
  <div class="comment">
    <span><b>作者</b>：{{ comment['作者'] }}</span>
    <span><b>研究方向</b>：{{ comment['研究方向'] }}</span>
    <span><b>投稿周期</b>：{{ comment['投稿周期'] }}</span>
    <span><b>录用情况</b>：{{ comment['录用情况'] }}</span>
    <span><b>审稿费</b>：{{ comment['审稿费'] }}</span>
    <span><b>版面费</b>：{{ comment['版面费'] }}</span>
    <span><b>时间</b>：{{ comment['时间'] }}</span>
    <div v-html="comment['内容']"></div>
  </div>
</template>

<script>
  export default {
    name: 'comment',
    props: {
      comment: {}
    },
    data () {
      return {
//        comment: {
//          '内容': 'xxx',
//          '录用情况': ' 已投修改后录用',
//          '作者': 'aakas888',
//          '审稿费': ' 约200元/篇  ',
//          '研究方向': ' 信息科学    ',
//          '投稿周期': ' 约3个月  ',
//          '版面费': ' 约4600元/页  ',
//          '时间': '时间：2016-09-02 16:29'
//        }
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 .comment {
   margin-top: 20px;
   background: #cff6fc;
   padding: 10px;
 }
  .comment span {
    color: #777777;
  }
  .comment div {
    margin-top: 10px;
  }
</style>
