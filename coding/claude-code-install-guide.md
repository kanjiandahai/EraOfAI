# Claude Code CLI 安装指南

## 系统要求
- macOS 10.15+ 或 Linux
- Node.js 18+ 
- Git

## 安装步骤

### 1. 安装 Node.js
```bash
# macOS 使用 Homebrew
brew install node

# Ubuntu/Debian
sudo apt update
sudo apt install nodejs npm

# 验证安装
node --version  # 应显示 v18 或更高
npm --version
```

### 2. 安装 Claude Code
```bash
npm install -g @anthropic-ai/claude-code
```

### 3. 验证安装
```bash
claude --version
```

### 4. 首次配置
```bash

# 使用环境变量
export ANTHROPIC_API_KEY=your_api_key_here
```

## 获取 API Key

1. 访问 [Anthropic Console](https://console.anthropic.com/)
2. 创建 API key
3. 在配置时输入或使用环境变量设置

## 常用命令

```bash
# 启动交互模式
claude

# 执行具体任务
claude "explain this codebase"

# 查看帮助
claude --help
```

## 故障排除

### 权限问题
```bash
# macOS/Linux 权限修复
sudo chown -R $(whoami) $(npm config get prefix)/{lib/node_modules,bin,share}
```

### 网络问题
```bash
# 设置代理（如需要）
export HTTPS_PROXY=http://proxy.company.com:8080
```

## 更新
```bash
npm update -g @anthropic-ai/claude-code
```

## 卸载
```bash
npm uninstall -g @anthropic-ai/claude-code
```