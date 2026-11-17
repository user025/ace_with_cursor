# ACE with Cursor

用 Cursor Agent Skill 练习 ACE（American Council on Exercise）行为改变咨询。

| 目录 | 给谁用 | 用户扮演 |
|---|---|---|
| [coach/](coach/README.md) | 教练 | 教练，对模拟客户说话 |
| [trainer/](trainer/README.md) | 训练者（来访者） | 训练者，接受模拟教练 |

对话导出原文见 `cursor_ace.md`（只读，不改）。

项目内 Cursor 会通过 `.cursor/skills/` 里的符号链接加载 `coach/` 下的 skill。个人安装可把对应 skill 目录复制到 `~/.cursor/skills/`。
