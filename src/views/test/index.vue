<template>
  <div class="app-container m-t-100">
    <el-upload
      class="upload-demo"
      action
      :on-change="handleChange"
      :on-exceed="handleExceed"
      :on-remove="handleRemove"
      :file-list="fileListUpload"
      :limit="limitUpload"
      accept="application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/vnd.ms-excel"
      :auto-upload="false"
    >
      <el-button size="small" type="primary">点击上传</el-button>
      <div slot="tip" class="el-upload__tip">只 能 上 传 xlsx / xls 文 件</div>
    </el-upload>
  </div>
</template>

<script>
export default {
  name: 'Test',
  data() {
    return {}
  },
  methods: {
    handleChange(file, fileList) {
      this.fileTemp = file.raw
    },
    handleRemove(file, fileList) {
      this.fileTemp = null
    }
  }
}
</script>

<style scoped>
.field-label {
  vertical-align: middle;
}
.box-card {
  width: 400px;
  max-width: 100%;
  margin: 20px auto;
}

.block {
  padding: 30px 24px;
}

.tag-item {
  margin-right: 15px;
}
.m-t-100 {
  margin-top: 100px;
}
</style>
