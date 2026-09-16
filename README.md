# OnlineNote

极简纯前端在线文本编辑器，单文件、零依赖、无需服务器。

## 功能

- ✅ 纯前端，单个 HTML 文件即可运行
- ✅ 内容自动保存到浏览器本地（localStorage）
- ✅ 多笔记支持：通过 URL 参数区分不同文件
- ✅ 自动保存，带"保存中 / 已保存"状态提示
- ✅ 实时字数统计
- ✅ 跨标签页同步（同浏览器多标签打开同一笔记自动同步）
- ✅ 零依赖，纯原生 HTML / CSS / JS

## 使用方法

### 本地使用

直接用浏览器打开 `index.html` 即可开始打字。

### URL 参数：多笔记切换

在网址后面加 `?` + 任意参数，即可创建或打开不同的笔记：

| URL | 对应的笔记 |
|-----|----------|
| `index.html` | 默认笔记 |
| `index.html?todo` | 待办清单 |
| `index.html?diary` | 日记 |
| `index.html?work-project1` | 工作 / 项目1 笔记 |
| `index.html?我的读书笔记` | 中文参数也可以 |

每个参数对应一份独立存储的内容，互不干扰。

### 存储说明

所有内容保存在浏览器的 `localStorage` 里，key 格式为 `onlinenote:<参数>`。

- ✅ 关闭浏览器、重启电脑都不会丢
- ⚠️ 清理浏览器数据会一并删除，请定期备份重要内容
- ⚠️ 不同浏览器 / 不同设备之间不互通

## 部署到 GitHub Pages

1. 把 `index.html` 推到 GitHub 仓库
2. 进入仓库 **Settings → Pages**
3. **Source** 选择 `main` 分支根目录，Save
4. 等一两分钟，访问 `https://<你的用户名>.github.io/<仓库名>/`

部署后使用示例：

```
https://<用户名>.github.io/<仓库名>v/?todo      # 待办
https://<用户名>.github.io/<仓库名>/?日记       # 中文也可以
```

## 技术栈

- 原生 HTML
- 原生 CSS
- 原生 JavaScript（无任何依赖库）
