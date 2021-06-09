#include <stdio.h>
#include <math.h>
typedef struct
{ 
double real, imag;
} complex_t;

int scan_complex(complex_t *c);
void print_complex(complex_t c);
complex_t add_complex(complex_t c1, complex_t c2);
complex_t subtract_complex(complex_t c1, complex_t c2); 
complex_t multiply_complex(complex_t c1, complex_t c2); 
complex_t divide_complex(complex_t c1, complex_t c2);
double abs_complex(complex_t c);

int scan_complex(complex_t *c){ 
printf("Bilangan Real: ");
scanf("%lf", &(*c).real);
printf("Bilangan Imajiner: ");
scanf("%lf", &(*c).imag); 
}
void print_complex(complex_t c){
if (c.imag>=0) 
printf("%.2f + %.2f i\n", c.real, c.imag);
else 
printf("%.2f - %.2f i\n", c.real, -c.imag);
}
complex_t add_complex(complex_t c1, complex_t c2){
complex_t hasil;
hasil.real = c1.real + c2.real;
hasil.imag = c1.imag + c2.imag; 
return hasil;
}
complex_t subtract_complex(complex_t c1, complex_t c2){
complex_t hasil; 
hasil.real = c1.real - c2.real;
hasil.imag = c1.imag - c2.imag;
return hasil; 
}
complex_t multiply_complex(complex_t c1, complex_t c2){
complex_t hasil; 
hasil.real = (c1.real*c2.real)-(c1.imag*c2.imag); 
hasil.imag = (c1.real*c2.imag) + (c1.imag*c2.real); 
return hasil;
}
complex_t divide_complex(complex_t c1, complex_t c2){
complex_t hasil;
double penyebut; 
c2.imag = -c2.imag;
hasil = multiply_complex(c1, c2);
penyebut = (c2.real*c2.real) + (c2.imag*c2.imag);
hasil.real /= penyebut;
hasil.imag /= penyebut;
return hasil; 
}
double abs_complex(complex_t c){
double hasil; 
hasil = sqrt(c.real*c.real + c.imag*c.imag);
return hasil; 
}

int main(){ 
complex_t bil1, bil2;
double w,x,y,z;
complex_t a,b,c,d;
printf("Program Operasi Bilangan Kompleks (A + B i)\n\n");
printf("Masukkan Bilangan real dan imajiner untuk bilangan kompleks pertama:\n");
scan_complex(&bil1);
printf("Masukkan Bilangan real dan imajiner untuk bilangan kompleks kedua:\n");
scan_complex(&bil2);
a = add_complex(bil1, bil2);
b = subtract_complex(bil1, bil2);
c = multiply_complex(bil1, bil2); 
d = divide_complex(bil1, bil2); 
printf("\nHasil\n");
w=bil1.real;
x=bil1.imag;
y=bil2.real;
z=bil2.real;
printf("(%.2f+%.2fi)+(%.2f+%.2fi)=",w,x,y,z); print_complex(a);
printf("(%.2f+%.2fi)+(%.2f+%.2fi)=",w,x,y,z); print_complex(b);
printf("(%.2f+%.2fi)+(%.2f+%.2fi)=",w,x,y,z);print_complex(c);
printf("(%.2f+%.2fi)+(%.2f+%.2fi)=",w,x,y,z); print_complex(d);
printf("|%.2f+%.2fi| = %.2f\n",w,x, abs_complex(bil1));
printf("|%.2f+%.2fi| = %.2f\n",y,z, abs_complex(bil2));
return 0; 
