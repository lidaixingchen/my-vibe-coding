# My Vibe Coding

个人项目集合，使用 Git Submodules 管理多个独立项目。

## 包含的项目

- [todo-app](./todo-app) - 待办事项应用（Vue 3 + TypeScript + Vite + Pinia + Tailwind CSS）

## 使用方式

### 克隆仓库（含所有子模块）

```bash
git clone --recurse-submodules https://github.com/lidaixingchen/my-vibe-coding.git
```

### 添加子项目

```bash
git submodule add <仓库地址> <目录名>
```

### 更新所有子模块

```bash
git submodule update --remote
```

### 初始化子模块（已克隆但未初始化）

```bash
git submodule update --init --recursive
```