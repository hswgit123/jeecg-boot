<template>
  <div>
<!--    <div id="herder">页头</div>-->
    <div id="main">
      <div class="main-left">
        <a-card
          style="margin-top: 24px"
          :bordered="false"
          title="最新态势">
          <a-list size="large"  >
            <a-list-item :key="index" v-for="(item, index) in data">
              <a-list-item-meta :description="item.description">
                <a-avatar slot="avatar" size="large" shape="square" :src="item.avatar"/>
                <a slot="title">{{ item.title }}</a>
              </a-list-item-meta>
<!--              <div class="list-content">
                <div class="list-content-item">
                  <span>Owner</span>
                  <p>{{ item.owner }}</p>
                </div>
                <div class="list-content-item">
                  <span>开始时间</span>
                  <p>{{ item.startAt }}</p>
                </div>
              </div>-->
            </a-list-item>
          </a-list>
        </a-card>

        <a-card
          style="margin-top: 24px"
          :bordered="false"
          title="最新态势">
          <a-list size="large"  >
            <a-list-item :key="index" v-for="(item, index) in data">
              <a-list-item-meta :description="item.description">
                <a-avatar slot="avatar" size="large" shape="square" :src="item.avatar"/>
                <a slot="title">{{ item.title }}</a>
              </a-list-item-meta>
              <!--              <div class="list-content">
                              <div class="list-content-item">
                                <span>Owner</span>
                                <p>{{ item.owner }}</p>
                              </div>
                              <div class="list-content-item">
                                <span>开始时间</span>
                                <p>{{ item.startAt }}</p>
                              </div>
                            </div>-->
            </a-list-item>
          </a-list>
        </a-card>

      </div>
      <div class="main-center">中间</div>
      <div class="main-right">右列</div>
    </div>
    <div id="footer">页脚</div>

  </div>
</template>

<script>
  import HeadInfo from '@/components/tools/HeadInfo'

  const data = []
  data.push({
    title: 'Alipay',
    avatar: 'https://gw.alipayobjects.com/zos/rmsportal/WdGqmHpayyMjiEhcKoVE.png',
    description: '那是一种内在的东西， 他们到达不了，也无法触及的',
    owner: '付晓晓',
    startAt: '2018-07-26 22:44',
    progress: {
      value: 90
    }
  })
  data.push({
    title: 'Angular',
    avatar: 'https://gw.alipayobjects.com/zos/rmsportal/zOsKZmFRdUtvpqCImOVY.png',
    description: '希望是一个好东西，也许是最好的，好东西是不会消亡的',
    owner: '曲丽丽',
    startAt: '2018-07-26 22:44',
    progress: {
      value: 54
    }
  })
  data.push({
    title: 'Ant Design',
    avatar: 'https://gw.alipayobjects.com/zos/rmsportal/dURIMkkrRFpPgTuzkwnB.png',
    description: '生命就像一盒巧克力，结果往往出人意料',
    owner: '林东东',
    startAt: '2018-07-26 22:44',
    progress: {
      value: 66
    }
  })
  data.push({
    title: 'Ant Design Pro',
    avatar: 'https://gw.alipayobjects.com/zos/rmsportal/sfjbOqnsXXJgNCjCzDBL.png',
    description: '城镇中有那么多的酒馆，她却偏偏走进了我的酒馆',
    owner: '周星星',
    startAt: '2018-07-26 22:44',
    progress: {
      value: 30
    }
  })
  data.push({
    title: 'Bootstrap',
    avatar: 'https://gw.alipayobjects.com/zos/rmsportal/siCrBXXhmvTQGWPNLBow.png',
    description: '那时候我只会想自己想要什么，从不想自己拥有什么',
    owner: '吴加好',
    startAt: '2018-07-26 22:44',
    progress: {
      status: 'exception',
      value: 100
    }
  })

  export default {
    name: "StandardList",
    components: {
      HeadInfo
    },
    data () {
      return {
        data
      }
    }
  }
</script>

<style scoped>
  *{margin:0;padding:0;}
  #herder{
    height:50px;
    background:#ffffff;
  }
  #main{
    width:100%;
    overflow:hidden;
    background:#ffffff;
  }
  #main .main-left{
    width:30%;
    height:100%;
    float:left;
    background:#ffffff;
    border:1px solid #cccccc;
  }
  #main .main-center{
    width:40%;
    height:100%;
    background:#ffffff;
    float:left;
    border:1px solid #cccccc;
  }
  #main .main-right{
    width:30%;
    height:100%;
    background:#ffffff;
    float:right;
    border:1px solid #cccccc;
  }
  #footer{
    height:50px;
    background:#ffffff;
  }
  .ant-avatar-lg {
    width: 48px;
    height: 48px;
    line-height: 48px;
  }

  .list-content-item {
    color: rgba(0, 0, 0, .45);
    display: inline-block;
    vertical-align: middle;
    font-size: 14px;
  }
  span {
    line-height: 20px;
  }
  p {
    margin-top: 4px;
    margin-bottom: 0;
    line-height: 22px;
  }
</style>