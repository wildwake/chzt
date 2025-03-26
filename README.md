彩虹特工

## 📖 项目概述

珠玑妙算是一款基于经典Mastermind游戏规则开发的逻辑推理游戏，玩家需要在有限次数内通过系统提供的提示，推理出隐藏的颜色组合。游戏采用现代化UI设计，支持多种难度级别，为玩家提供沉浸式的益智体验。

## ✨ 功能特性

- **多种游戏模式** - 初级模式和高级模式满足不同玩家需求
- **难度选择** - 高级模式支持4-7种颜色的多级难度
- **智能提示系统** - 颜色点提示帮助玩家分析和推理
- **计时与记录** - 记录游戏完成时间，保存最佳记录
- **便捷操作** - 支持点击放置和双击/长按自动填充
- **现代化UI** - 暗色主题、精美动画和响应式设计


</p>

## 🚀 安装与部署

### 环境要求

- HBuilderX 3.0+
- Node.js 12.0.0+
- 微信开发者工具 (用于小程序部署)


```

## 🎮 游戏规则

### 初级模式

1. 系统从7种颜色中选择4种不同颜色作为密码，**颜色不会重复**
2. 玩家有7次机会猜测密码
3. 每次猜测后，系统会提供颜色提示
4. 猜对所有颜色和位置即为胜利
5. **开局辅助**：游戏开始时，系统会自动在第一行填入4种不同颜色作为初始提示，并给出相应的提示点，帮助玩家开始推理
6. **放置规则**：在每行猜测中，玩家不能在同一行中放置重复的颜色
7. **操作方式**：
   - 点击下方颜色选择区的颜色，然后点击棋盘上的空位放置
   - 双击或长按颜色，系统会自动将该颜色填充到当前行的第一个空位
8. **提示系统详解**：
   - 玩家每完成一行猜测后，系统会在棋子右侧显示带颜色的提示点
   - **绿色提示**：表示有棋子的颜色和位置都正确
   - **白色提示**：表示有棋子的颜色正确但位置错误
   - **黑色提示**：表示有棋子完全错误(颜色和位置都不正确)
   - 提示点的**排列顺序**是固定的："绿色→白色→黑色"，与实际棋子的位置无关
   - 提示点的**数量**表示对应状态的棋子数量
   - **示例解读**：如果看到2个绿点、1个白点和1个黑点，意味着有2个棋子完全正确，1个棋子颜色正确但位置错误，1个棋子完全错误

9. **推理技巧**：
   - 利用初始提示行分析可能的颜色组合
   - 每猜测一行后，结合之前的提示进行逻辑推理
   - 如果某行出现多个白点，需考虑颜色位置的不同排列组合
   - 绿点数量增加表示您正在接近正确答案

### 高级模式

1. 系统从4-7种颜色中选择4种不同颜色作为密码（根据难度级别）
2. 玩家有7次机会猜测密码
3. **难度级别**：
   - 入门(4种颜色)：从4种颜色中选择，适合初学者
   - 简单(5种颜色)：从5种颜色中选择，有一定挑战
   - 中等(6种颜色)：从6种颜色中选择，限时挑战！1分钟内完成
   - 困难(7种颜色)：从7种颜色中选择，终极限时挑战！1分钟内猜出答案
4. **计时规则**：
   - 入门和简单难度：记录完成时间，保存最佳记录
   - 中等和困难难度：限时60秒完成，超时即为失败
5. **开局辅助**：游戏开始时，系统会自动在第一行填入4种随机颜色作为初始提示，并确保该提示行的绿色点（完全正确）不超过1个，避免游戏过于简单
6. **放置规则**：与初级模式相同，玩家不能在同一行中放置重复的颜色，密码中的4种颜色也不会重复
7. **提示系统详解**：
   - 玩家每完成一行猜测后，系统会在棋子右侧显示带颜色的提示点
   - **绿色点**：颜色和位置都正确的色块个数
   - **白色点**：颜色正确但位置错误的色块个数
   - **灰色点**：完全错误的色块个数
   - 提示点的**排列顺序**是固定的："绿色→白色→灰色"，与实际棋子的位置无关
   - 提示点的**数量**直接反映各种状态的棋子数量
   - **示例解读**：如果看到2个绿点、1个白点和1个灰点，意味着有2个棋子完全正确，1个棋子颜色正确但位置错误，1个棋子完全错误
   - **高级模式特点**：与初级模式相比，高级模式的挑战在于可用颜色数量更多，需要更复杂的逻辑推理

8. **倒计时挑战**（中等和困难难度）：
   - 倒计时从60秒开始，玩家需要在时间耗尽前猜出正确答案
   - 当剩余时间少于30秒时，界面会进入警告状态，提醒玩家抓紧时间
   - 当剩余时间少于10秒时，界面会进入临界状态，倒计时显示闪烁提醒
   - 最后5秒会有震动提醒（如设备支持）
   - 直观的进度条会实时显示剩余时间比例
   - 时间耗尽时游戏自动结束，视为失败

9. **推理技巧**：
   - 初始提示行通常包含1-2个正确位置的棋子，可作为分析起点
   - 注意分析每行变化后提示点的变化，系统地推理每个位置的可能颜色
   - 使用排除法确定各个位置的可能颜色
   - 优先分析绿点和白点的变化规律
   - 在限时挑战中，应尽量迅速做出有效猜测，避免时间耗尽

10. **辅助功能**：
    - 当前行会高亮显示
    - 完成的行会略微变暗，便于区分
    - 中等和困难难度的界面顶部会显示剩余时间和挑战类型

### 通用操作说明

1. **选择颜色**：点击底部颜色选择区的颜色块
2. **放置颜色**：
   - 方法一：先选择颜色，再点击当前行的空位放置
   - 方法二：双击或长按颜色块，自动将颜色填充到当前行第一个空位
3. **确认猜测**：填满当前行后，点击"确认"按钮提交猜测
4. **清除当前行**：点击"清除"按钮可重新选择当前行的颜色
5. **查看游戏规则**：随时点击"规则"按钮查看游戏说明
6. **重新开始**：点击"重新开始"按钮可重置游戏
7. **返回主页**：点击"退回"按钮可返回到模式选择页面

## 🎓 教学关卡实现流程与逻辑

### 1. 概述

教学关卡是为新手玩家设计的引导式学习功能，帮助玩家快速掌握珠玑妙算的游戏规则和操作方法。与常规游戏模式不同，教学关卡采用了预设的交互流程和视觉提示，通过步骤引导的方式让玩家边玩边学。

### 2. 组件架构

教学关卡通过以下组件架构实现：

```
pages/simple-mode/
├── simple-mode.vue                # 简单模式入口页，包含难度选择和模式切换
└── components/
    ├── SimpleGame.vue             # 常规游戏组件
    └── SimpleTutorial.vue         # 教学关卡组件
