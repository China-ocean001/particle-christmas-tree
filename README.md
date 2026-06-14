# 🎄 粒子圣诞树特效

> HTML Canvas 粒子动画圣诞树 — 纯前端节日特效

<div align="center">

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Canvas](https://img.shields.io/badge/Canvas-API-FF6384?style=flat)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)](LICENSE)

</div>

---

## 📖 项目简介

两个纯前端圣诞树特效页面，使用 HTML5 Canvas 和 CSS3 实现，无需任何依赖，浏览器直接打开即可欣赏。

---

## ✨ 效果展示

| 文件 | 技术 | 效果描述 |
|------|------|----------|
| `christmas_tree.html` | CSS3 绘制 | 传统圣诞树造型，层叠三角形 + 装饰球 + 星星顶部 |
| `particle_christmas_tree.html` | Canvas 粒子动画 | 数千粒子组成圣诞树，动态飘落雪花、闪烁彩灯 |

---

## 🎨 技术实现

### christmas_tree.html — CSS 圣诞树

```
          ★
         /★\
        /★★★\
       /★★★★★\
      /★★★★★★★\
     /★★★★★★★★★\
    /★★★★★★★★★★★\
   /★★★★★★★★★★★★★\
        ||||||
        ||||||
```

- CSS `border` 技巧绘制三角形
- CSS `box-shadow` 装饰球
- 纯 CSS 无 JS

### particle_christmas_tree.html — 粒子动画

```javascript
// 核心动画循环
class ParticleTree {
  constructor(canvas) {
    this.particles = [];     // 粒子数组
    this.snowflakes = [];    // 雪花数组
  }

  animate() {
    // 1. 清除画布
    // 2. 更新所有粒子（旋转、闪烁）
    // 3. 更新雪花（飘落、重置）
    // 4. 递归调用 requestAnimationFrame
    requestAnimationFrame(() => this.animate());
  }
}
```

- **粒子系统**：数千个彩色粒子组成圣诞树轮廓
- **雪花飘落**：随机生成，自然飘落效果
- **彩灯闪烁**：粒子颜色周期性变换
- **星星旋转**：顶部星星持续旋转

---

## 🚀 快速开始

### 零依赖预览

直接用浏览器打开：

```bash
# 普通圣诞树
start christmas_tree.html          # Windows
open christmas_tree.html           # macOS

# 粒子圣诞树 (推荐！)
start particle_christmas_tree.html # Windows
open particle_christmas_tree.html  # macOS
```

### 本地服务器

```bash
npx serve .
# 访问 http://localhost:3000
```

---

## ⚙️ 自定义

在 `particle_christmas_tree.html` 中可调整：

```javascript
// 粒子数量（越多越密集）
const PARTICLE_COUNT = 3000;

// 雪花密度
const SNOWFLAKE_COUNT = 100;

// 动画速度
const ANIMATION_SPEED = 1;

// 圣诞树颜色
const TREE_COLORS = ['#2ecc71', '#27ae60', '#1abc9c'];

// 装饰灯颜色
const LIGHT_COLORS = ['#e74c3c', '#f1c40f', '#3498db', '#e91e63'];
```

---

## 🌐 浏览器兼容性

| 浏览器 | 兼容性 |
|--------|--------|
| Chrome 90+ | ✅ 完美 |
| Edge 90+ | ✅ 完美 |
| Firefox 88+ | ✅ 完美 |
| Safari 14+ | ✅ 完美 |
| IE 11 | ❌ 不支持 Canvas |

---

## 📄 License

MIT License

---

<div align="center">

🎄 **Merry Christmas!** 🎅

**⭐ 如果这个项目让你开心，请给一个 Star！**

</div>
