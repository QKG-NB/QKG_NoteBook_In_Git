## 描述
当前运行模式  
该变量显示当前设定的运行模式。
## 语法
mode = $MODE_OP
## 语法说明
| 元素    | 说明    |
|---|---|
| mode    | 类型：ENUM MODE_OP    |
|    | - #AUT：自动模式    |
|    | - #EX：外部自动模式    |
|    | - #T1：T1 模式    |
|    | - #T2：T2 模式    |
|    | - #INVALID：无效运行模式    |
## 示例
DECL MODE_OP opmode
opmode = $MODE_OP
IF opmode == #AUT THEN
    HALT
ENDIF