```

这种分离式架构使教学功能与常规游戏逻辑分离，便于维护和扩展。

### 3. 教学关卡状态管理

#### 3.1 关键状态变量

```javascript
// 游戏状态相关变量
const currentRow = ref(1);           // 当前活动行（第二行，第一行为提示）
const selectedColor = ref(null);     // 当前选中的颜色
const boardState = ref([]);          // 棋盘状态
const hintState = ref([]);           // 提示状态
const showTutorialModal = ref(false); // 是否显示教学模式提示弹窗
const showStepTooltip = ref(true);   // 是否显示步骤提示框

// 教学步骤
const currentStep = ref(1);          // 当前步骤
```

#### 3.2 教学步骤定义

教学关卡通过预定义的步骤数组控制整个学习流程：

```javascript
const tutorialSteps = [
  // 步骤1: 游戏介绍
  {
    text: "这是一个推理解谜游戏，你将扮演一个侦探，在特定的条件下完成破译密码的任务。"
  },
  // 步骤2: 游戏目标
  {
    text: "游戏目标是猜出密码的4种颜色及其正确的排列顺序。"
  },
  // 步骤3: 绿色提示线说明
  {
    text: "请观察第一行，绿色线条表示该区域颜色和位置都正确。"
  },
  // 步骤4: 白色提示线说明
  {
    text: "请观察第一行，白色线条表示该区域颜色正确但位置错误。"
  },
  // 步骤5: 开始实际操作 - 选择红色
  {
    text: "现在让我们开始解谜，红色和橙色的颜色和位置都对，所以我们优先填入这两个颜色，请选择下方的红色。",
    highlightColor: true,
    colorIndex: 0,  // 高亮红色
    hideButton: true  // 隐藏下一步按钮
  },
  // 步骤6: 放置红色
  {
    text: "很好！现在请点击第二行第一个格子，放置红色方块。",
    highlightSlot: true,
    rowIndex: 1,  // 第二行
    colIndex: 0,   // 第一列
    hideButton: true  // 隐藏下一步按钮
  },
  // 步骤7: 长按操作
  {
    text: "除了点击格子，还有另一种更快的操作方式：长按颜色块可以自动填入空格。请长按橙色试试看！",
    highlightColor: true,
    colorIndex: 1,  // 高亮橙色
    hideButton: true  // 隐藏下一步按钮
  },
  // 步骤8: 放置黄色
  {
    text: "太棒了！现在我们来看黄色和绿色，它们的位置需要交换。让我们先放置黄色，请长按黄色色块。",
    highlightColor: true,
    colorIndex: 2,  // 高亮黄色
    hideButton: true  // 隐藏下一步按钮
  },
  // 步骤9: 放置绿色
  {
    text: "最后，让我们放置绿色。请长按绿色色块完成这一行。",
    highlightColor: true,
    colorIndex: 3,  // 高亮绿色
    hideButton: true  // 隐藏下一步按钮
  },
  // 步骤10: 确认猜测
  {
    text: "现在所有颜色都已经放置完毕，请点击下方闪烁的确认按钮提交答案。",
    highlightConfirmButton: true,  // 高亮确认按钮
    hideButton: true  // 隐藏下一步按钮
  }
];
```

### 4. 教学模式初始化流程

教学关卡的初始化流程包括：

1. **预设第一行**：显示固定的初始提示行，包含4个色块和对应提示
2. **初始化棋盘状态**：创建7×4的空棋盘矩阵
3. **初始化提示状态**：创建对应的提示矩阵
4. **显示欢迎提示**：首次加载时显示教学模式欢迎弹窗

```javascript
// 初始化预设第一行
const initializeFirstRow = () => {
  try {
    // 预设第一行的固定色块
    boardState.value[0] = [
      '#FF0000', // 红色
      '#FF7F00', // 橙色
      '#FFFF00', // 黄色
      '#00FF00', // 绿色
    ];
    
    // 设置2个绿色和2个白色的提示
    hintState.value[0] = ['correct', 'correct', 'misplaced', 'misplaced'];
    
  } catch (error) {
    console.error('初始化教学第一行时出错:', error);
  }
};

