## 本项目实现的最终作用是基于JSP在线网络考试管理系统
## 分为3个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 用户管理
 - 管理员登录
 - 角色管理
 - 试卷管理
 - 题目管理
### 第2个角色为设计文稿，实现了如下功能：
 - PPT截图
 - 论文截图
### 第3个角色为学生角色，实现了如下功能：
 - 学生角色登录
 - 答题考试
 - 试题列表查看
 - 错题查看
## 数据库设计如下：
# 数据库设计文档

**数据库名：** zaixianexam_sys

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [paper](#paper) |  |
| [roleright](#roleright) |  |
| [studentpaper](#studentpaper) |  |
| [subject](#subject) |  |
| [sysfunction](#sysfunction) |  |
| [sysrole](#sysrole) |  |
| [sysuser](#sysuser) |  |

**表名：** <a id="paper">paper</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | pid |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | pname |   varchar   | 11 |   0    |    N     |  N   |       |   |
|  3   | sid |   int   | 10 |   0    |    N     |  N   |       |   |

**表名：** <a id="roleright">roleright</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | RRID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | FUNID |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | ROLEID |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="studentpaper">studentpaper</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | spid |   varchar   | 15 |   0    |    N     |  N   |       |   |
|  2   | UserId |   int   | 10 |   0    |    N     |  N   |       | 用户ID  |
|  3   | sid |   int   | 10 |   0    |    N     |  N   |       |   |
|  4   | studentkey |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | studentstate |   int   | 10 |   0    |    N     |  N   |       |   |
|  6   | pname |   varchar   | 11 |   0    |    N     |  N   |       |   |

**表名：** <a id="subject">subject</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | sid |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | scontent |   varchar   | 150 |   0    |    N     |  N   |       |   |
|  3   | sa |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  4   | sb |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  5   | sc |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  6   | sd |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  7   | skey |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  8   | sstate |   int   | 10 |   0    |    N     |  N   |       |   |

**表名：** <a id="sysfunction">sysfunction</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | FUNID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | FUNNAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | FUNURL |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | FUNPID |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  5   | FUNSTATE |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="sysrole">sysrole</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ROLEID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | ROLENAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | ROLESTATE |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  4   | ROLEDESC |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="sysuser">sysuser</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | UserId |   int   | 10 |   0    |    N     |  Y   |       | 用户ID  |
|  2   | ROLEID |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | userName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  4   | USERPWD |   char   | 20 |   0    |    Y     |  N   |   NULL    |   |
|  5   | USERTRUENAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  6   | USERSTATE |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**运行不出来可以微信 javape 我的公众号：源码码头**
