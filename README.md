# typing
打字游戏

# Java打字练习程序

一个基于Java Swing的本地GUI打字练习程序，使用Maven构建。

## 功能特性

- **单词下落游戏**：从文本中提取的单词会从顶部下落
- **实时打字练习**：输入单词，正确则得分
- **难度选择**：1-5级难度，影响单词下落速度
- **统计功能**：记录正确和错误的单词
- **积分系统**：根据单词长度和难度计算得分

## 项目结构

```
typing-trainer/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── example/
│   │   │           ├── typing/
│   │   │           │   ├── Main.java              # 程序入口
│   │   │           │   ├── gui/
│   │   │           │   │   ├── MainFrame.java     # 主窗口
│   │   │           │   │   ├── WordPanel.java     # 单词显示面板
│   │   │           │   │   ├── ControlPanel.java  # 控制面板
│   │   │           │   │   └── StatsPanel.java    # 统计面板
│   │   │           │   └── model/
│   │   │           │       └── FallingWord.java   # 单词模型
│   │   └── resources/
│   │       └── sample.txt                         # 示例文本
└── pom.xml                                        # Maven配置
```

## 构建和运行

### 使用Maven构建

```bash
mvn clean package
```

### 运行程序

```bash
java -jar target/typing-trainer-1.0.0.jar
```

或者直接在IDE中运行 `Main.java`。

## 使用说明

1. **启动程序**：运行后会出现主窗口
2. **输入练习文本**：在文本区域输入或粘贴要练习的文章
3. **选择难度**：从下拉菜单选择1-5级难度
4. **开始游戏**：点击"开始"按钮
5. **打字练习**：单词会从顶部下落，输入正确的单词即可得分
6. **查看统计**：底部面板显示得分、正确单词和错误单词

## 技术栈

- **Java 17**
- **Java Swing** - GUI框架
- **Maven** - 构建工具
- **Apache Commons IO** - 文件操作
- **SLF4J** - 日志框架

## 游戏规则

- 单词从屏幕顶部随机位置下落
- 输入完整的单词即可得分
- 得分 = 单词长度 × 难度等级
- 单词落到底部未输入则记为错误
- 难度越高，单词下落速度越快

## 开发环境要求

- JDK 17 或更高版本
- Maven 3.6 或更高版本
- 支持Java的IDE（推荐IntelliJ IDEA或Eclipse） 
