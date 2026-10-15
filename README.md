# Human-Pet Interaction

用于为地毯搭配北美住宅中的人宠互动场景。提供地毯图片和场景要求后，skill 会生成可直接用于图像生成的英文提示词；明确要求生成图片时，也可在具备图像生成能力的环境中出图。

## 能做什么

- 从参考地毯提取风格和整体色调，为客厅、厨房、卧室、餐厅、走廊等空间安排合理的地毯位置、家具与摆件；不要求复制地毯的具体图案。
- 设计人物的自然面部特征、季节适宜的服装，以及人物和宠物之间有接触、有回应的互动。未指定宠物时，会根据场景选取合适的宠物。
- 使用内置动作索引和宠物种类资料，让互动方式与宠物选择保持变化；在连续场景中避免重复使用相同的人脸、服装与家具方案。
- 将人物、互动、空间、镜头和光线组织成一段可复制的提示词；默认用英文输出。

## 安装

将本仓库的完整文件夹放入 Codex 的 skills 目录，并确保 `SKILL.md` 位于该文件夹根目录。例如：

```text
~/.codex/skills/north-american-rug-human-pet-scenes/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── ...
```

仓库中的 `references/` 是 skill 的组成部分，请与 `SKILL.md` 一起保留。私有仓库的克隆或下载需要相应 GitHub 访问权限。

## 使用示例

附上地毯图片，然后输入：

> 自然仿生风格，年轻白人女性，客厅，坐在沙发上与金毛玩耍，30 度略微俯视拍摄，展示较为完整的地毯，夏季。请输出提示词。

如需直接生成场景图，将最后一句改为“请生成图片”。也可以指定宠物种类、人数、服装正式程度、互动动作、画幅和地毯展示比例。

## 文件说明

- [`SKILL.md`](SKILL.md)：场景构建、人物与宠物、家具、镜头及最终提示词的核心规则。
- [`references/character-and-clothing.md`](references/character-and-clothing.md)：人物面部真实性、差异化选角与服装搭配。
- [`references/interaction-action-index.md`](references/interaction-action-index.md)：按姿态和活动检索人宠互动动作。
- [`references/pet-type-library.md`](references/pet-type-library.md)：宠物类型与适配的互动线索。
- `references/interaction-folder-*.md`、`references/interaction-pdf-images.md`：从参考场景提炼的文字动作记录；原始参考图片未包含在仓库中。

本仓库目前为私有仓库；README 仅说明使用方式，具体执行规则以 `SKILL.md` 为准。
