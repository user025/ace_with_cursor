# 教练 Skills

给健身教练、ACE 考生、咨询练习者。用户扮演**教练**，agent 扮演客户与评价官。

目标不是当场把人劝去训练，而是按 TTM 阶段匹配改变过程，推动决策平衡和自我效能。

## 已上线

### ace-behavior-change-sim

双角色 ACE 行为改变模拟。

- **触发：** 「开始模拟」「无意向期客户」「ACE 行为改变练习」「结束模拟」
- **结构：** 客户 subagent 只演戏；评价官 subagent 只旁观，内容不回传给客户
- **默认人设：** 35 岁久坐女性、无意向期、办卡只坚持两周、家人希望她练
- **每轮评价：** 阶段、策略+过程（匹配/过早/过晚）、ABC、决策平衡、自我效能、客户状态、依据、建议
- **结束：** 总分、阶段是否移动、优缺点引用、3 句替代表达、下一场只改一个习惯

文件：

- [ace-behavior-change-sim/SKILL.md](ace-behavior-change-sim/SKILL.md) — 开场、resume、复盘流程
- [ace-behavior-change-sim/ace-reference.md](ace-behavior-change-sim/ace-reference.md) — 阶段、10 个改变过程、ABC
- [ace-behavior-change-sim/client-prompt.md](ace-behavior-change-sim/client-prompt.md) — 客户人设与反应规则
- [ace-behavior-change-sim/evaluator-prompt.md](ace-behavior-change-sim/evaluator-prompt.md) — 八项评分与复盘

无意向期红线：不要把 Collaborate、训练菜单、「一起试试」当成成功；意识唤醒用问题，不用说教讲好处。

## 和训练者目录的关系

教练 skill 练「怎么问」。训练者 skill 练「被这样问时，自己处在哪一阶段」。对偶方案见 [../trainer/README.md](../trainer/README.md)。
