#include "dirent.h"
#include <string>
#include <iostream>
//#include <unistd.h>

using namespace std;
/*Ыежн*/
int fileNameFilter(const struct dirent *cur)
{
	std::string str(cur->d_name);
	if (str.find(".jpg") != std::string::npos)
	{
		return 1;
	}
	return 0;
}

int main()
{
	while (1)
	{
		struct dirent **namelist;
		//int n = scandir("h:/10", &namelist, 0, alphasort);
		int n = scandir("h:/10", &namelist, 0, versionsort);

		if (n < 0)
			cerr << "memery error " << endl;
		else
			cout << "total number is: " << n << endl;

		for (int i = 0; i < n; i++)
		{
			// /* skip . && .. */
			// if(namelist[i]->d_name[0] == '.')
			//     continue;

			cout << namelist[i]->d_name << endl;
			free(namelist[i]);
		}
		free(namelist);
		//sleep(5);
	}

	return 0;
}