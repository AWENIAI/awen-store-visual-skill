# awen-store-visual-skill

中文商业视觉生成 Skill 包，适合门店营销物料、产品材质精修、电商详情页 10 屏规划、海报分层与 PSD 工作流。

## 适合什么场景

- 门店开业海报
- 门店桌牌 / 立牌 / 展架
- 产品海报 / 新品海报
- 食品、饮品、家居、服饰等产品精修
- 电商详情页信息提取与分页规划
- 海报图层拆分与 PSD 合成规则

## 安装与使用

### 在 Codex 中安装

1. 将整个文件夹放入 Codex 的 Skills 目录。
2. 确保根目录直接包含 `SKILL.md`。
3. 重启或刷新 Codex 后即可使用。

常见路径：

- `~/.codex/skills/awen-store-visual-skill`
- `~/.agents/skills/awen-store-visual-skill`

### 在 Claude 中安装

1. 将整个文件夹放到 Claude 可读取的 Skills 目录。
2. 确保 `SKILL.md` 位于技能根目录。
3. 重新加载 Claude 后，直接用中文描述任务即可。

常见做法：

- 放到 `~/.claude/skills/awen-store-visual-skill`
- 或者放到你当前 Claude 环境约定的 skills 目录

### 在 Antigravity 中安装

1. 将整个文件夹放到 Antigravity 的技能目录。
2. 确保 `SKILL.md` 是入口文件。
3. 重启或刷新技能索引后使用。

常见做法：

- 放到 Antigravity 识别的 skills 目录
- 保持目录结构不变

### 使用方法

直接用中文给最少信息，Skill 会自动路由到对应模板。

```text
场景：门店开业海报
品牌：AWENAI
门店类型：柠檬茶店
比例：4:5
数量：4 张独立海报
```

```text
场景：材质精修
材质：玻璃
输入：产品图
要求：白底商业精修，保留标签和瓶身结构
```

```text
场景：详情页
输入：产品图
目标：提取产品信息，并生成 10 屏 3:4 详情页提示词
```

```text
场景：PSD 分层
输入：海报图
目标：拆分背景、文字、产品、装饰元素，保持位置不变
```

## 文件结构

- `SKILL.md`：主入口，负责任务路由和全局规则
- `prompts/`：各类任务的具体提示词模板
- `rules/`：通用规则和变量规范
- `examples/`：可直接复制的快捷示例
- `assets/cases/`：实际产出展示案例

## 实际产出展示

### 门店海报

![门店产品海报](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/01-store-poster.png)

### 门店桌牌

![门店桌牌](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/02-tablecard.png)

### 海报案例

![海报案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/03-steak-set.png)

## 详情页与信息页案例

![详情页案例 1](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/04-detail-9-10.png)

![产品信息总览](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/05-product-info-overview.png)

![原料页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/06-coffee-ingredients.png)

![烘焙页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/07-coffee-roast.png)

![生活方式页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/08-coffee-lifestyle.png)

![烘焙曲线页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/09-coffee-roast-profile.png)

![冲泡页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/10-coffee-pour.png)

![产品封面页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/11-coffee-product-cover.png)

![杯装页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/12-coffee-cup.png)

![包装细节页案例](/Users/karissa/Documents/New%20project/awen-store-visual-skill/assets/cases/13-package-details.png)

## 输出习惯

- 优先保留用户提供的品牌、产品名、价格、比例和文案
- 不做无根据推测
- 中文主标题、价格和活动信息优先保证可读
- 批量图必须是独立图片，不要拼贴
- PSD 相关任务先输出分层规则，再交给支持 PSD 的工具继续处理

## 常见问题

### 没有图片怎么办？

如果任务不依赖实拍图，可以直接用文字变量生成。

### 信息不全怎么办？

可以先用已有信息生成通用版本，但真实品牌名、价格、成分和活动时间不要乱补。

### 怎么改模板？

优先改 `prompts/` 下对应模板，再同步更新 `examples/`。
