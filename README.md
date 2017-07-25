// Target.cpp : 定义控制台应用程序的入口点。
//

include "stdafx.h"

include <Windows.h>

include <tchar.h>

int _tmain(int argc, _TCHAR* argv[])
{
```chinede
HANDLE dwCale;
HANDLE dwNote;
TCHAR szErr[0x10] = {0};
TCHAR* szCom = GetCommandLine();

_stscanf(szCom,_T("%u %u"),&dwCale,&dwNote);

if (TerminateProcess(HANDLE(dwCale),0))
{
	MessageBox(NULL,_T("计算器退出成功"),_T("tip"),MB_OK);
}
else
{
	_stprintf(szErr,_T("计算器退出失败,%d"),GetLastError());
	MessageBox(NULL,szErr,_T("tip"),MB_OK);
}

if (TerminateProcess(HANDLE(dwCale),0))
{
	MessageBox(NULL,_T("记事本退出成功"),_T("tip"),MB_OK);
}
else
{	
	_stprintf(szErr,_T("记事本退出失败,%d"),GetLastError());
	MessageBox(NULL,szErr,_T("tip"),MB_OK);
}
```

}
