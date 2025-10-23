# 多语言访问说明

## 🌍 如何切换语言版本

本博客已启用多语言支持，目前支持：
- 🇨🇳 简体中文（默认）
- 🇬🇧 English
- 🇯🇵 日本語

### 访问方式

#### 方法一：通过 URL 后缀访问

对于支持多语言的文章（如《神秘猫猫历险记》），可以通过以下方式访问：

1. **中文版（默认）**：
   ```
   https://shaddocknh3.github.io/p/神秘猫猫历险记/
   ```

2. **英文版**：
   ```
   https://shaddocknh3.github.io/en/p/神秘猫猫历险记/
   ```

3. **日文版**：
   ```
   https://shaddocknh3.github.io/ja/p/神秘猫猫历险记/
   ```

#### 方法二：使用语言切换器（如果主题支持）

Stack 主题应该在页面右上角显示语言切换器，点击即可切换。

### 本地测试

启动 Hugo 服务器后：

```bash
hugo server -D
```

访问：
- 中文：http://localhost:1313/
- 英文：http://localhost:1313/en/
- 日文：http://localhost:1313/ja/

### 配置文件

多语言配置位于：
- `/config/_default/languages.toml` - 主配置
- `/config/_default/languages.zh-cn.toml` - 中文配置
- `/config/_default/languages.en.toml` - 英文配置
- `/config/_default/languages.ja.toml` - 日文配置

### 文章多语言版本

采用文件命名约定：
```
content/post/神秘猫猫历险记/
├── index.md       (中文版)
├── index.en.md    (英文版)
└── index.ja.md    (日文版)
```

Hugo 会自动识别这些文件并建立翻译关联。

## 注意事项

1. **URL 结构**：
   - 默认语言（中文）的 URL 不包含语言代码
   - 其他语言的 URL 包含语言代码前缀（/en/, /ja/）

2. **SEO 优化**：
   - Hugo 会自动添加 `<link rel="alternate" hreflang="...">` 标签
   - 帮助搜索引擎识别不同语言版本

3. **主题支持**：
   - Stack 主题原生支持多语言
   - 语言切换器会自动显示在导航栏
