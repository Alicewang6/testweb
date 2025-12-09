# 道器智造网站

## 项目结构

```
web/
├── index.html          # 首页
├── about.html          # 关于我们
├── services.html       # 服务介绍
├── products.html       # 产品展示
├── contact.html        # 联系我们
├── css/
│   ├── style.css      # 主样式文件
│   └── tabs.css       # 标签切换组件样式
├── js/
│   ├── tabs.js        # 可复用的标签切换组件
│   ├── carousel.js    # 轮播图功能
│   ├── message.js     # 留言功能
│   └── navbar.js      # 导航栏响应式功能
└── images/
    └── README.md      # 图片说明文件
```

## 功能说明

### 1. 首页 (index.html)
- **轮播图**: 自动播放的图片轮播，支持手动切换
- **服务介绍标签页**: 展示AI、物联网、云计算、大数据等服务
- **留言功能**: 用户可以提交留言，留言保存在浏览器本地存储中

### 2. 关于我们 (about.html)
- 公司介绍和使命愿景
- 发展历程（使用标签切换组件展示）
- 核心团队介绍

### 3. 服务介绍 (services.html)
- 详细的服务分类和介绍
- 使用标签切换组件展示不同服务类别

### 4. 产品展示 (products.html)
- 产品分类展示
- 平台产品、软件产品、硬件产品、解决方案

### 5. 联系我们 (contact.html)
- 公司联系信息
- 在线留言表单

## 可复用组件

### 标签切换组件 (tabs.js)

这是一个可复用的标签切换组件，可以在任何页面使用。

**使用方法：**

1. HTML结构：
```html
<div id="my-tabs" class="tabs-container">
    <div class="tabs-header">
        <button class="tab-btn active" data-tab="tab1">标签1</button>
        <button class="tab-btn" data-tab="tab2">标签2</button>
    </div>
    <div class="tabs-content">
        <div class="tab-panel active" id="tab1">内容1</div>
        <div class="tab-panel" id="tab2">内容2</div>
    </div>
</div>
```

2. 引入CSS和JS：
```html
<link rel="stylesheet" href="css/tabs.css">
<script src="js/tabs.js"></script>
```

3. 组件会自动初始化，无需手动调用。

**注意事项：**
- 每个标签按钮需要有 `data-tab` 属性，值为对应面板的ID
- 第一个标签和面板需要添加 `active` 类
- 面板的ID必须与按钮的 `data-tab` 值匹配

## 图片准备

请将轮播图图片放置在 `images/` 文件夹中：
- `banner-1.jpg` - 技术创新主题
- `banner-2.jpg` - 智能制造主题  
- `banner-3.jpg` - 数字化转型主题

详细说明请查看 `images/README.md`

## 浏览器支持

- Chrome (最新版本)
- Firefox (最新版本)
- Safari (最新版本)
- Edge (最新版本)
- 移动端浏览器

## 技术特点

- 响应式设计，支持移动端和桌面端
- 纯原生JavaScript，无需框架
- 使用CSS变量，易于主题定制
- 留言功能使用LocalStorage本地存储
- 代码结构清晰，易于维护和扩展

## 使用说明

1. 将所有文件放置在web服务器目录中
2. 添加轮播图图片到 `images/` 文件夹
3. 根据需要修改联系信息、公司介绍等内容
4. 可以通过修改CSS变量来调整主题颜色

## 自定义主题颜色

在 `css/style.css` 文件的 `:root` 中修改CSS变量：

```css
:root {
    --primary-color: #2563eb;    /* 主色调 */
    --secondary-color: #1e40af;  /* 次要颜色 */
    --accent-color: #3b82f6;     /* 强调色 */
    /* ... */
}
```

