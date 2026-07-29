# 我的日历 — GitHub 云同步版

## 工作原理

```
手机/电脑浏览器
      ↓
GitHub Pages（托管网页）
      ↓
GitHub API（读写数据）
      ↓
你的私有仓库（存数据）
```

---

## 首次设置步骤

### 第 1 步：创建 GitHub Personal Access Token

1. 打开 https://github.com/settings/tokens/new
2. 在 "Note" 填写：`日历应用`
3. 在 "Expiration" 选择：`No expiration`（永不过期）
4. 勾选 **repo** 权限（勾这一个就够了）
5. 点击底部的 **Generate token**
6. **复制生成的 token**（格式是 `ghp_xxxxxxxxxxxx`），保存好，只显示一次

### 第 2 步：创建私有数据仓库

1. 打开 https://github.com/new
2. Repository name: `calendar-data`
3. 选择 **Private**（私有）
4. 勾选 "Add a README file"
5. 点击 **Create repository**

### 第 3 步：启用 GitHub Pages

> 仓库 `zmd-10086/calendar` 已创建并推送代码后：

1. 打开 https://github.com/zmd-10086/calendar/settings/pages
2. Source 选择 **Deploy from a branch**
3. Branch 选择 **main**，目录选 **/ (root)**
4. 点击 **Save**
5. 等待 1-2 分钟，页面会显示网址：`https://zmd-10086.github.io/calendar/`

### 第 4 步：打开网站

1. 浏览器访问：`https://zmd-10086.github.io/calendar/`
2. 输入：
   - GitHub 用户名：`zmd-10086`
   - 数据仓库名：`calendar-data`
   - Personal Access Token：第 1 步生成的 token
3. 勾选"记住用户名和仓库名"
4. 点击"进入日历"

---

## 跨设备使用

- 每台设备都访问同一个网址
- 第一次打开时输入同样的 Token
- 数据自动跨设备同步

---

## 从旧的单机版迁移数据

1. 用浏览器打开旧的 `index.html`（桌面上的 rili 文件夹）
2. 点击 **📥 导出备份**，得到一个 JSON 文件
3. 在新网站上点击 **📤 导入备份**
4. 选择刚才的 JSON 文件，选择"覆盖"模式
5. 数据就全部迁移过来了
