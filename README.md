## ALC-Projeto1.2



#include <stdio.h>

int main(){

   
    int m, n,i,j;
    m = 0;n=0;i=0;j=0;
    printf("Digite o valor de m: ");
    scanf("%d", &m);
    printf("Digite o valor de n: ");
    scanf("%d", &n);

    float x[n],y[m],ax[n];
    float A[m][n];
    printf("Digite o valor os valores do vetor X:\n");
    for(i=0;i<n;i++){
        scanf("%f", &x[i]);
    }
    printf("Digite o valor os valores do vetor Y:\n");
    for(i=0;i<n;i++){
        scanf("%f", &y[i]);
    }

    for(i=0; i < m; i++){
       for(j=0; j < n; j++){
            printf("Digite o valor A[%d][%d]:",i+1,j+1);
            scanf("%f", &A[i][j]);
       }
    }


    for (int i = 0 ; i <= m; i++){
        for (int j = 0; j <= n; j++){
            if(j==0){
                ax[i]= A[i][j]*x[j];

            }else{
                ax[i]=ax[i]+(A[i][j]*x[j]);
            }
        }
    y[i]=ax[i]+y[i];
    }
    printf("\n ax+y = { ");
    for(i=0;i<m;i++){
        printf("%2.f ",y[i]);

    }
    printf("}");


    return 0;
}
