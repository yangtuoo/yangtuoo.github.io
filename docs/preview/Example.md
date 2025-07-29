---
title: 写作文章示例汇总
tags:
  - Examples
createTime: 2025/07/20 14:30:31
permalink: /article/ACexamples/
---

## Markdown


### 隐秘文本
- 启用  
  在`.vuepress/config.ts`文件于`markdown`位置配置`plot: true`  
- 代码示例
  - 遮罩层效果 + 鼠标悬停(`!!文本!!{.mask .hover}`)：!!文本!!{.mask .hover} 
  - 遮罩层效果 + 点击(`!!文本!!{.mask .click}`)：!!文本!!{.mask .click} 
  - 文本模糊效果 + 鼠标悬停(`!!文本!!{.blur .hover}`)：!!文本!!{.blur .hover} 
  - 文本模糊效果 + 点击(`!!文本!!{.blur .click}`)：!!文本!!{.blur .click} 

### 马克笔
- 内置配置
   - **default**: `==Default==` - ==Default==
   - **info**: `==Info=={.info}` - ==Info=={.info}
   - **note**: `==Note=={.note}` - ==Note=={.note}
   - **tip**: `==Tip=={.tip}` - ==Tip=={.tip}
   - **warning**: `==Warning=={.warning}` - ==Warning=={.warning}
   - **danger**: `==Danger=={.danger}` - ==Danger=={.danger}
   - **caution**: `==Caution=={.caution}` - ==Caution=={.caution}
   - **important**: `==Important=={.important}` - ==Important=={.important}

### 缩写词

- 启用：在`.vuepress/config.ts`文件于`markdown`位置配置`abbr: true`
- 代码示例：  
  **输入：**

  ```md
  The HTML specification is maintained by the W3C.

  *[HTML]: Hyper Text Markup Language
  *[W3C]:  World Wide Web Consortium
  ```

  **输出：**

  The HTML specification is maintained by the W3C.

  *[HTML]: Hyper Text Markup Language
  *[W3C]:  World Wide Web Consortium

### 内容注释
- 启用：在`.vuepress/config.ts`文件于`markdown`位置配置`annotation: true`
- 代码示例：
  同一个 label 定义单或多个注释，多个定义以列表的形式渲染。
  **输入：**
  
  ```md
  我是一个单个label [+label] 
  
  [+label]:
     示例1
  [+label]:
     示例2
  ```
  
  **输出：**
  
  我是一个label [+label] 
  
  [+label]:
     示例1
  [+label]:
     示例2


### 折叠面板

::: tabs
   @tab 启用

      该功能默认不启用，你需要在 `theme` 配置中启用。

      ```ts title=".vuepress/config.ts"
      export default defineUserConfig({
      theme: plumeTheme({
      markdown: {
         collapse: true, // [!code ++]
      }
         })
      })
      ```

   @tab 普通格式

      __输入：__

      ```md
      ::: collapse
      - 标题 1        
                     
      内容          

      - 标题 2

      内容
      :::
      ```
   @tab 特殊说明
      添加 `expand` 选项，默认展开所有面板  
      例如：`::: collapse expand`  

      添加 `accordion` 选项，设置为手风琴模式，只允许展开一个面板，点击其他面板会关闭之前的面板    
      例如：`::: collapse accordion`

      折叠面板默认全部关闭，可以使用 `:+` 标记项初始状态为展开。    
      例如：`:+ 标题 2` 

      折叠面板配置 `expand` 时默认全部展开，可以使用 `:-` 标记项初始状态为折叠。 
      例如：`:- 标题 2 `  


    
:::
- 代码示例
::: collapse
- 标题 1        
                
  内容          

- 标题 2

  内容
:::

### 选项组
- 代码示例  
   **输入：**

   ````
   ::: tabs
   @tab 示例1

   内容

   @tab 示例2

   ```md
  示例
   ```

   :::
   ````

   **输出：**

   ::: tabs
   @tab 示例1

   内容

   @tab 示例2

   ```md
    示例
   ```

   :::

