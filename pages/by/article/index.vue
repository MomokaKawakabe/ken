<template>
  <div class="page-article">
    <div class="article-title-bar">
      写文章
    </div>
    <div class="article-form-content">
      <div class="form-item">
        <div class="form-label">
          标题
        </div>
        <div class="form-input">
          <el-input placeholder="标题" size="medium" />
        </div>
      </div>
      <div class="form-item">
        <div class="form-label">
          分类
        </div>
        <div class="form-input">
          <el-input size="medium" />
        </div>
      </div>
      <div class="form-item">
        <div class="form-label">
          标签
        </div>
        <div class="form-input">
          <el-input size="medium" />
        </div>
      </div>
      <div class="form-item form-item-abstract">
        <div class="form-label">
          摘要
        </div>
        <div class="form-input">
          <el-input type="textarea" :autosize="{ minRows: 2, maxRows: 4}" placeholder="摘要" size="medium" />
        </div>
      </div>
      <div class="form-title">
        正文
      </div>
      <mavon-editor
        v-model="value"
        :subfield="false"
        box-shadow-style="0 0 2px 1px rgba(0, 0, 0, 0.3)"
        :toolbars="toolbars"
        font-size="16px"
      />
    </div>
    <div class="article-submit">
      <div class="default-button">
        提交并发布
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'ByArticle',
  transition: 'fade',
  data () {
    return {
      toolbars: {
        bold: true, // 粗体
        italic: true, // 斜体
        underline: true, // 下划线
        strikethrough: true, // 中划线
        superscript: true, // 上角标
        subscript: true, // 下角标
        link: true, // 链接
        imagelink: true, // 图片链接
        code: true, // code
        help: true, // 帮助
        /* 2.1.8 */
        alignleft: true, // 左对齐
        aligncenter: true, // 居中
        alignright: true, // 右对齐
        /* 2.2.1 */
        preview: true // 预览
      }
    }
  }
})
</script>

<style lang="less">
@import "assets/css/color";
.page-article {
  color: @f_main;
  .article-title-bar {
    padding: 20px;
    font-size: 22px;
    color: @f_main;
    border-bottom: 2px solid;
    border-image: @b_theme_line_b 1;
  }
  .article-form-content {
    padding: 60px 60px 40px 60px;
    .form-item {
      display: flex;
      align-items: center;
      margin-bottom: 26px;
      font-size: 14px;
      .form-label {
        width: 120px;
        font-weight: 600;
      }
      .form-input {
        width: 100%;
      }
    }
    .form-item-abstract {
      align-items: flex-start;
    }
    .form-title {
      font-weight: 600;
      font-size: 14px;
      margin-bottom: 13px;
    }
  }
  .article-submit {
    text-align: right;
    padding: 0 60px;
  }
}
</style>
