# GitHub Pages 上传与发布说明

## 一、所需材料

本压缩包已经包含发布所需的全部网站文件：

1. `index.html`（必须）
2. `.nojekyll`（建议保留）
3. `README.md`（项目说明，不影响网页）

当前网站是单文件静态网页，照片、CSS 和 JavaScript 已嵌入 `index.html`，不需要额外上传图片文件夹。

## 二、注册并登录 GitHub

1. 打开 GitHub 官网。
2. 注册账号并完成邮箱验证。
3. 登录后进入个人主页。

建议使用适合公开展示的用户名，因为默认网站地址会包含 GitHub 用户名。

## 三、新建仓库

### 方式 A：项目网站（推荐，最灵活）

1. 点击右上角 `+` → `New repository`。
2. Repository name 填写一个英文名称，例如：`neckie-portfolio`。
3. 选择 `Public`。
4. 不要勾选“Add a README file”（压缩包内已经包含）。
5. 点击 `Create repository`。

默认网址通常为：

```text
https://你的用户名.github.io/neckie-portfolio/
```

### 方式 B：个人主页网站

把仓库名称准确设置为：

```text
你的用户名.github.io
```

默认网址为：

```text
https://你的用户名.github.io/
```

每个账号只能有一个同名的个人主页仓库。

## 四、通过浏览器上传文件

1. 解压本压缩包。
2. 进入新建的 GitHub 仓库。
3. 点击 `Add file` → `Upload files`。
4. 把解压后的文件拖入上传区域：
   - `index.html`
   - `.nojekyll`
   - `README.md`
   - 其他说明文件可以一起上传，也可以不上传。
5. 在页面底部填写提交说明，例如：

```text
Initial portfolio website
```

6. 点击 `Commit changes`。

注意：Windows 文件资源管理器可能不显示 `.nojekyll`。即使漏传该文件，这个纯 HTML 网站通常仍可工作；之后也可以在 GitHub 网页端新建一个名为 `.nojekyll` 的空文件。

## 五、开启 GitHub Pages

1. 在仓库顶部点击 `Settings`。
2. 左侧找到 `Code and automation` → `Pages`。
3. 在 `Build and deployment` 中：
   - Source 选择 `Deploy from a branch`；
   - Branch 选择 `main`；
   - Folder 选择 `/(root)`；
   - 点击 `Save`。
4. 等待 GitHub 完成构建。
5. 回到 `Settings` → `Pages`，点击 `Visit site`。

首次发布或更新通常需要短暂等待。也可以进入仓库的 `Actions` 标签查看部署状态：绿色对勾表示成功，红色叉号表示部署失败。

## 六、启用 HTTPS

在 `Settings` → `Pages` 页面中勾选 `Enforce HTTPS`。如果选项暂时不可用，等待证书生成后再尝试。

## 七、以后如何更新

1. 在仓库中点击 `index.html`。
2. 选择上传新的同名文件，或删除旧文件后重新上传。
3. 点击 `Commit changes`。
4. 等待 Pages 自动重新部署。

建议每次更新前在本地浏览器中打开 `index.html`，检查：

- 页面能否正常加载；
- 导航能否跳转；
- “多元的我”卡片能否展开和返回；
- 手机尺寸下是否正常；
- 邮箱和外部链接是否正确。

## 八、常见问题

### 打开网站后显示 404

检查以下项目：

- 文件是否准确命名为 `index.html`；
- `index.html` 是否在仓库根目录，而不是多套了一层文件夹；
- Pages 发布分支是否为 `main`、目录是否为 `/(root)`；
- `Actions` 中部署是否完成。

### 页面更新后仍显示旧版本

- 等待部署完成；
- 使用 `Ctrl + F5` 强制刷新；
- 尝试无痕窗口；
- 查看 `Actions` 是否出现新的 Pages 部署记录。

### 图片不显示

当前版本的图片已经嵌入 `index.html`，正常情况下不会出现相对路径丢失。如果日后把图片拆分到 `assets` 文件夹，需要保证文件名、大小写和 HTML 路径完全一致。

### 网站地址太长

可以把仓库改为 `你的用户名.github.io`，或者绑定自己购买的域名。绑定域名前，请先阅读压缩包中的 `自定义域名说明.txt`。
