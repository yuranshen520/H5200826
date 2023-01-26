<template>
    <div>
        <el-row :gutter="10">
          <!-- 之后用v-for进行遍历 -->
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple-light"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple-light"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple-light"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple-light"><vote_content></vote_content></div></el-col>
          <el-col :xs="24" :sm="12" :lg="8"><div class="grid-content bg-purple"><vote_content></vote_content></div></el-col>
        </el-row>
        
    </div>
</template>

<script>
import vote_content from './vote_content'
export default {
    name: 'Vote_content',
    data() {
        return {
            property: 'value',
        };
    },
    components:{vote_content}
}
</script>

<style lang="scss" scoped>>
  .el-row {
    margin-bottom: 20px;
    height: 500px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 330px;
    margin-bottom: 10px;
    overflow: hidden;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>