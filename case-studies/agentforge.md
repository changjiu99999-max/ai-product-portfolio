# AgentForge

**Agent Runtime & Evaluation Platform**

[返回作品集](../README.md)

## 产品问题

复杂 Agent 长任务会跨越工具、进程、状态与上下文。只看最终答案，无法判断执行权是否唯一、未知动作能否重试、恢复是否尊重历史事实。AgentForge 将这些风险转成可验证的平台契约。

## 产品设计

- **受控执行**：计划和工具声明必须经过身份、权限、预算与执行边界校验。
- **状态与恢复**：依据已提交事实决定 retry、resume 或停止，不把未知状态默认为成功。
- **信息治理**：区分上下文与记忆的来源、时效、信任及预算。
- **评估与证据**：分别定义场景合同满足、任务完成、工具执行与恢复的分母，保留失败和安全拒绝。

## 工程证据

Core Platform v0.1 的冻结 Benchmark 包含 **48 个场景**。2026-09-10 冻结安全回归与 2026-09-18 公开候选回归分别有 **894 个独立测试，894/894 PASS，零 failure/error/skip**；两批结果相互核对，不叠加为新的测试规模。

Benchmark 使用确定性 harness；正确拒绝可以满足场景合同。48 场景与 894 项测试都不代表真实模型质量、生产 SLO 或外部采用。

## 与 FactoryPilot 的关系

FactoryPilot 展示面向质量工程师的应用产品；AgentForge 展示面向 Agent 工程与平台团队的基础设施产品。两者的指标、用户和验证范围分别解释，不相互代用。

[公开工程仓库与完整证据](https://github.com/changjiu99999-max/agentforge) · [Product First README](https://github.com/changjiu99999-max/agentforge/blob/main/README.md)
