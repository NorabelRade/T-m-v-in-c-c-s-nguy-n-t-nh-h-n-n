# T-m-v-in-c-c-s-nguy-n-t-nh-h-n-n
Tìm và in ra màn hình tất cả các số nguyên tố không vượt quá số n cho trước nhập từ bàn phím. Số nguyên tố là số chỉ có ước số là 1 và chính số đó.
#include <stdio.h>
#include <conio.h>

void main()
{
	int n, i, j, d;
	clrscr();
	printf("Nhap gia tri N : ");
	scanf("%d", &n);
	printf("Cac so nguyen to khong vuot qua %d la :\n", n);

	for (d = 0, i = 2; i <= n; i++)
	{
		for (j = 2; j <= i / 2; j++)
			if (i % j == 0) break;
		if (j == i / 2 + 1)
		{
			d++;
			printf(" %d", i);
		}
	}
	printf("\nTong so co %d so nguyen to", d);
	getch();
}
