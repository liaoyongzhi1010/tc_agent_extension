# TC Agent 前端扩展（VS Code）

该仓库仅包含 **TC Agent** 的 VS Code 前端扩展（UI/客户端逻辑），后端服务需单独部署。

## 依赖

- Node.js 18+
- VS Code 1.85+
- 已运行的 TC Agent 后端

## 安装与编译

```bash
npm install
npm run compile
```

在 VS Code 中打开本目录，按 **F5** 启动扩展开发宿主进行调试。

## 后端地址配置

方式 A：打开 VS Code 设置（`Ctrl+,`）→ 搜索 `TC Agent Backend Url` → 填写后端地址。  
方式 B：打开“设置 (JSON)”并添加以下配置：

```json
{
  "tcAgent.backendUrl": "http://43.137.51.37:6101"
}
```

> 如果后端在本机，填写 `http://127.0.0.1:8765`。修改后建议执行一次 **Reload Window**。

## Ask 与 Agent 如何选择

- **Ask**：概念解释、接口用法、快速问答、只需要答案不改代码  
- **Agent**：需要生成/修改代码、运行工具/编译/执行、跨多步落地任务  
- 不确定时先用 Ask，若需要“产出代码或执行任务”再切 Agent

## 说明

- 本仓库不包含后端。
- API Key 在后端配置，不在本扩展中配置。
