# Exercicios-thiago-20-
// TESTE DE SELEÇAO 1
#include <stdio.h>


int main() {
    int A, B, C, D;
    
    scanf("%d %d %d %d", &A, &B, &C, &D);
    if (B > C && D > A && C + D > A + B && C > 0 && D > 0 && A % 2 == 0){
        printf("Valores aceitos\n");
    }else{
        printf("Valores nao aceitos\n");
    }
    
 

    return 0;
}
//INTERVALO
#include <stdio.h>
 
int main() {
 
double valor;

scanf("%lf", &valor);

if(valor >= 0 && valor <= 25){
    printf("Intervalo [0,25]\n");
}
if(valor > 25 && valor <= 50){
    printf("Intervalo (25,50]\n");
}
if(valor > 50 && valor <= 75){
    printf("Intervalo (50,75]\n");
}
if(valor > 75 && valor <= 100){
    printf("Intervalo (75,100]\n");
}
if (valor <0 || valor > 100){
    printf("Fora de intervalo\n");
}
    return 0;
}
//Lanche
#include <stdio.h>
 
int main() {
 int codigo, quantidade;
 scanf("%d %d", &codigo, &quantidade);
 
 double total_da_conta;
 if(codigo == 1){
     total_da_conta = quantidade * 4.00;
 }else if(codigo ==2){
     total_da_conta = quantidade * 4.50;
 }else if(codigo == 3){
     total_da_conta = quantidade * 5.00;
 }else if(codigo == 4){
     total_da_conta = quantidade * 2.00;
 }else if(codigo == 5){
     total_da_conta = quantidade * 1.50;
 }
 printf("Total: R$ %.2f\n",total_da_conta);
    return 0;
}
// MEDIA 3
#include <stdio.h>
 
int main() {
 double N1, N2, N3, N4;
 scanf("%lf %lf %lf %lf", &N1, &N2, &N3, &N4);
 
 double media;
 media = (N1 * 2 + N2 * 3 + N3 * 4 + N4 * 1 ) / 10;
 printf("Media: %.1f\n", media);
 if (media >= 7){
     printf("Aluno aprovado.\n");
 }else if(media < 5){
     printf("Aluno reprovado.\n");
 }else{
     printf("Aluno em exame.\n");
     double exame;
     scanf("%lf", &exame);
     printf("Nota do exame: %.1f\n",exame);
     media = (media + exame) / 2;
     if (media >= 5){
         printf("Aluno aprovado.\n");
     }else{
         printf("Aluno reprovado.\n");
     }
     printf("Media final: %.1f\n", media);
 }
 return 0;
}
// COORDENADAS DE UM PONTO
#include <stdio.h>
 
int main() {
 double x,y;
 scanf("%lf %lf", &x, &y);
 if(x == 0 && y == 0){
    printf("Origem\n"); 
 }else if(x == 0 ){
     printf("Eixo Y\n");
 }else if(y == 0){
     printf("Eixo X\n");
 }else if (x > 0 && y > 0){
     printf("Q1\n");
 }else if (x < 0 && y > 0){
     printf("Q2\n");
 }else if (x < 0 && y < 0){
     printf("Q3\n");
 }else if (x > 0 && y < 0){
     printf("Q4\n");
 }
 
 
 
    return 0;
}
// SORT SIMPLES
#include <stdio.h>
 
int main() {
 int A, B, C;
 scanf("%d %d %d", &A, &B, &C);

 int A1, B1, C1;
 
 A1 = A;
 B1 = B;
 C1 = C;
 
 int temp;
 if(A > B){
     temp = A;
     A = B;
     B = temp;
 }
 if (A > C){
     temp = A;
     A = C;
     C = temp;
 }if(B > C){
     temp = B;
     B = C;
     C = temp;
 }
 printf("%d\n", A);
 printf("%d\n", B);
 printf("%d\n", C);
 printf("\n");
 
 printf("%d\n", A1);
 printf("%d\n", B1);
 printf("%d\n", C1);
 
    return 0;
}
// TRIANGULO
#include <stdio.h>
 
