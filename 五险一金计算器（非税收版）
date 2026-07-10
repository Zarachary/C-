#include <stdio.h>

int a = 0;
float b = 0.01;
float Salary; //工资
float HousingProvidentFundRate;//公积金比列
float HousingProvidentFund;//公积金扣费
float ThreeInsurancesRate = 0.102;// 医疗保险、养老保险、失业保险比列
float ThreeInsurances;// 医疗保险、养老保险、失业保险合计扣费
float Deduction;//扣除金额
float FinalIncome;//最终收入

void Calculator();//计算函数


int main()
{
  char decision;
 printf("========================\n");
 printf("#欢迎来到五险一金计算器#\n");
 printf("========================\n");
 printf("是否缴纳公积金？（Y/N）：");
 scanf("%c",&decision);
 getchar();

 if (decision == 'Y' || decision == 'y' )
 {
   printf("请输入公积金比列（5%%~12%%）:");
   scanf("%d", &a);
   
   while (a < 5 || a > 12)
   {
      printf("您输入的比列不对请重新输入：");
      scanf("%d", &a);
   }

 }
 else
 {
      a =0;
      printf("您的公积金缴纳比列为%d%%\n",a);
 }

      printf("请输入您的工资：");
      scanf("%f",&Salary);
      while (Salary < 0 )
      {
         printf("工资不能够为负数，请重新输入");
         scanf("%f",&Salary);
      }
         printf("您的工资为：%.2f\n",Salary);
      
   
   if(Salary !=0){
      Calculator();
      printf("===输出结果===\n");

      printf("生育保险和工伤保险由单位承担，本计算器不纳入计算\n");

      printf("公积金扣除：%f\n",HousingProvidentFund);

      printf("医疗保险、养老保险、失业保险扣除：%f\n",ThreeInsurances);

      printf("合计扣费：%f\n",Deduction);

      printf("最终个人收入为：%f\n",FinalIncome);
      }
      return 0;
 }
 
 


 


 void Calculator()
{
   HousingProvidentFundRate = a * b ;//公积金比列

   HousingProvidentFund = Salary * HousingProvidentFundRate; //公积金扣费

   ThreeInsurances = Salary * ThreeInsurancesRate; // 医疗保险、养老保险、失业保险合计扣费

   Deduction = HousingProvidentFund+ ThreeInsurances; //扣费额度

   FinalIncome = Salary - Deduction ;//最终收入
}
