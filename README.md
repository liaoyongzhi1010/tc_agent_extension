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

在 VS Code 设置中填写：

```json
{
  "tcAgent.backendUrl": "http://43.137.51.37:6101"
}
```

## 说明

- 本仓库不包含后端。
- API Key 在后端配置，不在本扩展中配置。
