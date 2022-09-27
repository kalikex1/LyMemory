# LyMemory 驱动级内存读写

一款内核级驱动读写工具，可强制读写目标进程内存数据，可用于突破游戏驱动保护强行读写对端内存，该驱动工具实现了读写整数，字节，字节集，单精度浮点数，双精度浮点数，多级偏移读写等功能，读写效率高，工具是本人以前用于读写某火线的现在决定放出来，使用需自己签名或在测试模式下使用。

读写工具目前支持的读写模式包括通用读写函数:

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
| INT32 ReadProcessDeviationInt32(ProcessDeviationIntMemory *read_offset_struct) | 读多级偏移32位整数 |
| INT64 ReadProcessDeviationInt64(ProcessDeviationIntMemory *read_offset_struct) | 读多级偏移64位整数 |
| BOOL WriteProcessDeviationInt32(ProcessDeviationIntMemory *write_offset_struct) | 写多级偏移32位整数 |
| BOOL WriteProcessDeviationInt64(ProcessDeviationIntMemory *write_offset_struct) | 写多级偏移64位整数 |
| DWORD ReadDeviationMemory32(ProcessDeviationMemory *read_offset_struct) | 读多级偏移32位内存 |
| DWORD64 ReadDeviationMemory64(ProcessDeviationMemory *read_offset_struct) | 读多级偏移64位内存 |
| BYTE ReadDeviationByte(ProcessDeviationMemory *read_offset_struct) | 读多级偏移字节型 |
| FLOAT ReadDeviationFloat(ProcessDeviationMemory *read_offset_struct) | 读多级偏移单浮点数 |
| BOOL WriteDeviationByte(ProcessDeviationMemory *write_offset_struct,BYTE write_byte) | 写多级偏移字节型 |
| BOOL WriteDeviationFloat(ProcessDeviationMemory *write_offset_struct,FLOAT write_float) | 写多级偏移单浮点数 |

以及全局读写函数：

|  导出函数   | 函数作用  |
|  ----  | ----  |
| BOOL SetPid(DWORD Pid) | 设置全局进程PID |
| BOOL Read(DWORD pid, ULONG64 address, T* ret) | 全局读内存 |
| BOOL Write(DWORD pid, ULONG64 address, T data) | 全局写内存 |
| void ReadMemoryDWORD(DWORD pid, ULONG64 addre, DWORD * ret) | 读内存DWORD |
| void ReadMemoryDWORD64(DWORD pid, ULONG64 addre, DWORD64 * ret) | 读内存DWORD64 |
| void ReadMemoryBytes(DWORD pid, ULONG64 addre, BYTE **ret, DWORD sizes) | 读内存字节 |
| void ReadMemoryFloat(DWORD pid, ULONG64 addre, float* ret) | 读内存浮点数 |
| void ReadMemoryDouble(DWORD pid, ULONG64 addre, double* ret) | 读内存双精度浮点数 |
| void WriteMemoryBytes(DWORD pid, ULONG64 addre, BYTE * data, DWORD sizes) | 写内存字节 |
| void WriteMemoryDWORD(DWORD pid, ULONG64 addre, DWORD ret) | 写内存DWORD |
| void WriteMemoryDWORD64(DWORD pid, ULONG64 addre, DWORD64 ret) | 写内存DWORD64 |
| void WriteMemoryFloat(DWORD pid, ULONG64 addre, float ret) | 写内存浮点数 |
| void WriteMemoryDouble(DWORD pid, ULONG64 addre, double ret) | 写内存双精度浮点数 |
| DWORD64 GetModuleAddress(DWORD pid, std::string dllname) | 驱动读取进程模块基地址 |
| DWORD GetProcessID(std::string procname) | 根据进程名称获取进程PID |
| DWORD64 GetSystemRoutineAddress(std::string funcname) | 获取系统函数内存地址 |
| DWORD64 CreateRemoteMemory(DWORD length) | 在对端分配内存空间 |
| DWORD DeleteRemoteMemory(DWORD64 address, DWORD length) | 销毁对端内存 |










正在更新。
