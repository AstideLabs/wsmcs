# 项目开发 TODO 列表

## 1. 项目初始化与配置
- [x] 创建 Vue 3 + Vite + TypeScript 项目基础代码
- [x] 安装并配置 TailwindCSS
- [x] 配置基础主题色 (Primary: `#2196F3`) 和样式重置
- [x] 按照规范建立目录结构 (`src/components`, `src/assets` 等)
- [x] 复制或整理所需图片资源到 `public/images` 或 `src/assets/images` 目录中

## 2. 核心组件开发 (UI还原)
*(按照 `DESIGN.md` 规范：圆角 `rounded-3xl`，软阴影 `soft shadow`，宽松间距，轻量 hover 动画)*

- [x] **Navbar (顶部导航栏)**
  - [x] 响应式设计（桌面端菜单，移动端折叠菜单）
  - [x] Logo 展示
- [x] **Hero Banner (首屏区域)**
  - [x] 铺满背景图 (`hero-bg` 相关图片)
  - [x] 背景遮罩以提升文字可读性
  - [x] 标题与主 CTA 按钮
- [x] **Features (玩法介绍区域)**
  - [x] 卡片式布局，支持自动换行
  - [x] 展示不同玩法（生存、粘液科技、起床战争等）及对应图片
- [x] **Staff (管理团队区域)**
  - [x] 团队成员卡片展示
- [x] **CTA (加入服务器区域)**
  - [x] 醒目的加入提示与按钮
- [x] **Footer (页脚)**
  - [x] 版权信息及相关链接

## 3. 页面组装与响应式调整
- [x] 在主页面引入并组装所有组件
- [x] 检查并确保 Desktop, Tablet, Mobile 端的响应式表现良好
- [x] 确保移动端无横向滚动，Hero 区域自适应

## 4. 动画与细节打磨
- [x] 添加轻量的渐变过渡和淡入动画 (Fade)
- [x] 添加按钮和卡片的微交互 (Hover 动效)
- [x] 检查图片拉伸问题，确保合理使用 `object-fit`

## 5. 构建与测试验收
- [x] 运行 `npm run build` 确保构建成功
- [x] 检查 TypeScript 报错
- [x] 检查 Console 报错
- [x] 最终对照 `design.png` 检查视觉还原度
