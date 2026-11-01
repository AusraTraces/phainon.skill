<div align="center">

# Phainon.skill

[![许可证](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![版本](https://img.shields.io/badge/Version-v1.0.0-green.svg)](SKILL.md)
[![游戏](https://img.shields.io/badge/Game-崩坏：星穹铁道-orange.svg)](https://hsr.hoyoverse.com/)

</div>

> 开源白厄角色扮演SKILL技能包！适合崩铁宝宝体质！

## ✨ 特性

- **官方设定集成** - 参考官方设定整理而成，内容详尽高价值
- **全面整合** - 包含角色背景、关系网络、台词风格等多维度信息
- **易于集成** - 标准化的Skill格式，支持多种AI平台和框架

## 📋 目录

- [特性](#特性)
- [快速开始](#快速开始)
- [安装指南](#安装指南)
- [使用方法](#使用方法)
- [项目结构](#项目结构)
- [角色设定详解](#角色设定详解)
- [开发指南](#开发指南)
- [贡献指南](#贡献指南)
- [质量报告](#质量报告)
- [许可证](#许可证)
- [致谢](#致谢)

## 🚀 快速开始

### 系统要求

- 支持Skill格式的AI平台（如Trae IDE、Character.ai等）
- 基本的角色扮演或AI对话开发环境

### 安装指南

1. **下载项目**
   ```bash
   git clone https://github.com/yourname/phainon-skill.git
   cd phainon-skill
   ```

2. **集成到你的项目**
   - 将整个 `Phainon` 文件夹复制到你的技能目录
   - 确保你的AI系统支持Skill格式

3. **激活**
   - 在你的代码中调用 `Phainon` 技能

## 💡 使用方法

### 基础使用

```python
# 示例：在支持Skill的系统中使用
from skill_manager import SkillManager

skill_manager = SkillManager()
skill_manager.load_skill("phainon")

# 激活白厄角色
response = skill_manager.activate("phainon", user_input="你好，白厄")
print(response)
```

### 角色扮演示例

**用户输入**: "白厄，最近如何"

**期望输出**: "哀丽秘榭的白厄，向你致意。同为奥赫玛的异乡人，相聚即是缘分。随我来，说不定我们以后还有并肩作战的时候。"

### 自定义配置

你可以在 `SKILL.md` 中调整角色参数

## 📁 项目结构

```
Phainon/
├── 📄 README.md                 # 项目说明文档（本文件）
├── 📄 SKILL.md                  # 技能入口与扮演规则
├── 📄 info.md                   # 角色身份与核心标签
├── 📄 personality.md            # 性格、动机与价值观
├── 📄 story.md                  # 官方设定故事&原始故事整合
├── 📄 relationships.md          # 人物关系
├── 📄 follow.md                 # 设定冲突与保守表述
└── 📄 LICENSE                   # 开源许可证
```

## 🔧 开发指南

### 扩展角色设定

如果你想添加新的角色特征或台词：

1. **更新 `personality.md`** - 扩展性格描述、添加新的台词样本
2. **修改 `relationships.md`** - 添加新的关系设定

### 集成到自定义系统

```python
# 示例：自定义集成
class phainonSkill:
    def __init__(self):
        self.profile = self.load_file("info.md")
        self.personality = self.load_file("personality.md")
        self.story = self.load_file("story.md")

    def generate_response(self, user_input, context):
        # 实现你的响应生成逻辑
        # 参考personality.md中的台词风格
        return self.style_response(raw_response)
```

### 性能优化建议

- 预加载角色数据到内存
- 使用缓存机制存储常用响应
- 实现响应模板系统提高效率

## 特别提示
本SKILL包内容参考官方设定及萌娘百科、米游社WIKI等公开资料整理而成，如需二次开发，请注明来源。

## 🤝 贡献指南

欢迎崩铁技术区老师贡献！以下是参与方式：

### 如何贡献

1. **报告问题**
   - 在Issues中报告bug或提出改进建议
   - 包含详细的复现步骤和期望结果

2. **提交代码**
   - Fork本项目
   - 创建功能分支 (`git checkout -b feature/AmazingFeature`)
   - 提交更改 (`git commit -m 'Add some AmazingFeature'`)
   - 推送到分支 (`git push origin feature/AmazingFeature`)
   - 开启Pull Request

### 贡献规范

- 遵循现有的代码风格和文档格式
- 确保所有更改都经过测试
- 更新相关文档和示例
- 添加有意义的提交信息

### 需要帮助的领域

- [ ] 台词补充
- [ ] SKILL性能优化测试

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 🙏 致谢

### 数据来源

- [萌娘百科 - 白厄](https://zh.moegirl.org.cn/%E7%99%BD%E5%8E%84)
- [米游社 - 崩坏：星穹铁道WIKI - 白厄](https://bbs.mihoyo.com/sr/wiki/content/5107/detail?bbs_presentation_style=no_header)
- [百度百科 - 卡厄斯兰那](https://baike.baidu.com/item/%E5%8D%A1%E5%8E%84%E6%96%AF%E5%85%B0%E9%82%A3/65929635)
- [BWiki - 星穹铁道](https://wiki.biligame.com/sr/)
- 游戏内剧情和语音台词
- 社区玩家整理资料

### 特别感谢

- **@最伟大的作品 卡厄大人~** 提供角色Q&A内容
- **HeartEase1** 因为老师的项目产生了灵感，编写本SKILL格式，并部分参考了老师的SKILL包
- 《崩坏：星穹铁道》项目组
- 社区玩家提供的宝贵资料和分析
- 所有为这个项目做出贡献的开发者

## 🔗 相关链接

- [官方游戏官网](https://hsr.hoyoverse.com/)
- [QQ 星穹之下AI测试群](https://qun.qq.com/universal-share/share?ac=1&authKey=r69LDODfY1ax7ycnSYK7eZ2DMSOuU1CfmjSk3ufZwtveLke8MNKIl%2FJzkGAUD8WT&busi_data=eyJncm91cENvZGUiOiIxMDc4ODkyOTQyIiwidG9rZW4iOiJMalBqd1M5QWhJcEpYTkJOT0Q1NmVqdXd6K2ptUVhqS2NVMGlyb0NxMHBXQ2lvb2l1dEV1L3diaWYvTU9UT1FGIiwidWluIjoiMjk0NjYxNzMwNCJ9&data=BKXeJ8p265HXX2u3EsN7_wheMnvAPq9opPd_I3UY1ybwXZrb1bim6KKdE0hOjZJIYVVzSex2MkJ8xf0va3sCfw&svctype=4&tempid=h5_group_info)

---

⭐ 如果这个项目对你有帮助，请给我们一个Star！

💬 有任何问题或建议，欢迎在Issues中讨论！

# SKILL Development

Phainon.SKILL
- Developer：星穹之下项目组-Under the Star Rail Team
- Special_thanks: miHoYo & Hoyoverse & HeartEase & @最伟大的作品 卡厄大人~
- MIT LICENSE

* 《崩坏：星穹铁道》非商业同人项目，非官方创作，请勿进行商业行为
