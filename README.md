# 瓦猫写作私教（zhihu-writing-coach）

一个网文写作教练 Skill。用大白话教人物塑造、反派设计、开篇节奏和写作底层逻辑，适合新人作者入门，也适合迷茫期作者回炉。

这个 Skill 不讲平台运营、算法、日收数据——那是执行层的事。它只解决一个问题：**你写的东西为什么不行，以及怎么练。**

## 它能帮你什么

- **人物塑造**：标签化收集、缺点驱动、记忆点设计、行为理由、争议点
- **反派设计**：五段位分级、闪光点、理想、偏执、记忆点
- **开篇与节奏**：流水账诊断、核心重点、连环转折、串珠子节奏、代入感五法
- **写作底层逻辑**：自我认知、受众需求、市场定位、创作框架、练习方法
- **起名与创作框架**：七路起名法、从定位到开篇的完整流程

## 怎么触发

装好之后，直接说人话就行，比如：

- 我写的人物总是很扁平，怎么让他活起来？
- 我开篇写了几千字，读者说像流水账，怎么办？
- 我反派怎么写才不会千篇一律？
- 新人写网文从哪下手，一点头绪都没有。
- 小说人物的名字怎么起才不土？

## 安装

### WorkBuddy / CodeBuddy

把整个目录拷到 skills 目录下：

```bash
cp -r zhihu-writing-coach ~/.workbuddy/skills/
```

Windows 也可以用目录联接，指向本仓库的克隆位置（改一处两边生效）。
在 **PowerShell** 里执行，把 `<本仓库路径>` 换成实际路径：

```powershell
New-Item -ItemType Junction `
  -Path "$env:USERPROFILE\.workbuddy\skills\zhihu-writing-coach" `
  -Target "<本仓库路径>"
```

> 注意：目录名要和 `SKILL.md` 里的 `name` 字段保持一致（都是 `zhihu-writing-coach`），否则部分 Agent 会识别不到。

### 其他支持 Skill 的 Agent

`SKILL.md` 是标准格式（YAML frontmatter + Markdown）。把目录放到对应 agent 的 skills 路径下即可，`references/` 会被自动按需加载。

## 目录结构

```
zhihu-writing-coach/
├── SKILL.md                      # 技能定义：身份、知识调用规则、教学方法、输出风格
├── references/                   # 知识库，提问时按需读取
│   ├── characters.md             # 人物塑造
│   ├── villains.md               # 反派设计
│   ├── pacing.md                 # 开篇、节奏与代入感
│   ├── fundamentals.md           # 写作底层逻辑与练习方法
│   └── framework.md              # 起名、创作框架
├── assets/
│   └── avatar.png                # 头像（备份用，Skill 不加载）
├── LICENSE
└── README.md
```

## 工作原理

`SKILL.md` 里写死了**知识调用规则**：用户问到哪一类问题，先读对应的 `references/` 文件，再结合问题回答；不允许凭记忆编造具体例子和方法。

这么做是为了避免模型一本正经地胡说——教学里的每个范例、每套方法都来自知识文件，不是现编的。

## 知识来源与版权

内容整理自知乎作者**瓦猫**的 13 篇网文写作干货文章，保留了核心教学内容（框架、例子、方法论、作业），删除了图片、过渡语和平台推广内容。

- **版权归原作者瓦猫所有**，本项目仅作学习整理，未获原作者授权
- 未经授权请勿用于商业用途
- 如果原作者认为本仓库不妥，请联系删除

具体来源对应关系：

| 文件 | 来源文章 |
|------|----------|
| `characters.md` | 第 2、7、12 篇 |
| `villains.md` | 第 3、13 篇 |
| `pacing.md` | 第 8、11 篇 |
| `fundamentals.md` | 第 1、5、6、9 篇 |
| `framework.md` | 第 4、10 篇 |

## 许可

见 [LICENSE](LICENSE)。
