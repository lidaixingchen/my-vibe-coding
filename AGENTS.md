# AGENTS.md

## 项目概述

个人项目集合仓库，使用 Git Submodules 管理多个独立子项目。



## 常用命令

### Git Submodule 管理

```bash
# 添加新的子模块
git submodule add <仓库URL> <目录名>

# 克隆含子模块的仓库
git clone --recurse-submodules <仓库URL>

# 初始化并拉取所有子模块
git submodule update --init --recursive

# 更新子模块到远程最新
git submodule update --remote

# 查看子模块状态
git submodule status
```

### 代码规范

- 禁止魔法数字和硬编码
- 所有 `mcp_CodeGraph_*` 工具调用必须带 `projectPath` 参数
- 使用项目已有的库和工具，遵循现有代码风格

## 目录结构

```
my-vibe-coding/
├── .gitmodules          Git 子模块配置
├── todo-app/            子模块：待办事项应用
└── README.md
```

## 注意事项

- 子模块 URL 应使用 HTTPS 或 SSH 格式（而非本地绝对路径），以支持团队协作
- 修改子模块后需在父仓库中提交子模块引用的 commit hash