// 生命周期钩子
onMounted(() => {
  // 初始化第一行
  initializeFirstRow();
  // 显示教学提示弹窗
  showTutorialModal.value = true;
});
```

### 5. 交互流程与实现

#### 5.1 步骤导航逻辑

教学模式使用 `nextStep` 函数控制步骤导航：

```javascript
// 进入下一个教学步骤
const nextStep = () => {
  if (currentStep.value < tutorialSteps.length) {
    currentStep.value++;
    
    // 根据步骤设置高亮内容
    if (currentStep.value === 3) {
      // 第三步：高亮绿色线条
      currentHighlight.value = 'correct';
      highlightColorIndex.value = null;
      highlightSlotPosition.value = { row: null, col: null };
    } else if (currentStep.value === 4) {
      // 第四步：高亮白色线条
      currentHighlight.value = 'misplaced';
      highlightColorIndex.value = null;
      highlightSlotPosition.value = { row: null, col: null };
    }
    // ... 其他步骤设置
  } else {
    // 最后一步完成后隐藏提示
    showStepTooltip.value = false;
    currentHighlight.value = null;
    highlightColorIndex.value = null;
    highlightSlotPosition.value = { row: null, col: null };
  }
};
```

#### 5.2 交互事件处理

教学关卡的交互事件处理包括：

1. **颜色选择**：玩家点击颜色块时的处理逻辑
   ```javascript
   const handleColorSelect = (color, index) => {
     selectedColor.value = color;
     
     // 如果是在教学步骤中选择了高亮的颜色，自动进入下一步
     if (currentStep.value === 5 && index === highlightColorIndex.value) {
       nextStep();
     }
   };
   ```

2. **放置色块**：玩家点击棋盘格子时的处理逻辑
   ```javascript
   const handlePegTap = (rowIndex, colIndex) => {
     // 只能在当前活动行放置颜色
     if (rowIndex !== currentRow.value) return;
     
     // 需要先选择颜色
     if (selectedColor.value === null) {
       uni.showToast({
         title: '请先选择一个颜色',
         icon: 'none',
         duration: 1500
       });
       return;
     }
     
     // 更新棋盘状态
     boardState.value[rowIndex][colIndex] = selectedColor.value;
     
     // 如果是在教学步骤中放置在高亮格子，自动进入下一步
     if (currentStep.value === 6 && 
         rowIndex === highlightSlotPosition.value.row && 
         colIndex === highlightSlotPosition.value.col) {
       nextStep();
     }
   };
   ```

3. **长按操作**：长按颜色块自动填充的处理逻辑
   ```javascript
   const handleColorLongPress = (color, index) => {
     selectedColor.value = color;
     
     // 自动填入当前行的第一个空格
     const currentRowState = boardState.value[currentRow.value];
     const emptySlotIndex = currentRowState.findIndex(slot => slot === null);
     
     if (emptySlotIndex !== -1) {
       boardState.value[currentRow.value][emptySlotIndex] = color;
     }
     
     // 如果是在教学步骤中长按了高亮的颜色，自动进入下一步
     if ((currentStep.value === 7 || currentStep.value === 8 || currentStep.value === 9) && 
         index === highlightColorIndex.value) {
       nextStep();
     }
   };
   ```

4. **确认猜测**：点击确认按钮时的处理逻辑
   ```javascript
   const confirmCurrentRow = () => {
     // 检查当前行是否已填满
     if (!boardState.value[currentRow.value].every(color => color !== null)) {
       uni.showToast({
         title: '请先填满当前行',
         icon: 'none',
         duration: 1500
       });
       return;
     }
     
     // 如果是在教学步骤中点击了确认按钮
     if (currentStep.value === 10) {
       // 显示成功提示框
       showSuccessModal.value = true;
       // 隐藏教学提示
       showStepTooltip.value = false;
     }
   };
   ```

### 6. 视觉反馈系统

教学模式使用多种视觉提示帮助玩家理解游戏规则：

#### 6.1 高亮提示系统

```html
<!-- 色块高亮效果 -->
<view 
  v-if="currentHighlight && hintState[row - 1] && hintState[row - 1][col - 1] === currentHighlight"
  class="peg-highlight"
  :class="{
    'highlight-correct': currentHighlight === 'correct',
    'highlight-misplaced': currentHighlight === 'misplaced'
  }"
