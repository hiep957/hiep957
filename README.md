#include <iostream>
using namespace std;

int BinarySearch(int a[], int x, int f, int t) {
		int m =(t+f)/2;
		if(x == a[m]) {
		 	cout <<"x o vi tri: "<<m;
		 }
		else {
		 	if (x>a[m]){
		 		BinarySearch(a,x,m,t);
			 }
			 else if(x<a[m]){
			 	BinarySearch(a,x,f,m-1);
			 }
		 }
	}


int a[1000];


int main() {
	int n;
	cout <<"Nhap so phan tu cua mang:"; cin >>n;
	int f =0;
	int t=n-1;
	cout <<"Nhap phan tu cua mang: "<<endl;
	for(int i=0;i<n;i++) {
		cin >> a[i];
	}		
	for(int i=0;i<n;i++) {
		cout <<a[i]<<"   ";
	}
	int x;
	cout <<"Nhap so can tim x: ";
	cin >>x;
	BinarySearch(a,x,f,t);
}
