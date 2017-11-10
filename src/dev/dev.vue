<template>
  <aside class="dev">
    <div class="item">
      <vueDropdown className="down">
        <div slot="title">测试</div>
        <div slot="text">
          <ul>
            <li>导航一</li>
            <li>导航二</li>
            <li>导航三</li>
            <li>导航四</li>
            <li>导航五</li>
          </ul>
        </div>
      </vueDropdown>
    </div>

  </aside>
</template>
<script>
  import vueDropdown from '../components/vue-dropdown.vue'

  export default {
    data() {
      return {};
    },
    methods: {},
    components: {vueDropdown}
  };
</script>
<style rel="stylesheet/scss" lang="scss">
  .dev {
    .item {
      float: left;
      margin-right: 20px;
      .down {
        margin: 100px 300px;
        ul{
          li{
            width: 100px;
            height:44px;
            line-height:44px;
            cursor: pointer;
            &:hover{
              color: #308697;
            }
          }
        }
      }

    }
  }


</style>

