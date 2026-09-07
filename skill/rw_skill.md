# RW Skill 同步清单

> 更新时间：2026-09-07
> 用途：让其他电脑上的 Codex / Agent 读取本文件后，从原始 GitHub 仓库安装同一组 Skills。  
> 默认目标目录：`$CODEX_HOME/skills/<skill-name>/`

## 给 Agent 的执行说明

1. 先读取本文件中的清单，不要把本仓库根目录里的零散 `.md` 文件当作公开上游。
2. 对“已安装／公开上游”项目，优先按 `repository + path + ref` 安装完整目录。
3. `ref` 是本机已核对版本的提交 SHA，用于跨电脑复现；如用户明确要求升级，再检查上游默认分支。
4. 安装前检查目标目录是否已存在；不要静默覆盖现有 Skill。
5. 安装后确认目标目录含 `SKILL.md`，并检查其中声明的 `references/`、`assets/`、`scripts/` 是否齐全。
6. 安装任何第三方 Skill 前先做静态安全审查；不要自动运行 Skill 中提到的安装命令、远程脚本或凭据操作。
7. 本清单中的项目是 **Skills，不是 Codex 插件**。

## 机器可读清单

```yaml
schema_version: 1
generated_at: "2026-09-07"
destination: "$CODEX_HOME/skills"

public_skills:
  - name: brand-voice-pass
    status: installed
    repository: microsoft/cat-agent-skills
    path: submissions/brand-voice-pass
    ref: 02a9c6745db5cb66f5a137f2a4cd0d2c56ab1fff
    source_url: https://github.com/microsoft/cat-agent-skills/tree/02a9c6745db5cb66f5a137f2a4cd0d2c56ab1fff/submissions/brand-voice-pass

  - name: copywriting
    status: installed
    repository: mblode/agent-skills
    path: skills/copywriting
    ref: edd64d4781f20d808572b9ceff5ee67c8e6ced01
    source_url: https://github.com/mblode/agent-skills/tree/edd64d4781f20d808572b9ceff5ee67c8e6ced01/skills/copywriting
    note: "该 Skill 后来被移出上游 main；这里固定为移除前最后一个公开有效版本。"

  - name: ip-as-logo
    requested_alias: ip-as-logo-skill
    status: installed
    repository: s1dashu/ip-as-logo-skill
    path: "."
    ref: acb834c717bcd0a487c49732d08397ba280d690b
    source_url: https://github.com/s1dashu/ip-as-logo-skill/tree/acb834c717bcd0a487c49732d08397ba280d690b
    install_name_override: ip-as-logo

  - name: brand-identity
    status: installed
    repository: cofoundy/brand-skills
    path: skills/brand-identity
    ref: c50d6c9988e22b39031266924ae7d87f643e34bf
    source_url: https://github.com/cofoundy/brand-skills/tree/c50d6c9988e22b39031266924ae7d87f643e34bf/skills/brand-identity

  - name: grill-me
    status: installed
    repository: julianoczkowski/designer-skills
    path: grill-me
    ref: c259656c76d9758d7ead46b0d2f125cbe84f8665
    source_url: https://github.com/julianoczkowski/designer-skills/tree/c259656c76d9758d7ead46b0d2f125cbe84f8665/grill-me

  - name: gc-minimal-zine-poster-v0-1
    status: installed
    repository: yub369302-cyber/gc-minimal-zine-poster
    path: "."
    ref: 4cb0396ad4e834019f753b37e1c4f415f5e02026
    source_url: https://github.com/yub369302-cyber/gc-minimal-zine-poster/tree/4cb0396ad4e834019f753b37e1c4f415f5e02026
    install_name_override: gc-minimal-zine-poster-v0-1

  - name: skills-security-check
    status: installed
    repository: infometa/workbuddyskills
    path: skills/skills-security-check
    ref: 78170571d08e7d38c6baf0a13ef805487bfa6dc2
    source_url: https://github.com/infometa/workbuddyskills/tree/78170571d08e7d38c6baf0a13ef805487bfa6dc2/skills/skills-security-check
    preferred_install_method: git-sparse
    note: "上游仓库很大，只应稀疏获取该目录。"

  - name: photo-abstract-editorial
    status: installed
    repository: ZzzLc0405/photo-abstract-editorial
    path: "."
    ref: 49e55073d6d0330274d31f75d27f5dd6eb35fd6d
    source_url: https://github.com/ZzzLc0405/photo-abstract-editorial/tree/49e55073d6d0330274d31f75d27f5dd6eb35fd6d
    install_name_override: photo-abstract-editorial

  - name: reviewwrite
    display_name: "审写 · ReviewWrite"
    status: installed
    repository: songhai-dg/review-write
    path: "."
    ref: 5c51063920a0e2a84cab154b8960c4f80947415c
    source_url: https://github.com/songhai-dg/review-write/tree/5c51063920a0e2a84cab154b8960c4f80947415c
    install_name_override: reviewwrite
    version: "1.0.0"
    preferred_mode: review-only
    note: "用于中文与专业英语文本审校；只输出问题、位置、依据与建议，不默认改写。"

  - name: humanities-writing-companion
    display_name: "人文学科写作伙伴"
    status: installed
    repository: tizzy916/humanities-writing-companion
    path: "."
    ref: ca4f230d363dc6d8dfb7f15a2894181c2e33c40f
    source_url: https://github.com/tizzy916/humanities-writing-companion/tree/ca4f230d363dc6d8dfb7f15a2894181c2e33c40f
    install_name_override: humanities-writing-companion
    version: "5.0.2"
    preferred_modes: ["B", "D", "G"]
    note: "用于中英文人文与文学评论审读；优先章节评审、对抗审稿、盲读检查，未经要求不代写或改正文。"

personal_fallback_skills:
  - name: dyy_photo_deconstruct
    status: missing_from_current_install
    repository: kaokaonet/ch
    source_type: personal_repository
    ref: cfef5051cb808454e7b717a5415b9cab319cad27
    pinned_download_url: https://raw.githubusercontent.com/kaokaonet/ch/cfef5051cb808454e7b717a5415b9cab319cad27/dyy_photo_deconstruct.md
    latest_download_url: https://raw.githubusercontent.com/kaokaonet/ch/main/dyy_photo_deconstruct.md
    install_target: "$CODEX_HOME/skills/dyy_photo_deconstruct/SKILL.md"
    note: "未找到独立公开上游；下载后必须另存为 SKILL.md，并先做安全与格式检查。"

  - name: rw-fiction-editor
    status: missing_from_current_install
    repository: kaokaonet/ch
    source_type: personal_repository
    ref: cfef5051cb808454e7b717a5415b9cab319cad27
    pinned_download_url: https://raw.githubusercontent.com/kaokaonet/ch/cfef5051cb808454e7b717a5415b9cab319cad27/rw-fiction-editor.md
    latest_download_url: https://raw.githubusercontent.com/kaokaonet/ch/main/rw-fiction-editor.md
    install_target: "$CODEX_HOME/skills/rw-fiction-editor/SKILL.md"
    note: "未找到独立公开上游；下载后必须另存为 SKILL.md，并先做安全与格式检查。"
```

