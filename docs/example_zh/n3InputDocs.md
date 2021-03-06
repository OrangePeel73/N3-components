<template>

### 普通输入框

<div class="bs-docs-section" >
<div class="bs-example">

<n3-input v-model="value" ref="input" show-clean></n3-input>
<n3-button @click.native="$refs.input.focus()">聚焦</n3-button>

</div>

```html
<n3-input v-model="value" ref="input" icon="archive"></n3-input>
<n3-button @click.native="$refs.input.focus()">聚焦</n3-button>
```

### 密码输入框

<n3-input v-model="value2" type="password" ref="input2" show-clean></n3-input>
<n3-button @click.native="$refs.input2.focus()">聚焦</n3-button>

```html
<n3-input v-model="value2" ref="password" icon="archive"></n3-input>
<n3-button @click.native="$refs.input2.focus()">聚焦</n3-button>
```

### 参数

| 参数          | 类型            |   默认值         |   说明   |
|-------------  |---------------- |----------------  |-------- |
| name           | `String`     |    －        |        |
| readonly          | `Boolean`     |    `false`        |   只读    |
| disabled          | `Boolean`     |    `false`       |    禁止改变值    |
| width          | `String`     |    `220px`        |   宽度    |
| placeholder          | `String`   |    －        |  placeholder      |
| type          | `String`     |    `text`        |     输入框类型     |
| icon          | `String`     |    -        |     icon     |
| show-clean          | `Boolean`     |    `false`       |     显示清除icon     |

### 组件方法

| 方法名称      | 说明    | 备注      |
|---------- |-------- |---------- |
| clean  | 清空内容 |  |
| focus  | 聚焦 |  |
| blur  | 失焦 |  |

### Events

| 名称          |   说明          |  参数  |      
|-------------  |---------------- | -----|
| blur          | 失焦     | - |
| focus          | 聚焦     | - |
| change | 值变化 |  (currentValue) |

 <p>其他表单相关参数，请移步 <a href="#n3FormDocs" >表单验证</a> 待验证组件参数</p>
   
</div>
</template>

<script>
export default {
  data () {
    return {
      value: '',
      value2: ''
    }
  },
  mounted () {
    this.value = 100
  }
}
</script>
