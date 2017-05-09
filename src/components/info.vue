<template>
  <div class="info">
    <div>
      <div class="baseInfo">
        <div class="baseInfo1"><b>期刊名</b>：{{ journal['期刊名'] }}</div>
        <div class="baseInfo1"><b>出版地</b>：{{ journal['出版地'] }}</div>
        <div class="baseInfo1"><b>主办单位</b>：{{ journal['主办单位'] }}</div>
        <div class="baseInfo1"><b>复合影响因子</b>：{{ journal['复合影响因子'] }}</div>
        <div class="baseInfo1"><b>综合影响因子</b>：{{ journal['综合影响因子'] }}</div>
        <div class="baseInfo1"><b>审稿费用</b>：{{ journal['审稿费用'] }}</div>
        <div class="baseInfo1"><b>版面费用</b>：{{ journal['版面费用'] }}</div>
        <div class="baseInfo2"><b>数据库收录/荣誉</b>：{{ journal['数据库收录/荣誉'] }}</div>
        <div class="baseInfo2"><b>偏重的研究方向</b>：{{ journal['偏重的研究方向'] }}</div>
        <div class="baseInfo2"><b>投稿录用比例</b>：{{ journal['投稿录用比例'] }}</div>
        <div class="baseInfo2"><b>审稿速度</b>：{{ journal['审稿速度'] }} </div>
      </div>
    </div>
    <comment v-for="comment in journal['所有评论']" v-bind:comment="comment"></comment>
  </div>
</template>

<script>
  import Comment from '../components/comment.vue'
  export default {
    name: 'info',
    props: {
      journal: {}
    },
    data () {
      return {
//        journal: {
//          '审稿速度': '平均 12.6154 个月的审稿周期',
//          '复合影响因子': '2.77',
//          '审稿费用': '平均 196 元/篇',
//          '出版地': '北京市',
//          '投稿录用比例': '85%',
//          '版面费用': '平均 1100 元/页',
//          '综合影响因子': '1.456',
//          '所有评论': [
//            {
//              '内容': 'xxx',
//              '录用情况': ' 已投修改后录用',
//              '作者': 'aakas888',
//              '审稿费': ' 约200元/篇  ',
//              '研究方向': ' 信息科学    ',
//              '投稿周期': ' 约3个月  ',
//              '版面费': ' 约4600元/页  ',
//              '时间': '时间：2016-09-02 16:29'
//            },
//            {
//              '内容': 'yyy',
//              '录用情况': ' 已投修改后录用',
//              '作者': 'haha',
//              '审稿费': ' 约200元/篇  ',
//              '研究方向': ' 信息科学    ',
//              '投稿周期': ' 约3个月  ',
//              '版面费': ' 约4600元/页  ',
//              '时间': '时间：2016-09-02 16:29'
//            },
//            {
//              '内容': 'zzz',
//              '录用情况': ' 已投修改后录用',
//              '作者': 'heihei',
//              '审稿费': ' 约200元/篇  ',
//              '研究方向': ' 信息科学    ',
//              '投稿周期': ' 约3个月  ',
//              '版面费': ' 约4600元/页  ',
//              '时间': '时间：2016-09-02 16:29'
//            },
//            {
//              '内容': 'jj',
//              '录用情况': ' 已投修改后录用',
//              '作者': 'zuozuo',
//              '审稿费': ' 约200元/篇  ',
//              '研究方向': ' 信息科学    ',
//              '投稿周期': ' 约3个月  ',
//              '版面费': ' 约4600元/页  ',
//              '时间': '时间：2016-09-02 16:29'
//            }
//          ],
//          '期刊名': '计算机学报',
//          '数据库收录/荣誉': [
//            'CSCD 核心期刊',
//            '中科双效期刊',
//            '百种重点期刊',
//            '中国科学引文数据库',
//            'EI 工程索引',
//            'CBST 科学技术文献速报',
//            'SA 科学文摘'
//          ],
//          '偏重的研究方向': [
//            '信息科学(24)',
//            '计算机科学(22)',
//            '计算机应用技术(6)',
//            '计算机科学的基础理论(5)',
//            '计算机网络(3)',
//            '计算机体系结构(2)',
//            '信息安全(2)',
//            '自然语言理解与机器翻译(1)',
//            '信息处理方法与技术(1)',
//            '电子学与信息系统(1)',
//            '计算机软件(1)'
//          ],
//          '主办单位': '中国计算机学会;中国科学院计算技术研究所'
//        }
      }
    },
    components: {
      'comment': Comment
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .info {
    font-family: "Microsoft YaHei UI";
    font-size: 18px;
    padding: 5px;
    margin-top: 20px;
  }
  .baseInfo {
    color: #666666;
    background: #f6f6f6;
    padding: 10px;
  }
  .baseInfo1 {
    float: left;
    margin-right: 10px;
    margin-bottom: 5px;
  }
  .baseInfo2 {
    clear: both;
    margin-top: 5px;
  }
</style>
