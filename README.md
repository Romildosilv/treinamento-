treinamento Holerite//

#include <stdio.h>
#include <math.h>
double qtdhoras,valor,desc,inss,sind,ir,salario,salariobruto,salarioliquido;

int main()
{
  printf("\ndigite o valor de cada hora: ");
  scanf("%lf",&valor);
  printf("digite o numero de horas trabalhadas: ");
  scanf("%lf",&qtdhoras);
  salario=qtdhoras*valor;
if(salario>=0 )
{
    printf("\n*******descontos********");
  inss=inss-(salario*0.08);
  ir=ir-(salario*0.11);
  sind=sind-(salario*0.05);
  salariobruto=salario+inss+ir+sind;
  desc=desc-inss-sind-ir;
   printf("\n-salaro bruto: R$%.2lf",salariobruto);
   printf("\n-inss:  R$%.2lf",inss);
   printf("\n-imposto de renda:  R$%.2lf",ir);
   printf("\n-desconto sindicato:  R$%.2lf\n",sind);
   
   
  salarioliquido=salariobruto-desc;
   printf("\n*******salario a receber********");
  printf("\n+ salario bruto: R$%.2lf",salariobruto);
  printf("\n- inss (8%): R$%.2lf",inss);
  printf("\n- IR (11%): R$%.2f",ir);
  printf("\n- Sindicato (5%): R$%.2lf",sind);
  printf("\n= salario liquido a receber: R$%.2fl",salarioliquido);
  
 }
 else {
 printf ("\nnada a receber ***********");
 }
 
 return 0;
}