></view>

<!-- 颜色选择区高亮 -->
<view 
  v-for="(color, index) in colorOptions" 
  :key="index"
  class="color-option"
  :class="{
    'selected-color': selectedColor === color,
    'highlight-color': highlightColorIndex === index
  }"
  :style="{ backgroundColor: color }"
  @click="handleColorSelect(color, index)"
  @longpress="handleColorLongPress(color, index)"
></view>
```

#### 6.2 弹窗提示系统

```html
<!-- 教学提示弹窗 -->
<view class="tutorial-modal-overlay" v-if="showTutorialModal">
  <view class="tutorial-modal" @click.stop>
    <view class="tutorial-modal-header">
      <text class="tutorial-modal-title">游戏目的</text>
      <view class="tutorial-close-btn" @click="closeTutorialModal">×</view>
    </view>
    
    <view class="tutorial-modal-body">
      <!-- 教学内容区 -->
    </view>
    
    <view class="tutorial-modal-footer">
      <button class="tutorial-confirm-btn" @click="closeTutorialModal">开始教学</button>
    </view>
  </view>
</view>

<!-- 小型提示框 -->
<view class="floating-tooltip" v-if="showStepTooltip">
  <view class="tooltip-content">
    <text class="tooltip-text">{{ tutorialSteps[currentStep - 1].text }}</text>
    <view class="tooltip-buttons" v-if="!tutorialSteps[currentStep - 1].hideButton">
      <button class="tooltip-btn" @click="nextStep">{{ currentStep < tutorialSteps.length ? '下一步' : '完成教学' }}</button>
    </view>
  </view>
