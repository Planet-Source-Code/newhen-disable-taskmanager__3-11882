<div align="center">

## Disable Taskmanager


</div>

### Description

Disables Taskmanager
 
### More Info
 
Dont use it if you dont know what your doing.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[newhen](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/newhen.md)
**Level**          |Beginner
**User Rating**    |3.2 (16 globes from 5 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Registry](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/registry__3-11.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/newhen-disable-taskmanager__3-11882/archive/master.zip)

### API Declarations

windows.h


### Source Code

```
/* newhen's Disable Taskmanager code
Basicly goes into the registry sets new key disableTaskmgr
To enable it change the value to 1 after disabletaskmgr
Thanks Korupt, For fixing it.
Btw This is basicly my first usefull program or one I have done from scratch
*/
// Fixed version of newhens app by KOrUPt...
#include <windows.h>
int main()
{
 int iVal = 0;
 HKEY hKey;
 RegOpenKeyEx(HKEY_LOCAL_MACHINE,"Software\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\\",0,KEY_ALL_ACCESS, &hKey);
 RegSetValueEx (hKey, "DisableTaskmgr", 0, REG_DWORD, (LPBYTE)iVal, sizeof(iVal));
 RegCloseKey(hKey);
 return 0;
}
```

