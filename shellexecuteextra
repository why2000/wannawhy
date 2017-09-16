#include <stdio.h>
#include<windows.h>
#include<tchar.h>
void execute(char name[]){
	//selfcopy();
	//char ch;
	//char path[MAX_PATH]="c:\\encode.exe";
	///for(ch='d';ch<='e';ch++){
		//path[0] = ch;
	
		SHELLEXECUTEINFO sei={sizeof(SHELLEXECUTEINFO)};
		sei.lpVerb=TEXT("runas");
		sei.lpFile=TEXT(name);//add  application  which you want to run as administrator here
		//sei.nShow=SW_SHOWNORMAL;//without this,the windows will be hiden
		if(!ShellExecuteEx(&sei)){
		DWORD dwStatus=GetLastError();
		if(dwStatus==ERROR_CANCELLED){//调试用
		printf("提升权限被用户拒绝\n");
		}
		else 
		if(dwStatus==ERROR_FILE_NOT_FOUND){//调试用
		printf("所要执行的文件没有找到\n");
		}
		}
	//}
	//system("pause");
	
	}

int _tmain(int argc,TCHAR* argv[])
{	
	ShowWindow(FindWindow("ConsoleWindowClass",argv[0]),0);
	execute("encode.exe");
	return 0;
}
