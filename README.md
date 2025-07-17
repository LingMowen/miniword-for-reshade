# Miniword for ReShade

## 项目概述
Miniword for ReShade 是一个与 ReShade 紧密相关的项目。ReShade 是一款广受欢迎的开源着色器注入工具，常用于为游戏添加各类视觉特效。此项目可能专注于在 ReShade 框架下实现迷你文字相关的功能，如在游戏画面中展示自定义文字、运用不同字体样式等。从 `ReshadeEffectShaderToggler.ini` 文件可推测，该项目具备对 ReShade 中不同类型着色器（顶点着色器、像素着色器、计算着色器等）进行配置和管理的能力。

## 功能特性
### 着色器管理
- **分组配置**：支持将着色器分组管理，如配置文件中的 `Group0`，用户可针对不同组设置不同的属性。
- **哈希匹配**：通过着色器哈希值（如 `ShaderHash0`、`ShaderHash1`）精准定位和管理特定的像素着色器。

### 渲染与显示设置
- **渲染目标控制**：能够指定渲染目标索引（`RenderTargetIndex`），还可选择是否仅匹配交换链分辨率（`MatchSwapchainResolutionOnly`）。
- **纹理绑定管理**：提供多种纹理绑定相关操作，如是否提供纹理绑定（`ProvideTextureBinding`）、清除纹理绑定（`ClearTextureBindings`）等。

### 按键绑定
- **自定义按键**：尽管当前配置文件中多数按键绑定值设为 0，但预留了按键绑定功能，方便用户后续自定义操作快捷键。

## 安装步骤
### 简便安装方式。
- [迷你 reshade-installer]([https://github.com/LingMowen/miniword-for-reshade/issues](https://github.com/shisanwen-gmail/mini-reshade-installer?tab=readme-ov-file#%E8%BF%B7%E4%BD%A0%E4%B8%96%E7%95%8C%E5%85%89%E5%BD%B1%E5%8C%85%E5%AE%89%E8%A3%85%E5%99%A8))。

### 具体安装流程
1. **克隆项目代码**：使用以下命令将项目克隆到本地：
```bash
git clone https://github.com/LingMowen/miniword-for-reshade.git
```
2. **复制文件**：打开 ReShade 的安装目录，把克隆下来的 `miniword-for-reshade` 项目中的相关文件（具体文件依据项目实际情况确定）复制到 迷你世界 的对应目录。

## 使用方法
### 配置调整
- 打开 `ReshadeEffectShaderToggler.ini` 文件，依据自身需求修改配置项。例如，若要添加新的像素着色器，可在 `[Group0_PixelShaders]` 部分添加新的 `ShaderHash` 项，并相应调整 `AmountHashes` 的值。
```ini
[Group0_PixelShaders]
ShaderHash0=1581138296
ShaderHash1=1668299851
ShaderHash2=新的着色器哈希值
AmountHashes=3
```

### 运行项目
1. 启动支持 ReShade 的游戏。
2. 按下 ReShade 的默认快捷键 `Home` 打开 ReShade 菜单。
3. 在菜单里找到并启用 Miniword for ReShade 的相关功能。

## 贡献指南
若你想为该项目贡献代码，请按以下步骤操作：
1. **Fork 项目**：将本项目 Fork 到你的 GitHub 账户。
2. **创建新分支**：使用以下命令创建新分支：
```bash
git checkout -b new-feature
```
3. **进行代码修改**：在新分支上开展代码修改和功能开发工作。
4. **提交修改**：完成修改后，使用以下命令提交：
```bash
git add .
git commit -m "Add new feature"
git push origin new-feature
```
5. **创建 Pull Request**：在 GitHub 上创建一个 Pull Request，详细描述你的修改内容和目的。

## 问题反馈/联系我们
1.若在使用过程中遇到问题或有建议，可在 [项目的 Issues 页面](https://github.com/LingMowen/miniword-for-reshade/issues) 提交问题。提交时，请尽量提供详细信息，如操作系统、ReShade 版本、问题出现的具体情况等，以便开发者更好地理解和解决问题。
2.可以在[官方网站](https://mowen.biz)反馈。提交时，请尽量提供详细信息，如操作系统、ReShade 版本、问题出现的具体情况等，以便开发者更好地理解和解决问题
3.可以前往[官方QQ群](https://qm.qq.com/q/xpsf9NQOVq)

## 许可证
本项目采用MIT许可证。这意味着你可以自由地对项目代码进行修改，将修改后的版本分发给他人，并且可以将项目用于私人用途。但请确保在使用过程中遵循相关法律法规和道德准则。

## 致谢
感谢所有为这个项目做出贡献的开发者和用户。如果你有任何疑问或需要进一步的帮助，请随时联系项目维护者。 
