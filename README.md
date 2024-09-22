## 本项目实现的最终作用是基于SSH学生信息管理系统
## 分为3个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 专业管理
 - 学生管理
 - 学科管理
 - 学院管理
 - 教师管理
 - 班级管理
 - 管理员登录
### 第2个角色为教师角色，实现了如下功能：
 - 学生信息查询
 - 成绩管理
 - 教师登录
### 第3个角色为学生角色，实现了如下功能：
 - 个人信息修改
 - 学生角色登录
 - 密码修改
 - 成绩查询
## 数据库设计如下：
# 数据库设计文档

**数据库名：** ssh_xsxx_sys

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [cj](#cj) |  |
| [class_room](#class_room) |  |
| [manage](#manage) |  |
| [teacher](#teacher) | 教师信息表 |
| [user](#user) | 用户表 |
| [xk](#xk) |  |
| [xy](#xy) |  |
| [zy](#zy) |  |

**表名：** <a id="cj">cj</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | createTime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  3   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  4   | teacher_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  5   | user_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 用户ID  |
|  6   | xk_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | df |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="class_room">class_room</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  4   | zy_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="manage">manage</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  4   | realname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 真实名字  |
|  5   | type |   int   | 10 |   0    |    N     |  N   |       | 类型  |

**表名：** <a id="teacher">teacher</a>

**说明：** 教师信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  3   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  4   | phone |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  5   | realname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 真实名字  |
|  6   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  7   | xy_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  8   | sex |   int   | 10 |   0    |    Y     |  N   |   NULL    | 性别  |

**表名：** <a id="user">user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | age |   int   | 10 |   0    |    Y     |  N   |   NULL    | 年龄  |
|  3   | createTime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  4   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  5   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  6   | phone |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  7   | realname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 真实名字  |
|  8   | sex |   int   | 10 |   0    |    Y     |  N   |   NULL    | 性别  |
|  9   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  10   | classroom_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="xk">xk</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |

**表名：** <a id="xy">xy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |

**表名：** <a id="zy">zy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | isDelete |   int   | 10 |   0    |    Y     |  N   |   NULL    | 是否删除  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  4   | xy_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