int main() {
 double a, b, c;
 double perimetro, area;
 
 scanf("%lf %lf %lf", &a, &b, &c);
 
 if(a < b + c && b < a + c && c < b + a){
     perimetro = a + b + c;
     printf("Perimetro = %.1f\n", perimetro);
     
 }else{
     area = (a + b) * c / 2;
     printf("Area = %.1f\n", area);
 }
 
 
    return 0;
}
// MULTIPLOS
#include <stdio.h>
 
int main() {
 int A, B;
 scanf("%d %d", &A, &B);
 
 if(A % B == 0 || B % A ==0){
     printf("Sao Multiplos\n");
 }else{
     printf("Nao sao Multiplos\n");
 }
 
    return 0;
}
// TIPOS DE TRIANGULOS
#include <stdio.h>
 
int main() {
 double A, B, C;
 scanf("%lf %lf %lf", &A, &B, &C);
 
 double temp;
 if(A < B){
     temp = A;
     A = B;
     B = temp;
 }
 if(A < C){
     temp = A;
     A = C;
     C = temp;
 }
 if(B < C){
     temp = B;
     B = C;
     C = temp;
 }
 if(A >= B + C){
     printf("NAO FORMA TRIANGULO\n");
 }else{
 if(A * A == B * B + C * C){
     printf("TRIANGULO RETANGULO\n");
 }
 if(A * A > B * B + C * C){
     printf("TRIANGULO OBTUSANGULO\n");
 }
 if(A * A < B * B + C * C){
     printf("TRIANGULO ACUTANGULO\n");
 }
 if(A == B && B == C){
     printf("TRIANGULO EQUILATERO\n");
 }
 else if(A == B || B == C || A == C){
     printf("TRIANGULO ISOSCELES\n");
 }
    return 0;
}
}
// TEMPO DE JOGO
#include <stdio.h>
 
int main() {
 int horainicial, horafinal;
 int duracao;
 
 scanf("%d %d", &horainicial, &horafinal);

if (horafinal > horainicial){
    duracao = horafinal - horainicial;
    printf("O JOGO DUROU %d HORA(S)\n", duracao);
}else{
    duracao = (24 - horainicial) + horafinal;
    printf("O JOGO DUROU %d HORA(S)\n", duracao);
}
    return 0;
}
// AUMENTO DE SALARIO
#include <stdio.h>
 
int main() {
    double salario, novosalario, reajuste;
    int percentual;
    
    scanf("%lf", &salario);
    if(salario <= 400.00){
        reajuste = salario * 0.15;
        percentual = 15;
    }else if(salario <= 800.00){
        reajuste = salario * 0.12;
        percentual = 12;
    }else if(salario <= 1200.00){
        reajuste = salario * 0.10;
        percentual = 10;
    }else if(salario <= 2000.0){
        reajuste = salario * 0.07;
        percentual = 7;
    }else{
        salario > 2000;
        reajuste = salario * 0.04;
        percentual = 4;
    }
     novosalario= salario + reajuste;
     printf("Novo salario: %.2f\n", novosalario);
     printf("Reajuste ganho: %.2f\n", reajuste);
     printf("Em percentual: %d %%\n", percentual);
 
    return 0;
}
// DDD
#include <stdio.h>
 
int main() {
 int DDD;
 scanf("%d", &DDD);
 
 if(DDD == 61){
     printf("Brasilia\n");
 }else if(DDD == 71){
     printf("Salvador\n");
 }
 else if(DDD == 11){
     printf("Sao Paulo\n");
 }
 else if(DDD == 21){
     printf("Rio de Janeiro\n");
 }
 else if(DDD == 32){
     printf("Juiz de Fora\n");
 }
 else if(DDD == 19){
     printf("Campinas\n");
 }
 else if(DDD == 27){
     printf("Vitoria\n");
 }
 else if(DDD == 31){
     printf("Belo Horizonte\n");
 }
 else{
     printf("DDD nao cadastrado\n");
 }
 
    return 0;
}
// NUMEROS POSITIVOS
#include <stdio.h>
 