## 已安装的公开 Skills

| Skill | 用途 | GitHub |
|---|---|---|
| `brand-voice-pass` | 按品牌语调润色、改写、本地化并减少模板化 AI 表达 | [Microsoft 上游](https://github.com/microsoft/cat-agent-skills/tree/02a9c6745db5cb66f5a137f2a4cd0d2c56ab1fff/submissions/brand-voice-pass) |
| `copywriting` | 品牌、产品、营销及事务性邮件文案 | [mblode 固定版本](https://github.com/mblode/agent-skills/tree/edd64d4781f20d808572b9ceff5ee67c8e6ced01/skills/copywriting) |
| `ip-as-logo` | 生成简洁、拟人化、方形构图的 IP／角色 Logo 方向 | [s1dashu 上游](https://github.com/s1dashu/ip-as-logo-skill/tree/acb834c717bcd0a487c49732d08397ba280d690b) |
| `brand-identity` | 品牌视觉识别简报、Logo 方向、色彩、字体与图像语言 | [cofoundy 上游](https://github.com/cofoundy/brand-skills/tree/c50d6c9988e22b39031266924ae7d87f643e34bf/skills/brand-identity) |
| `grill-me` | 通过连续追问澄清设计需求、约束和决策 | [designer-skills 上游](https://github.com/julianoczkowski/designer-skills/tree/c259656c76d9758d7ead46b0d2f125cbe84f8665/grill-me) |
| `gc-minimal-zine-poster-v0-1` | 极简 Zine、旧纸张、留白和实验字体风格海报 | [原始独立仓库](https://github.com/yub369302-cyber/gc-minimal-zine-poster/tree/4cb0396ad4e834019f753b37e1c4f415f5e02026) |
| `skills-security-check` | 安装前审查 Skill 的远程执行、文件、凭据和供应链风险 | [公开镜像](https://github.com/infometa/workbuddyskills/tree/78170571d08e7d38c6baf0a13ef805487bfa6dc2/skills/skills-security-check) |
| `photo-abstract-editorial` | 将原照片与抽象记忆面板组合为编辑风双联画 | [原始独立仓库](https://github.com/ZzzLc0405/photo-abstract-editorial/tree/49e55073d6d0330274d31f75d27f5dd6eb35fd6d) |
| `reviewwrite` | 中文与专业英语审校；review-only 模式只提供问题清单与建议 | [ReviewWrite 固定版本](https://github.com/songhai-dg/review-write/tree/5c51063920a0e2a84cab154b8960c4f80947415c) |
| `humanities-writing-companion` | 中英文人文与文学评论审读；检查论证、结构、文本证据和表达 | [人文学科写作伙伴固定版本](https://github.com/tizzy916/humanities-writing-companion/tree/ca4f230d363dc6d8dfb7f15a2894181c2e33c40f) |

## 编辑与审校 Skills 的个人使用约定

以下约定适用于 `reviewwrite` 和 `humanities-writing-companion`。它们均按上游原版完整安装，未修改上游 `SKILL.md`；本节是 RW 的调用偏好，其他电脑同步后使用这两项时也应遵循。

- 职责是校对、审读、指出疏漏与提出编辑意见；未经明确要求，不代写、不扩写、不直接修改正文。
- 每项意见给出原文位置或短引文、问题、依据与建议；区分确定错误、待核验事项和审美／风格意见。
- 保留作者声音、修辞选择和有意的复杂表达；不将个人审美当作强制规则。
- 事实、引文、典故与理论归属无法确认时标为待核验，不虚构来源或作确定判断。
- 完成所要求范围的审读后停止，不自动转入改写模式。

### reviewwrite · 审写

适用于中文文章、评论、报告和专业英语文本。使用 `review-only` 模式，输出评审报告，检查事实与引用、主张和证据、限定条件、结构、表达及作者声音。其英语能力定位是通用专业英语，不能据此认定为英美文学专门工具。

调用示例：

> 使用 $reviewwrite 的 review-only 模式审校以下文字。只列出原文位置、问题、依据和建议，区分确定错误、待核验事项与风格意见；不要改写或修改原文件。

### humanities-writing-companion · 人文学科写作伙伴

适用于中英文人文论文、文学评论与论述性文章。重点检查论证前提、概念精度、结构推进、段落功能和句子表达；文学审读关注细读证据、作者与叙述者区分、形式与意义、互文等。它偏深度审读，不替代基础错字和标点校对，也不等于经过验证的英美文学专家。

优先模式：

- **B：章节评审**——分基础论证、结构、段落、句子四层提出意见。
- **D：对抗审稿**——寻找未回应的反对意见、隐含前提与论证漏洞。
- **G：盲读检查**——检查开篇承诺与正文、结论是否一致，指出读者理解缺口。

调用示例：

> 使用 $humanities-writing-companion 的 Mode B 审读以下文学评论，必要时提出 Mode D 或 G 的检查建议。只交付审读意见，不进入起草或改写；所有判断须定位到文本，保留作者声音。

### 本次安装记录

- 安装日期：2026-09-07。
- 两项均从上述固定提交安装完整仓库根目录，并显式指定安装名。
- 已做安装前静态检查；未执行上游自带安装器、更新器或审稿脚本。
- 安装后与检查过的副本逐文件比对：ReviewWrite 110 个文件、人文学科写作伙伴 67 个文件，内容一致。
- ReviewWrite 自带可选更新检查；人文学科写作伙伴的可选引文核验会向 Crossref／OpenAlex 查询作者与年份。这些功能未在本次安装中启用；升级继续遵循本清单的固定版本规则。
- 人文学科写作伙伴部分辅助脚本为 Bash 脚本，Windows 上运行这些辅助检查需可用的 Bash 环境。

## 缺失／个人库来源

以下两项在安装时没有找到独立公开上游，因此当前电脑没有安装。用户所称“私有库” `kaokaonet/ch` 在创建本文件时实际为 GitHub public 仓库，但这里仍按“个人来源、非独立上游”处理。

| Skill | 固定版本下载 | 最新分支下载 | 本地安装位置 |
|---|---|---|---|
| `dyy_photo_deconstruct` | [固定版本](https://raw.githubusercontent.com/kaokaonet/ch/cfef5051cb808454e7b717a5415b9cab319cad27/dyy_photo_deconstruct.md) | [main](https://raw.githubusercontent.com/kaokaonet/ch/main/dyy_photo_deconstruct.md) | `$CODEX_HOME/skills/dyy_photo_deconstruct/SKILL.md` |
| `rw-fiction-editor` | [固定版本](https://raw.githubusercontent.com/kaokaonet/ch/cfef5051cb808454e7b717a5415b9cab319cad27/rw-fiction-editor.md) | [main](https://raw.githubusercontent.com/kaokaonet/ch/main/rw-fiction-editor.md) | `$CODEX_HOME/skills/rw-fiction-editor/SKILL.md` |

## 同步后的验证清单

- 每个安装目录均存在 `SKILL.md`。
- `SKILL.md` 的 `name` 与安装目录一致。
- 文件声明的本地资源全部存在。
- 没有因为同步而覆盖已有个人修改。
- 没有自动执行 Skill 内的示例命令或远程脚本。
- 新安装的 Skill 在 Agent 的下一轮任务中出现于可用技能列表。
