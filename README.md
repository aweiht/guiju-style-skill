# guiju-style-skill

`guiju-style` 是一个通用 AI 文案 Skill：把一句日常吐槽改写成“规矩体”调侃，用一本正经的歪理、固定收尾和反差感回应原句。

## 在任何 AI 对话中使用

打开 [Skill 原文](skills/guiju-style/SKILL.md)，把文件里的规则粘贴到任何能接收文本指令的 AI 对话中，然后再发送你想回应的原句：

```text
健身卡办了一个月，去了三次，最近开始研究怎么转卡
```

更多完整场景见[案例集](examples.md)。

## 在支持 Skill 的工具中使用

支持加载 Skill 或指令文件的工具，可以按各自的方式加载 `SKILL.md`。支持 `$name` 调用语法的工具也可以用 `$guiju-style` 调用；例如 Codex 支持在对话中输入 `$guiju-style`，再附上原句。

## 可选：安装到 Codex

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
examples.md
skills/
└── guiju-style/
    └── SKILL.md
```

## 来源与说明

原始指令由用户提供，编写时有豆包协助；`skills/guiju-style/SKILL.md` 原样收录。原文宣称“七组问答”，但模板实际包含四组问答和两句收尾；本版本原样收录，使用时可按示例理解结构；数量表述待作者统一。

本项目采用 MIT License，版权标注为 2026 aweiht，详见 [LICENSE](LICENSE)。