### MarkDown卡片
- 代码示例
   输入
   ```md
   <!-- 单个卡片 -->
   ::: card title="标题" icon="twemoji:astonished-face"

   这里是卡片内容。
   :::

   <!-- 多个卡片 -->
   :::: card-grid

   ::: card title="卡片标题 1" icon="twemoji:astonished-face"

   这里是卡片内容。
   :::

   ::: card title="卡片标题 2" icon="twemoji:astonished-face"

   这里是卡片内容。
   :::

   ::::
   ```
   输出
   <!-- 单个卡片 -->
   ::: card title="标题" icon="twemoji:astonished-face"

   这里是卡片内容。
   :::

   <!-- 多个卡片 -->
   :::: card-grid

   ::: card title="卡片标题 1" icon="twemoji:astonished-face"

   这里是卡片内容。
   :::

   ::: card title="卡片标题 2" icon="twemoji:astonished-face"

   这里是卡片内容。
   :::

   ::::


### 步骤容器
- 说明  
  在 `steps` 容器内，使用 有序列表 （或无序列表） 来表示步骤。你可以在 容器内使用 任意 markdown 语法。
- 示例
    输入：

   ```md
   :::: steps
      1. 步骤 1

         ```ts
         console.log('Hello World!')
         ```

      2. 步骤 2

         这里是步骤 2 的相关内容

      3. 步骤 3

         ::: tip
         提示容器
         :::

      4. 结束
   ::::
   ```

   输出：

:::: steps

 1. 步骤 1

   ```ts
     console.log('Hello World!')
   ```

 2. 步骤 2

   这里是步骤 2 的相关内容

 3. 步骤 3

   ::: tip
    提示容器
   :::

 4. 结束
 ::::


### 字段容器
- 启用  
  在`.vuepress/config.ts`文件于`markdown`位置配置`field: true`
- 示例
  输入:  
   ```
   :::: field-group

      ::: field name="required" type="required" required default="默认值"
      字段描述信息
      :::

      ::: field name="optional" type="optional" optional default="true"
      <Badge type="tip" text="v1.0.0 新增"  />
      字段描述信息
      :::

      ::: field name="deprecated" type="deprecated" deprecated
      <Badge type="danger" text="v0.9.0 弃用"  />
      字段描述信息
      :::

      ::: field name="default" type="default" default="''"
      字段描述信息
      :::
   ::::
   ```


### 示例容器
- 配置
  - `title="xxx"`：标题
  - `no-padding`：不添加内边距
  - `img`: 仅包含图片时使用
  - `height="xxx"`: 高度
- 代码示例
  - 仅包含图片:

      ```md
      ::: demo-wrapper img no-padding
      ![hero](/plume.svg)
      :::
      ```

      **输出：**
      ::: demo-wrapper img no-padding
      ![hero](/plume.svg)
      :::
   - 包含 markdown 语法：

      ```md
      ::: demo-wrapper title="标题"
      ### 三级标题

      这是示例容器中的内容。
      :::
      ```

      **输出：**
      ::: demo-wrapper title="标题"

      ### 三级标题

      这是示例容器中的内容。
      :::
   - 包含 html /vue 代码：

      ```md
      ::: demo-wrapper
      <h1 class="your-demo-title">这是标题</h1>
      <p class="your-demo-paragraph">这是段落</p>

      <style>
      .your-demo-title {
         color: red;
      }
      .your-demo-paragraph {
         color: blue;
      }
      </style>
      :::
      ```

      **输出：**
      ::: demo-wrapper

      <h1 class="your-demo-title">这是标题</h1>
      <p class="your-demo-paragraph">这是段落</p>

      <style>
      .your-demo-title {
         color: red !important;
      }
      .your-demo-paragraph {
         color: blue !important;
      }
      </style>

      :::


