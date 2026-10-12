# guiju-style-skill

`guiju-style` 根据一句日常吐槽生成“规矩体”调侃文案：用一本正经的歪理、固定收尾和反差感回应原句。

## 使用

在 Codex 中输入 `$guiju-style`，再附上原句，例如：

```text
$guiju-style 我说今天早点睡，结果又刷手机到两点
```

## 安装到 Codex

在仓库根目录运行以下命令。`mkdir` 会在目标目录已存在时失败，因此不会覆盖已有 Skill：

```sh
set -e
target="${CODEX_HOME:-$HOME/.codex}/skills/guiju-style"
mkdir -p "${target%/*}"
mkdir "$target"
cp -R skills/guiju-style/. "$target/"
```

安装后可在 Codex 下一轮对话中调用 `$guiju-style`。

## 仓库结构

```text
AGENTS.md
.gitignore
LICENSE
README.md
skills/
└── guiju-style/
    └── SKILL.md
```

## 来源与说明

原始指令由用户提供，编写时有豆包协助；`skills/guiju-style/SKILL.md` 原样收录。原文宣称“七组问答”，但模板实际包含四组问答和两句收尾；本版本原样收录，使用时可按示例理解结构；数量表述待作者统一。

本项目采用 MIT License，版权标注为 2026 aweiht，详见 [LICENSE](LICENSE)。