</view>
```

### 7. 教学完成与进阶

教学完成后，系统会显示一个成功提示，并引导玩家进入正式游戏：

```javascript
// 修改关闭成功提示框的方法
const closeSuccessModal = () => {
  showSuccessModal.value = false;
  // 返回到难度选择界面，并传递参数指示选中入门难度
  emit('back', { selectDifficulty: 'beginner' });
};
```

### 8. 开发者扩展建议

对于想要扩展或修改教学关卡的开发者，可以考虑以下几点：

1. **增加教学步骤**：通过扩展 `tutorialSteps` 数组添加更多教学内容
2. **定制高亮内容**：修改 `highlightColorIndex` 和 `highlightSlotPosition` 来自定义高亮位置
3. **添加互动效果**：在 `handlePegTap`、`handleColorSelect` 等函数中增加更多互动逻辑
4. **优化提示文本**：修改步骤说明文本，使其更加直观易懂
5. **添加动画效果**：扩展 CSS 动画，增强视觉体验
6. **多语言支持**：将提示文本抽取为配置，支持多语言切换

### 9. 实现关键点

1. **预设棋盘状态**：预先设置第一行，作为玩家推理的基础
2. **步骤式引导**：将教学分解为小步骤，逐步引导玩家学习
3. **交互式学习**：通过高亮和引导完成实际操作，加深理解
4. **视觉反馈**：使用高亮效果直观展示关键元素
5. **渐进式难度**：从简单概念开始，逐步引入复杂规则
6. **无缝过渡**：教学完成后自然过渡到实际游戏

通过这种结构化的教学设计，新手玩家可以在几分钟内掌握游戏的核心规则和操作方法，显著降低学习门槛，提升游戏体验。

## 📂 项目结构

```
project-root/
├── pages/                       # 页面文件
│   ├── index/                   # 首页(游戏模式选择)
│   │   └── index.vue           
│   ├── simple-mode/             # 初级模式
│   │   └── simple-mode.vue
│   └── advanced-mode/           # 高级模式
│       └── advanced-mode.vue
├── static/                      # 静态资源文件
├── components/                  # 公共组件
├── App.vue                      # 应用入口组件
├── main.js                      # 应用入口js
├── manifest.json                # 应用配置
├── pages.json                   # 页面路由配置
└── uni.scss                     # 全局样式变量
```

## 💻 核心技术

- **前端框架**: uni-app (基于Vue.js)
- **状态管理**: Vue Composition API
- **UI设计**: 自定义组件 + CSS3动画
- **存储**: uni-app本地存储API

## ❓ 常见问题

### Q1: 游戏进度会保存吗？
A1: 游戏当前不支持进度保存，但会保存您的最佳记录时间。

### Q2: 如何区分初级模式和高级模式？
A2: 初级模式固定使用7种颜色中的4种，而高级模式可以根据难度选择4-7种可用颜色，颜色池更大，但两种模式下密码都是4种不同的颜色（无重复）。

### Q3: 提示点的颜色含义是什么？
A3: 
- 绿色点：表示颜色和位置都正确的棋子数量
- 白色点：表示颜色正确但位置错误的棋子数量
- 灰色点：表示完全错误的棋子数量

## 📝 更新日志

### V1.0.0 (2023-10-15)
- 初始版本发布
- 支持初级模式和高级模式
- 实现基本游戏功能和计时系统

## 🤝 贡献指南

1. Fork 项目
2. 创建特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 打开一个 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 👥 开发团队

- 产品设计: [开发者姓名]
- 前端开发: [开发者姓名]
- UI设计: [设计师姓名]

## 📱 联系与支持

- **问题反馈**: [contact@example.com]
- **官方网站**: [https://www.example.com]

## 📱 界面设计详解

本章节详细描述了游戏中各个页面的设计与实现，帮助开发者理解整个应用的界面结构和交互流程。

### 1. 主页 (pages/index/index.vue)

#### 1.1 页面结构

主页采用垂直流式布局，自上而下分为以下几个部分：

```
主页
├── 游戏标题区域
│   ├── 标题文本 "珠玑妙算"
│   ├── 副标题
│   └── 标题下划线装饰
├── 游戏模式选择区域
│   ├── 初级模式卡片
│   ├── 高级模式卡片
│   └── 闯关模式卡片 (带开发中提示)
├── 游戏说明按钮区域
└── 版本信息
```

#### 1.2 视觉设计

1. **背景效果**
   - 使用深色渐变背景 `linear-gradient(135deg, #0f0c29, #302b63, #24243e)`
   - 背景动画：15秒周期的渐变位置变换
   - 装饰性浮动圆圈：10个不同颜色、大小、透明度的圆形元素随机分布，带有浮动动画

2. **标题区域**
   - 主标题："珠玑妙算"，大号白色字体，带发光效果
   - 副标题：浅色小号字体
   - 标题下方有渐变横线装饰

3. **模式卡片**
   - 半透明玻璃拟态风格：`background: rgba(255, 255, 255, 0.08); backdrop-filter: blur(10rpx);`
   - 轻微边框：`border: 1px solid rgba(255, 255, 255, 0.1);`
   - 阴影效果：`box-shadow: 0 8rpx 32rpx rgba(0, 0, 0, 0.1);`
   - 按压反馈：点击时缩小至97%
   - 每个卡片包含：图标、标题、描述文本和操作按钮
   - 闯关模式卡片有"开发中"遮罩层和提示标签

4. **游戏介绍按钮**
   - 圆角按钮，使用玻璃拟态设计
   - 居中放置，宽度为屏幕的50%

5. **版本信息**
   - 位于页面右下角，小号浅色文本

#### 1.3 交互逻辑

1. **模式选择**
   - 点击初级模式卡片：导航至`/pages/simple-mode/simple-mode`
   - 点击高级模式卡片：导航至`/pages/advanced-mode/advanced-mode`
   - 点击闯关模式卡片：显示"正在开发中"提示，不跳转

2. **游戏规则查看**
   - 点击"游戏规则"按钮：弹出模态框显示详细游戏规则

3. **平台适配**
   - 自动检测平台（iOS/Android）并调整状态栏高度
   - 适配刘海屏，保证内容不被系统UI遮挡

#### 1.4 主要样式

```css
/* 容器基础样式 */
.container {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 40rpx 40rpx 40rpx;
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
}

/* 模式卡片样式 */
.game-mode-card {
  position: relative;
  border-radius: 20rpx;
  overflow: hidden;
  background: rgba(255, 255, 255, 0.08);
  backdrop-filter: blur(10rpx);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 8rpx 32rpx rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
  height: 140rpx;
  padding: 25rpx 30rpx;
}

/* 标题文本样式 */
.title-text {
  font-size: 55rpx;
  font-weight: bold;
  color: #ffffff;
  text-shadow: 0 4rpx 8rpx rgba(0, 0, 0, 0.4);
  letter-spacing: 2rpx;
  display: block;
  margin-bottom: 5rpx;
  animation: fadeIn 1.5s ease;
}
```

### 2. 初级模式 (pages/simple-mode/simple-mode.vue)

#### 2.1 页面结构

初级模式页面有两个主要状态：难度选择状态和游戏状态，通过v-if/v-else控制显示。

**难度选择状态结构：**
```
难度选择页面
├── 模式标题 ("初级模式")
├── 难度选择轮播组件
│   ├── 教学关卡卡片
│   ├── 4色难度卡片
│   ├── 5色难度卡片
│   ├── 6色难度卡片
│   └── 7色难度卡片
├── 开始游戏按钮
└── 返回主页按钮
```

**游戏状态结构：**
```
游戏页面 (条件渲染)
├── 教学关卡组件 (SimpleTutorial.vue) - 当选择教学关卡时显示
└── 游戏组件 (SimpleGame.vue) - 当选择其他难度时显示
```

#### 2.2 视觉设计

1. **难度选择界面**
   - 背景：深色主题，与主页保持一致
   - 难度卡片：使用横向轮播组件，展示5个不同难度选项
   - 每个卡片显示：难度等级、星级评价、颜色数量、颜色预览、描述文本和最佳记录
   - 教学模式卡片有特殊标识和样式

2. **难度卡片设计**
   - 卡片采用浮动立体效果，激活状态有额外的高亮边框
   - 颜色预览区展示实际游戏中使用的颜色
   - 教学卡片有特殊图标和提示文本

3. **按钮设计**
   - 开始游戏：大尺寸彩色渐变按钮，有轻微的提升阴影
   - 返回主页：次要按钮，半透明设计

#### 2.3 交互逻辑

1. **难度选择**
   - 横向滑动切换难度卡片
   - 点击卡片直接选中对应难度
   - 轮播组件底部有指示点，标记当前位置

2. **游戏流程控制**
   - 点击"开始游戏"：设置gameStarted为true，显示游戏组件
   - 根据selectedDifficulty条件渲染SimpleTutorial或SimpleGame组件
   - 游戏组件可通过emit事件返回难度选择界面

3. **数据持久化**
   - 读取并显示各难度的最佳记录
   - 游戏完成后更新并保存最佳记录

#### 2.4 主要样式

```css
/* 难度卡片样式 */
.difficulty-card {
  width: 85%;
  height: 350rpx;
  margin: 0 auto;
  padding: 30rpx;
  background: rgba(255, 255, 255, 0.08);
  border-radius: 20rpx;
  box-shadow: 0 10rpx 30rpx rgba(0, 0, 0, 0.2);
  transition: all 0.3s ease;
}

.active-card {
  transform: translateY(-10rpx);
  border: 2px solid rgba(255, 255, 255, 0.3);
  background: rgba(255, 255, 255, 0.12);
}

/* 教学卡片特殊样式 */
.tutorial-card {
  border-left: 5rpx solid #4CAF50;
}

/* 开始游戏按钮 */
.start-btn {
  width: 80%;
  height: 90rpx;
  background: linear-gradient(135deg, #43cea2, #185a9d);
  color: #ffffff;
  border-radius: 45rpx;
  font-size: 32rpx;
  font-weight: 500;
  box-shadow: 0 8rpx 25rpx rgba(24, 90, 157, 0.3);
}
```

### 3. 教学关卡 (components/SimpleTutorial.vue)

#### 3.1 组件结构

```
教学关卡组件
├── 游戏头部
│   ├── 标题 ("教学模式")
│   └── 难度标签 ("入门")
├── 游戏棋盘
│   ├── 7行猜测区域
│   │   └── 每行4个色块位置
│   ├── 颜色选择区
│   │   ├── 4种颜色选项
│   │   ├── 确认按钮
│   │   └── 清除按钮
│   └── 控制按钮区
│       ├── 返回按钮
│       └── 重新开始按钮
├── 教学提示弹窗 (首次显示)
├── 步骤提示框 (跟随教学步骤)
└── 成功提示框 (教学完成时)
```

#### 3.2 视觉设计

1. **整体界面**
   - 深色背景，现代化界面
   - 第一行为固定的提示行，包含4个预设颜色和提示
   - 当前活动行有高亮效果，其他行有不同的透明度

2. **教学提示设计**
   - 初始大型弹窗：清晰介绍游戏目标和基本规则
   - 浮动小型提示框：位于界面中上部，显示当前步骤的具体指引
   - 步骤提示框：包含提示文本和下一步按钮
   - 特定步骤中的高亮元素：高亮当前需要关注的UI元素

3. **高亮反馈系统**
   - 色块高亮：边缘发光效果，吸引用户注意
   - 提示线高亮：增强提示线的可见性
   - 按钮高亮：增加呼吸动画

4. **成功提示设计**
   - 全屏半透明遮罩
   - 居中显示的成功信息卡片
   - 祝贺文本和继续游戏按钮

#### 3.3 交互逻辑

详见上面的"教学关卡实现流程与逻辑"章节中的完整描述。

#### 3.4 主要样式

```css
/* 游戏棋盘容器 */
.game-board {
  flex: 1;
  padding: 20rpx 0;
  width: 100%;
}

/* 猜测行样式 */
.guess-row {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 10rpx 0;
  padding: 10rpx;
  border-radius: 10rpx;
}

/* 教学提示弹窗 */
.tutorial-modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.75);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

/* 高亮效果 */
.highlight-color {
  box-shadow: 0 0 0 4rpx #ffffff, 0 0 20rpx 4rpx rgba(81, 230, 255, 0.8);
  transform: scale(1.1);
  z-index: 2;
  animation: pulse 1.5s infinite;
}
```

### 4. 游戏组件 (components/SimpleGame.vue)

#### 4.1 组件结构

```
游戏组件
├── 游戏头部
│   ├── 左侧区域
│   │   ├── 模式标题
│   │   ├── 难度标签
│   │   └── 计时器
│   └── 右侧区域 (留白或按钮)
├── 游戏棋盘
│   ├── 7行猜测区域
│   │   └── 每行4个色块位置
│   ├── 颜色选择区
│   │   ├── 4-7种颜色选项 (根据难度)
│   │   ├── 确认按钮
│   │   └── 清除按钮
│   └── 控制按钮区
│       ├── 返回按钮
│       ├── 重新开始按钮
│       └── 规则按钮
└── 结果弹窗 (游戏结束时)
```

#### 4.2 视觉设计

1. **头部设计**
   - 模式标题和难度显示
   - 计时器：高级模式显示倒计时，初级模式显示计时
   - 最佳记录显示（如果有）

2. **棋盘设计**
   - 活动行有轻微的高亮背景
   - 完成的行略微变暗
   - 色块使用圆形设计，有边框和阴影
   - 提示线使用不同颜色：绿色(正确)、白色(位置错误)、灰色(完全错误)

3. **颜色选择区**
   - 圆形颜色按钮，选中状态有边框高亮
   - 确认和清除按钮有明显的状态反馈
   - 按钮悬停和按压效果

4. **结果弹窗**
   - 成功/失败状态有不同的标题栏颜色
   - 显示正确的颜色组合
   - 展示用时和记录信息
   - 提供"再玩一次"、"返回菜单"和"下一难度"(如适用)按钮

#### 4.3 交互逻辑

1. **游戏初始化**
   - 根据难度设置可用颜色
   - 随机生成4个不同颜色作为密码
   - 初始化提示行：随机4色但保证绿色提示不超过2个
   - 开始计时器：普通计时或倒计时

2. **游戏操作**
   - 选择颜色：点击颜色选择区
   - 放置色块：点击格子或长按颜色自动填充
   - 确认猜测：提交当前行，获取反馈
   - 清除当前行：重新选择

3. **结果处理**
   - 胜利条件：所有提示都为correct
   - 失败条件：用完7次机会或时间耗尽
   - 记录保存：如果是新纪录，存储最佳时间

#### 4.4 主要样式

```css
/* 游戏头部样式 */
.game-header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20rpx 30rpx;
  margin-bottom: 20rpx;
}

/* 棋子样式 */
.peg {
  width: 80rpx;
  height: 80rpx;
  border-radius: 50%;
  box-shadow: 0 4rpx 8rpx rgba(0, 0, 0, 0.3);
  border: 1px solid rgba(255, 255, 255, 0.2);
  transition: all 0.2s ease;
}

/* 提示线样式 */
.hint-line {
  position: absolute;
  right: -10rpx;
  width: 6rpx;
  height: 70%;
  border-radius: 3rpx;
}

.correct-line {
  background-color: #4CAF50;
}

.misplaced-line {
  background-color: #FFFFFF;
}

.incorrect-line {
  background-color: #555555;
}

/* 结果弹窗样式 */
.result-modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}
```

### 5. 高级模式 (pages/advanced-mode/advanced-mode.vue)

#### 5.1 页面结构

高级模式的整体结构与初级模式类似，但有一些针对高级功能的特殊设计。

```
高级模式页面
├── 难度选择状态
│   ├── 模式标题 ("高级模式")
│   ├── 难度选择轮播组件
│   │   ├── 4色难度卡片 ("入门")
│   │   ├── 5色难度卡片 ("简单")
│   │   ├── 6色难度卡片 ("中等") - 带限时标识
│   │   └── 7色难度卡片 ("困难") - 带限时标识
│   ├── 开始游戏按钮
│   └── 返回主页按钮
└── 游戏状态
    └── 高级游戏组件 (AdvancedGame.vue)
```

#### 5.2 视觉设计

1. **难度选择界面**
   - 与初级模式相似的卡片设计，但颜色主题不同
   - 限时难度(中等/困难)有倒计时图标和特殊标识
   - 更多颜色选项的视觉预览

2. **游戏界面特色**
   - 高级模式特有的倒计时进度条
   - 不同难度有不同的颜色主题
   - 倒计时警告状态：时间不足时界面变红

#### 5.3 交互逻辑

1. **难度控制**
   - 选择4-7色难度，6-7色为限时模式
   - 限时模式有60秒倒计时
   - 时间不足时有视觉和震动警告

2. **高级游戏流程**
   - 初始提示行：确保绿色提示不超过1个
   - 更多颜色选择，增加推理难度
   - 限时挑战：时间耗尽自动结束游戏

#### 5.4 主要样式

```css
/* 限时难度标识 */
.timed-challenge {
  position: absolute;
  top: 15rpx;
  right: 15rpx;
  background: rgba(255, 87, 34, 0.9);
  color: white;
  font-size: 22rpx;
  padding: 4rpx 12rpx;
  border-radius: 20rpx;
  display: flex;
  align-items: center;
}

/* 倒计时进度条 */
.timer-progress {
  width: 100%;
  height: 6rpx;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 3rpx;
  overflow: hidden;
  margin-top: 6rpx;
}

.timer-progress-bar {
  height: 100%;
  background: linear-gradient(90deg, #4CAF50, #FFEB3B, #FF5722);
  transition: width 1s linear;
}

/* 警告状态 */
.timer-warning {
  color: #FF5722;
  animation: blink 1s infinite;
}
```

### 6. 闯关模式 (pages/complex-mode/complex-mode.vue)

#### 6.1 页面结构

闯关模式目前显示为"开发中"状态，页面结构简单。

```
闯关模式页面
├── 页面头部
│   ├── 返回按钮
│   └── 标题 ("闯关模式")
└── 开发中提示容器
    ├── 开发中图标
    ├── 标题 ("功能开发中")
    ├── 提示信息
    ├── 详细说明
    └── 返回主页按钮
```

#### 6.2 视觉设计

1. **整体界面**
   - 深色背景，与其他页面保持一致
   - 居中显示的开发中提示卡片
   - 玻璃拟态效果设计

2. **提示卡片设计**
   - 半透明背景，模糊效果
   - 旋转的施工图标
   - 清晰的提示文本
   - 引导用户返回的按钮

#### 6.3 交互逻辑

1. **基本操作**
   - 页面加载时显示Toast提示"功能开发中"
   - 点击返回按钮或返回主页按钮：导航回主页

#### 6.4 主要样式

```css
.developing-container {
  width: 90%;
  max-width: 650rpx;
  margin: 60rpx auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 30rpx;
  padding: 50rpx 40rpx;
  backdrop-filter: blur(10px);
  box-shadow: 0 10rpx 30rpx rgba(0, 0, 0, 0.2);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.developing-icon {
  font-size: 100rpx;
  margin-bottom: 30rpx;
  animation: rotate 3s infinite linear;
}

.back-home-btn {
  width: 70%;
  height: 90rpx;
  border-radius: 45rpx;
  background: linear-gradient(135deg, #43cea2, #185a9d);
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 32rpx;
  font-weight: 500;
  box-shadow: 0 5rpx 15rpx rgba(24, 90, 157, 0.3);
  transition: all 0.2s ease;
}
```

### 7. 全局UI组件与样式

#### 7.1 全局主题

游戏整体采用深色主题，主要颜色配置如下：

```css
:root {
  /* 主要颜色 */
  --primary-bg: #1e1e2e;
  --secondary-bg: #252535;
  --card-bg: rgba(255, 255, 255, 0.08);
  
  /* 文本颜色 */
  --text-primary: #ffffff;
  --text-secondary: rgba(255, 255, 255, 0.7);
  --text-tertiary: rgba(255, 255, 255, 0.4);
  
  /* 强调色 */
  --accent-green: #4CAF50;
  --accent-blue: #2196F3;
  --accent-orange: #FF9800;
  --accent-red: #FF5722;
  
  /* 界面尺寸 */
  --status-bar-height: 44px; /* 默认值，会被JS动态替换 */
  --border-radius: 20rpx;
  --card-padding: 30rpx;
}
```

#### 7.2 通用卡片组件

游戏中的卡片元素共享以下设计特点：

```css
.card {
  background: rgba(255, 255, 255, 0.08);
  backdrop-filter: blur(10rpx);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 20rpx;
  box-shadow: 0 8rpx 32rpx rgba(0, 0, 0, 0.1);
  padding: 25rpx 30rpx;
}
```

#### 7.3 按钮样式

游戏中使用的按钮有几种主要类型：

1. **主按钮**：用于主要操作，如开始游戏
   ```css
   .primary-btn {
     background: linear-gradient(135deg, #43cea2, #185a9d);
     color: #ffffff;
     border-radius: 45rpx;
     height: 90rpx;
     font-weight: 500;
     box-shadow: 0 8rpx 25rpx rgba(24, 90, 157, 0.3);
   }
   ```

2. **次要按钮**：用于辅助操作，如返回
   ```css
   .secondary-btn {
     background: rgba(255, 255, 255, 0.08);
     color: rgba(255, 255, 255, 0.9);
     border: 1px solid rgba(255, 255, 255, 0.1);
     border-radius: 45rpx;
     height: 80rpx;
   }
   ```

3. **控制按钮**：用于游戏内操作，如确认、清除
   ```css
   .control-btn {
     height: 80rpx;
     border-radius: 12rpx;
     box-shadow: 0 4rpx 12rpx rgba(0, 0, 0, 0.2);
   }
   ```

#### 7.4 动画效果

游戏中使用了多种动画效果增强用户体验：

```css
/* 渐入动画 */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10rpx); }
  to { opacity: 1; transform: translateY(0); }
}

/* 呼吸效果 */
@keyframes pulse {
  0% { opacity: 0.6; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.05); }
  100% { opacity: 0.6; transform: scale(1); }
}

/* 旋转动画 */
@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

/* 背景渐变动画 */
@keyframes gradientBG {
  0% { background-position: 0% 50% }
  50% { background-position: 100% 50% }
  100% { background-position: 0% 50% }
}

/* 闪烁效果 */
@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}
```

通过以上详细的界面描述，开发者应该能够清晰地理解游戏的整体设计风格、布局结构和交互逻辑，从而能够重新制作出相似的界面。

---

<p align="center">如果您喜欢这个项目，别忘了给它一个⭐️</p> 