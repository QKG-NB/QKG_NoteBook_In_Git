实现代码：
`Global DEFFCT CHAR[256] Real_To_String(Var:IN );浮点数转字符串`
`DECL STATE_T State;定义指令执行后的状态`
`DECL CHAR Ret[256];定义返回值` 
`DECL REAL Var;d`
`DECL INT zOffset,Index;定义写入字符串的起始位置（0为起始位置）
`IF VARSTATE("Var")<>#INITIALIZED THEN`
   `MsgQuit("Input    data not initialized!")`
   `HALT`
`ENDIF`
`FOR Index=1 TO 256`
    `Ret[Index]=0`
`ENDFOR`
`zOffset=0`
`SWRITE(Ret[],State,zOffset,"%F",Var)`
`IF zOffset<=256 THEN`
   `RETURN (Ret[])`
  `ELSE`
   `MsgQuit("Input    data out of length boundary!")`
   `HALT`
   `RETURN ("0")`
`ENDIF`
`ENDFCT`




