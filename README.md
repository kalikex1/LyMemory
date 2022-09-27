# LyMemory 驱动级内存读写

一款内核级驱动读写工具，可强制读写目标进程内存数据，可用于突破游戏驱动保护强行读写对端内存，该驱动工具实现了读写整数，字节，字节集，单精度浮点数，双精度浮点数，多级偏移读写等功能，读写效率高，工具是本人以前用于读写某火线的现在决定放出来，使用需自己签名或在测试模式下。

读写工具目前支持的读写模式包括如下表所示:

|  导出函数   | 函数作用  |
|  ----  | ----  |
| BYTE ReadProcessMemoryByte(DWORD Pid, ULONG64 Address) | 读内存字节 |
| BOOL WriteProcessMemoryByte(DWORD Pid, ULONG64 Address, BYTE bytef) | 写内存字节 |
| DWORD ReadProcessMemoryInt32(DWORD Pid, ULONG64 Address) | 读内存32位整数型 |
| DWORD ReadProcessMemoryInt64(DWORD Pid, ULONG64 Address) | 读内存64位整数型 |
| BOOL WriteProcessMemoryInt32(DWORD Pid, ULONG64 Address, DWORD write) | 写内存32位整数型 |
| BOOL WriteProcessMemoryInt64(DWORD Pid, ULONG64 Address, DWORD write) | 写内存64位整数型 |
| FLOAT ReadProcessMemoryFloat(DWORD Pid, ULONG64 Address) | 读内存单精度浮点数 |
| DOUBLE ReadProcessMemoryDouble(DWORD Pid, ULONG64 Address) | 读内存双精度浮点数 |
| BOOL WriteProcessMemoryFloat(DWORD Pid, ULONG64 Address, FLOAT write) | 写内存单精度浮点数 |
| BOOL WriteProcessMemoryDouble(DWORD Pid, ULONG64 Address, DOUBLE write) | 写内存双精度浮点数 |
| INT32 ReadProcessDeviationInt32(ProcessDeviationIntMemory *read_offset_struct) | 读多级偏移32位整数型 |
| INT64 ReadProcessDeviationInt64(ProcessDeviationIntMemory *read_offset_struct) | 读多级偏移64位整数型 |
| BOOL WriteProcessDeviationInt32(ProcessDeviationIntMemory *write_offset_struct) | 写多级偏移32位整数型 |
| BOOL WriteProcessDeviationInt64(ProcessDeviationIntMemory *write_offset_struct) | 写多级偏移64位整数型 |
| DWORD ReadDeviationMemory32(ProcessDeviationMemory *read_offset_struct) | 读多级偏移32位内存地址 |
| DWORD64 ReadDeviationMemory64(ProcessDeviationMemory *read_offset_struct) | 读多级偏移64位内存地址 |
| BYTE ReadDeviationByte(ProcessDeviationMemory *read_offset_struct) | 读多级偏移字节型 |
| FLOAT ReadDeviationFloat(ProcessDeviationMemory *read_offset_struct) | 读多级偏移单精度浮点数 |
| BOOL WriteDeviationByte(ProcessDeviationMemory *write_offset_struct,BYTE write_byte) | 写多级偏移字节型 |
| BOOL WriteDeviationFloat(ProcessDeviationMemory *write_offset_struct,FLOAT write_float) | 写多级偏移单精度浮点数 |










正在更新。
