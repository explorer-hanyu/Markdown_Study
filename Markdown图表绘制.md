# Markdown图表绘制
## 常见的Markdown图表绘制工具
Mermaid 支持通过文本语言生成各种图表：

- 流程图 (Flowchart)
- 序列图 (Sequence Diagram)
- 类图 (Class Diagram)
- 状态图 (State Diagram)
- 甘特图 (Gantt Chart)
- 饼图 (Pie Chart)

## 流程图
```mermaid
graph TD
    A[开始] --> B{条件判断}
    B -->|Yes| C[执行操作A]
    B -->|No| D[执行操作B]
    C --> E[结束]
    D --> E
```
### 流程图方向
TD 或 TB：从上到下
BT：从下到上
RL：从右到左
LR：从左到右

### 流程图嵌套
```mermaid
graph TB
  %% 外层子图 A
  subgraph A[A类]
    direction TB  %% 子图内部方向
    a1[a1小类]
    a2[a2小类]
    end

  %% 外层子图 B
  subgraph B[B类]
    direction TB
    b1[b1小类]
    b2[b2小类]
    end

    a1 --> b2 & a2
  ```

### 节点形状
A`[方形]`：矩形
B`(圆角矩形)`：圆角矩形
C`{菱形}`：菱形（决策）
D`((圆形))`：圆形
E`>旗帜形]`：旗帜形

### 连接线类型
`---` 实线
`-.-` 虚线
`===` 粗实线
`-->` 实线箭头
`-.->` 虚线箭头
`==>` 粗实线箭头

## 时序图与甘特图
### 时序图
```mermaid
sequenceDiagram
    participant A as 用户
    participant B as 系统
    participant C as 数据库
    
    A->>B: 登录请求
    B->>C: 验证用户信息
    C-->>B: 返回验证结果
    B-->>A: 登录成功/失败
```
时序图语法要点：
- `participant` 定义参与者
- `->>` 实线箭头
- `-->>` 虚线箭头
- `note` 添加注释

### 甘特图
```mermaid
gantt
    title 项目开发计划
    dateFormat  YYYY-MM-DD
    axisFormat  %m%d
    section 设计阶段
    需求分析      :done,    des1, 2024-01-01,2024-01-15
    UI设计       :active,  des2, 2024-01-10, 40d
    section 开发阶段
    前端开发      :         dev1, after des2, 50d
    后端开发      :         dev2, 2024-02-01, 60d
    section 测试阶段
    单元测试      :         test1, after dev1, 18d
    集成测试      :         test2, after dev2, 20d
```
甘特图语法要点：
- `title` 设置标题
- `dateFormat` 定义日期格式
- `axisFormat` 定义X轴格式
- `section` 定义阶段
- 任务状态：done（已完成）、active（进行中）、crit（关键）

## 饼图
```mermaid
pie
    title 浏览器市场份额
    "Chrome" : 65
    "Safari" : 15
    "Firefox" : 10
    "其他" : 10
```


## 类图
类图用于面向对象设计，展示类及其关系。
```mermaid
classDiagram
    class 用户 {
        +用户名: string
        +密码: string
        +登录()
    }
    
    class 订单 {
        +订单号: int
        +创建日期: date
        +计算总价()
    }
    
    用户 "1" --> "n" 订单
```

类图语法要点：
- 定义关系：
  - `<|--` 继承（子类指向父类）
  - `..|>`实现（类指向接口）
  - `-->` 关联（单向关联）
  - `--` 双向关联
  - `o--` 聚合（整体-部分，部分可独立）
  - `*--` 组合（整体-部分，同生共死）
  - `..>` 依赖
- 在类内部
  - `+` 表示 public
  - `-` 表示 private
  - `#` 表示 protected。

## 状态图
```mermaid
stateDiagram
    [*] --> 关闭
    关闭 --> 打开 : 开门
    打开 --> 关闭 : 关门
    关闭 --> 锁定 : 上锁
    锁定 --> 关闭 : 解锁
    打开 --> 锁定 : 紧急锁定
    锁定 --> [*] : 系统重置
```

状态图基本语法:
- 使用 stateDiagram-v2或 stateDiagram（兼容旧版）。
- [*] 表示起点或终点。
- 状态用文字描述，可以换行或使用复合状态。

# 高级技巧
## 主题定制

```mermaid
%%{init: {'theme': 'forest'}}%%
pie
    title 自定义主题
    "项目A" : 30
    "项目B" : 50
    "项目C" : 20
```

## 交互式图表

```mermaid
graph TD
    A[点击我] --> B[显示详细信息]
    click A "https://www.runoob.com" "提示文本"
```
