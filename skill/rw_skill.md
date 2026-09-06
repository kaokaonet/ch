# RW Skill 同步清单

> 更新时间：2026-09-06  
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
generated_at: "2026-09-06"
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
