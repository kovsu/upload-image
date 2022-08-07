## 图床

![首页](http://43.138.22.23:3333/images/220827_introduction-1659878977874.png "图片上传")

![Images页面](http://43.138.22.23:3333/images/220827_introduction_2-1659878516951.png "图片分类")

### 技术栈
- 前端使用的是 Vue3 (vue-router vueuse fontawesome ...)
- 后端使用的是 Nest

### 项目描述
只要是正常操作，这个项目能满足一个图床的基本需求。我限制了一次只能选择五张图片，如果你不正常操作，这个也限制不了你。所有图片上传完成时，上传按钮被禁用，你得一个一个清除掉已经上传成功的图片。
在查看所由图片页面，我是根据天进行分类，hover 到图片上，点击就能复制图片的url 到剪切板。

### 不足
- 图片名字不能乱取，不要包含（/ - .）符号
- Images页面是一次性拿取所有图片
- 上传中，上传按钮还是能被点击的，可以加一个状态的变量
- 没有去实现拖拽图片到相应区域，实现上传功能

### 能改进的地方
> 我并没有打算就用这个作为我的图床，这只是一个示例，或者说，我只会用它来保存少量图片。后端提供一个时间（因为我是根据时间分类，这个操作是在前端进行处理完成的）对应图片的接口，然后在 Images 界面第一次返回给最近时间的图片，然后让时间标题是折叠的，点击展开后在发送请求