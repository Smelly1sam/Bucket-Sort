#include <iostream>
#include <ctime>
#include <cstdlib>

using namespace std;

int a1d[1000];
int x,y;
int a2d[1000][10];
int r,c;
int loc;
int round=0;

void randarray(){
  for(x=0;x<1000;x++){
		a1d[x]=((rand()) % 999)+1;
	}
	}

void nestzeros(){
	for (r=0;r<1000;r++){
		for (c=0;c<10;c++){
			a2d[r][c]=0;
		}
	}
}

void sort(){
	if (round==0){
	for (x=0;x<1000;x++){
		loc=((a1d[x])%10);
		a2d[x][loc]=a1d[x];
	}
	}
	else if (round==1){
		for (x=0;x<1000;x++){
		loc=int(((a1d[x])%100)/10);
		a2d[x][loc]=a1d[x];
	}
	}
	else if (round==2){
		for (x=0;x<1000;x++){
		loc=int(((a1d[x])%1000)/100);
		a2d[x][loc]=a1d[x];
		}
	}
	round++;
}

void gather(){
	x=0;
	for (c=0;c<10;c++){
		for (r=0;r<1000;r++){
			if (a2d[r][c]>0){
				a1d[x]=a2d[r][c];
				x++;
			}

		}
	}
nestzeros();
}

void display(){
for(x=0;x<1000;x++){
	cout<<a1d[x]<<'\t';
}
cout<<endl<<endl;
x=0;
}

int main(){
	srand((unsigned)time(0));
	randarray();
	display();
	nestzeros();
	sort();
	gather();
	sort();
	gather();
	sort();
	gather();
	display();
	system("pause");
	return 0;
}
