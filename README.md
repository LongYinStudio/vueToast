# vueToast

`vue 组件 模仿 原生 android 的 toast`

## 使用

```javascript
1. vue 脚手架创建项目，并将文件放在指定目录
2. 导入Toast组件
3. 在Vue实例的事件里添加
   this.$refs.Toast.showToast("内容", 时间/ms);
```

1. 目录结构

```bash
├─App.vue
├─components
     └Toast.vue
```

2. App.vue `导入Toast组件`

```javascript
import Toast from "./components/Toast.vue";
export default {
  components: { Toast },
  methods: {
    show() {
      this.$refs.Toast.showToast("test", 1000);
    },
    comments: {
      Toast,
    },
  },
};
```
