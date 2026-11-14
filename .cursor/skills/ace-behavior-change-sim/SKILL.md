---
name: ace-behavior-change-sim
description: Run dual-agent ACE fitness behavior-change roleplay with a stage-accurate client and a hidden evaluator scoring TTM processes of change, decisional balance, self-efficacy, and ACE ABC. Use when the user wants ACE 行为改变模拟, TTM/MI coaching practice, 无意向期客户, 健身咨询角色扮演, or to create 客户 and 评价官 subagents.
---

# ACE 行为改变双角色模拟

用两个独立 subagent：客户只演戏，评价官只旁观。不要自己兼演两角，除非 Task/resume 失败。

## 何时启动

用户要练习 ACE 咨询、创建无意向期/意向期客户、或说「开始模拟 / 结束模拟」。先读：

- [ace-reference.md](ace-reference.md)
- [client-prompt.md](client-prompt.md)
- [evaluator-prompt.md](evaluator-prompt.md)

## 开场

1. 未指定人设时，用默认：35 岁久坐女性、无意向期、办卡只坚持两周、家人希望她练但不是她的目标、潜在价值是陪家人和腰酸。
2. 用 Task、`generalPurpose`、`inherit` **并行**启动客户与评价官。把对应 prompt 全文填入，替换占位符。
3. 只展示客户开场白。评价官就绪信息不展示。
4. 记住两个 agent ID，后续 `resume`。

## 每一轮

用户以教练身份说话后：

1. 先 resume 客户：只给本轮教练原话，令其输出 1–3 句客户回应。
2. 再 resume 评价官：同时给教练原话和客户回应。
3. 对用户展示：

```markdown
**客户：**
「……」

**评价官：**
- **阶段：**
- **策略+过程：**
- **ABC：**
- **决策平衡：**
- **自我效能：**
- **客户状态：**
- **依据：**
- **建议：**
```

4. 不要把评价官内容发给客户。不要替用户写下一句教练台词，除非用户明确要求示范。

## Resume 失败

若模型不可用导致无法 resume：用完整逐字稿重建两个 agent，再继续。不要静默自己扮演。

## 结束

用户说「结束模拟」时，resume 两者做复盘。展示：总分、最终阶段、是否移动、优缺点引用、3 句可直接用的替代表达、下一场只改一个习惯。客户退出角色后可附 2–4 句主观感受。

## 阶段匹配红线

无意向期禁止把 Collaborate、训练菜单、准备度邀请当成成功策略。意识唤醒必须用问题，不能用说教讲好处。完整对照见 [ace-reference.md](ace-reference.md)。