### 文件树
- 配置 
  在`.vuepress/config.ts`文件于`markdown`位置 `配置 icon: 'simple', // 'simple' | 'colored'` 修改默认类型为普通或多彩
  以下语法可用于自定义文件树的外观：
    - 通过加粗文件名或目录名来突出显示，例如 `**README.md**`
    - 通过在名称后添加更多文本来为文件或目录添加注释
    - 通过在名称前添加 `++` 或 `--` 来标记文件或目录为 **新增** 或 **删除**
    - 使用 `...` 或 `…` 作为名称来添加占位符文件和目录。
    - 在 `:::file-tree` 后添加 `icon="simple"` 或 添加 `icon="colored"` 可以切换为简单图标或彩色图标，默认为彩色图标。
    - 在 `:::file-tree` 后添加 `title="xxxx"` 可以为文件树添加标题。
- 示例 
  **输入：**

   ```md /++/ /--/
   ::: file-tree

   - docs
   - .vuepress
      - ++ config.ts
   - -- page1.md
   - README.md
   - theme  一个 **主题** 目录
   - client
      - components
         - **Navbar.vue**
      - composables
         - useNavbar.ts
      - styles
         - navbar.css
      - config.ts
   - node/
   - package.json
   - pnpm-lock.yaml
   - .gitignore
   - README.md
   - …
   :::
   ```

   **输出：**

   ::: file-tree

   - docs
   - .vuepress
      - ++ config.ts
   - -- page1.md
   - README.md
   - theme  一个 **主题** 目录
   - client
      - components
         - **Navbar.vue**
      - composables
         - useNavbar.ts
      - styles
         - navbar.css
      - config.ts
   - node/
   - package.json
   - pnpm-lock.yaml
   - .gitignore
   - README.md
   - …
   :::


### 代码树
- 启用  
   在`.vuepress/config.ts`文件于`markdown`位置 `codeTree: true` 
- 配置
   使用 `::: code-tree` 容器包裹多个代码块。  

   - 在 `::: code-tree` 后使用 `title="Project Name"` 声明代码树的标题  
   - 在 `::: code-tree` 后使用 `height="400px"` 声明代码树的高度  
   - 在 `::: code-tree` 后使用 `entry="filepath"` 声明默认展开的文件路径  
   - 在代码块 <code>\`\`\` lang</code> 后使用 `title="filepath"` 声明当前代码块的文件路径  
   - 如果在 `::: code-tree` 未声明 `entry="filepath"`，可以在代码块 <code>\`\`\` lang</code> 后使用 `:active` 声明当前代码块为展开状态
   - 如果未指定展开的文件路径，默认展开第一个文件  
- 代码示例
   **输入：**

   ````md :collapsed-lines
   ::: code-tree title="Vue App" height="400px" entry="src/main.ts"
   ```vue title="src/components/HelloWorld.vue"
   <template>
   <div class="hello">
      <h1>Hello World</h1>
   </div>
   </template>
   ```

   ```vue title="src/App.vue"
   <template>
   <div id="app">
      <h3>vuepress-theme-plume</h3>
      <HelloWorld />
   </div>
   </template>
   ```

   ```ts title="src/main.ts"
   import { createApp } from 'vue'
   import App from './App.vue'

   createApp(App).mount('#app')
   ```

   ```json title="package.json"
   {
   "name": "Vue App",
   "scripts": {
      "dev": "vite"
   }
   }
   ```
   :::
   ````

   **输出：**

   ::: code-tree title="Vue App" height="400px" entry="src/main.ts"

   ```vue title="src/components/HelloWorld.vue"
   <template>
   <div class="hello">
      <h1>Hello World</h1>
   </div>
   </template>
   ```

   ```vue title="src/App.vue"
   <template>
   <div id="app">
      <h3>vuepress-theme-plume</h3>
      <HelloWorld />
   </div>
   </template>
   ```

   ```ts title="src/main.ts"
   import { createApp } from 'vue'
   import App from './App.vue'

   createApp(App).mount('#app')
   ```

   ```json title="package.json"
   {
   "name": "Vue App",
   "scripts": {
      "dev": "vite"
   }
   }
   ```

   :::




















