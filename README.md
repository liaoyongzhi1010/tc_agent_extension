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

1.打开 VS Code,按Ctrl+Shift+P(Windows/Linux)或Cmd+Shift+P(苹果)，打开命令面板。
2.在命令面板的输入框里，直接 打开输入设置(JSON)
3.在下拉列表中，选择首选项:打开用户设置(JSON)这一项，回车即可打开settings.json文件。

<img width="1190" height="798" alt="ed22097bcd41d72422a1fa2ba02c5317" src="https://github.com/user-attachments/assets/1997313d-e874-4b92-a4b0-6fe8525158e5" />
4.把"tcAgent.backendUrl":"http://43.137.51.37:6101”这一行添加进去，保存文件就完成配置了。

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