int main() {
 double A, B, C, D, E, F;
 int positivos = 0;
 
 scanf("%lf %lf %lf %lf %lf %lf", &A, &B, &C, &D, &E, &F);
 
 if(A > 0){
     positivos ++;
 }
 if(B > 0){
     positivos ++;
 }
 if(C > 0){
     positivos ++;
 }
 if(D > 0){
     positivos ++;
 }
 if(E > 0){
     positivos ++;
 }
 if(F > 0){
     positivos ++;
 }
 printf("%d valores positivos\n", positivos);
    return 0;
}
// POSITIVOS E MEDIA
#include <stdio.h>
 
int main() {
 double valor;
 int positivos = 0;
 double soma = 0;
 double media;
 
 for(int i = 0; i < 6; i++){
     scanf("%lf", &valor);
     if(valor > 0){
         positivos++;
         soma = soma + valor;
     }
 }
 media  = soma / positivos;
 printf("%d valores positivos\n", positivos);
 printf("%.1f\n", media);
 
 
    return 0;
}
//PARES ENTRE 5 NUMEROS
#include <stdio.h>
 
int main() {
 int A, B, C, D, E;
 int pares = 0;
 scanf("%d %d %d %d %d", &A, &B, &C, &D, &E);
 if(A % 2 == 0){
     pares++;
 }
 if(B % 2 == 0){
     pares++;
 }
 if(C % 2 == 0){
     pares++;
 }
 if(D % 2 == 0){
     pares++;
 }
 if(E % 2 == 0){
     pares++;
 }
  printf("%d valores pares\n", pares);
  
  
    return 0;
}
// PARES IMPARES POSITIVOS E NEGATIVOS
#include <stdio.h>
 
int main() {
 int A, B, C, D, E;
 int pares = 0;
 int impares = 0;
 int positivos = 0;
 int negativos = 0;
 
 scanf("%d %d %d %d %d", &A, &B, &C, &D, &E);
 
 if(A % 2 == 0){
     pares++;
 }
 if(A % 2 != 0){
     impares++;
 }
 if(A > 0 ){
     positivos++;
 }
 if(A < 0){
     negativos++;
 }
 if(B % 2 == 0){
     pares++;
 }
 if(B % 2 != 0){
     impares++;
 }
 if(B > 0){
     positivos++;
 }
 if(B < 0){
     negativos++;
 }
 if(C % 2 != 0){
     impares++;
 }
 if(C > 0){
     positivos++;
 }
 if(C < 0){
     negativos++;
 }
 if(D % 2 == 0){
     pares++;
 }
 if(D % 2 != 0){
     impares++;
 }
 if(D > 0){
     positivos++;
 }
 if(D < 0){
     negativos++;
 }
 if(E % 2 == 0){
     pares++;
 }
 if(E % 2 != 0){
     impares++;
 }
 if(E > 0){
     positivos++;
 }
 if(E < 0){
     negativos++;
 }
 
 
 printf("%d valor(es) par(es)\n", pares);
 printf("%d valor(es) impar(es)\n", impares);
 printf("%d valor(es) positivo(s)\n", positivos);
 printf("%d valor(es) negativo(s)\n", negativos);
    return 0;
}
// SEIS NUMEROS IMPARES
#include <stdio.h>
 
int main() {
 int X;
 scanf("%d", &X);
 if(X % 2 == 0){
     X = X + 1;
 }
  printf("%d\n", X);
  printf("%d\n", X + 2);
  printf("%d\n", X + 4);
  printf("%d\n", X + 6);
  printf("%d\n", X + 8);
  printf("%d\n", X + 10);
     return 0;
}
