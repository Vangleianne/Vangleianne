#include <math.h>
#include <stdlib.h>
#include <stdio.h>           //biblioteca

#define k 0.55555555555         // Declaração de constante

void cabecalho();               // Função Cabeçalho

void cab();                     // Função Cabeçalho Menor

int menu();                     // Função Menu

float situacao_aluno();         // Função Situação do Aluno: Aprovado ou Reprovado

int senha ();                   // Função Senha: Acesso Permitido ou Acesso Negado

int ano_bissexto();             // Função Ano Bissexto

int calculadora();              // Função Calculadora

int progressao_arit_geomet();    // Função Progressão Aritmética ou Geométrica

int num_primos();               // Função Números Primos em um Intervalo

int operacao_bancaria ();        // Função Operação Bancária

int cadastro_de_aluno ();        // Função Cadastro de Aluno
struct infAluno;

int diferenca_entre_duas_datas();  // Função Diferença entre Duas Datas
struct dma;

int limite_de_temperatura();


int main()                      // Função Principal
{
    int opcao = 0;
    int cont = 1;               // variável para retornar ao menu principal
    
    cabecalho (); // Função Cabeçalho
    
    do
    {
        
    
        opcao = menu();
    
        switch (opcao)
        {   case 0:
                
                printf("Sair do programa\n");
                //system("pause"); 
                return 0;
                break;
            
            case 1:
                while(cont == 1)
                {
                    situacao_aluno();                   // Função Situação do Aluno: Aprovado ou Reprovado
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;
            
            case 2:
                while(cont == 1)
                {   senha();                            // Função Senha: Acesso Permitido ou Acesso Negado
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;

            case 3:
                while(cont ==1)
                {   ano_bissexto();                     // Função Ano Bissexto;
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }                
                
            case 4:
                while(cont == 1)
                {   calculadora();                      // Função Calculadora;
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }                
                if (cont == 0)
                {   opcao = 0; }
                
                break;    
            
            case 5:
                while(cont ==1)
                {   progressao_arit_geomet();           // Função Progressão Aritmética ou Geométrica
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                } 
                if (cont == 0 )
                {   opcao = 0; }
                break; 
            
            case 6:
                while(cont ==1)
                {   num_primos();                       // Função Números Primos em um Intervalo
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;
            
            case 7:
                while(cont ==1)
                {   operacao_bancaria();                       // Função Operação Bancária
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;

            case 8:
                while(cont ==1)
                {   cadastro_de_aluno ();                      // Função Cadastro de Aluno
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;

            case 9:
                while(cont ==1)
                {   diferenca_entre_duas_datas();                      // Função Diferença entre Duas Datas
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;
                
            case 10:
                while(cont ==1)
                {   limite_de_temperatura();                      // Função de Controle de Temperatura em ºF
                    printf("Voltar ao Painel: (1) Sim ou (0) Nao --- "); 
                    scanf("%d", &cont);
                    cab(); break;
                }
                if (cont == 0)
                {   opcao = 0; }
                break;
                
        default:
            printf("---Opção Invalida. Escolha uma opção disponível");
    }
    
    } while(cont);
}



void cabecalho ()   // Função Cabeçalho
{ 
  printf("-----------------------------------------------------------------\n");   
  printf("-------Instituto Federal de Educação, Ciência e Tecnologia-------\n");
  printf("-------Curso: Engenharia Elétrica 2021.2 - 1º Período------------\n");
  printf("-------Aluno:Vangleianne de Araujo Pinho----------------------------\n");
  printf("-------Disciplina: Algorítmo e Lógica de Programação 1-----------\n");
  printf("-------Trabalho Final--------------------------------------------\n");
  printf("-----------------------------------------------------------------\n\n");   
  return;
}



void cab ()                         // Função Cabeçalho Menor
{ 
  printf("-----------------------------------------------------------------\n");   
  return;
}




int menu()    // Função Menu
{
    int opcao;
    do
    {
        printf("-------Painel do Aplicativo--------------------------------------\n   ");
        printf("--- 0. Sair\n   ");
        printf("--- 1. Situação do Aluno: Aprovado ou Reprovado?\n   ");
        printf("--- 2. Senha: Acesso Permitido ou Acesso Negado?\n   ");
        printf("--- 3. Veja se o ano é bissexto.\n   ");
        printf("--- 4. Função Calculadora.\n   ");
        printf("--- 5. Calcule a Soma da Progessão: Aritmética ou Geométrica.\n   ");        
        printf("--- 6. Veja quais são os números primos de um intervalo.\n");      
        printf("   --- 7. Operacão Bancária.\n"); 
        printf("   --- 8. Cadastro de Aluno.\n");
        printf("   --- 9. Diferença entre Duas Datas.\n");
        printf("   --- 10. Controle de Limite de Temperatura e Conversão em ºF para ºC.\n"); 
        printf("-----------------------------------------------------------------\n   ");
        printf(" --- Escolha uma opção:   --- --- ---  ");
        scanf("%d", &opcao);
        cab();

        return opcao;
    }
    while(opcao);
}



float situacao_aluno()                                          // Função Situação do Aluno: Aprovado ou Reprovado
{
    float nota = 0.00;
    float trabalho = 0.00;
    
    cab();
    printf ("--- Digite a nota do aluno:    ");
    scanf("%f", &nota);
    printf ("--- Digite o valor do trabalho do aluno:    ");
    scanf("%f", &trabalho);
    
    if (nota >= 6 || trabalho >= 8)
    {   printf ("--- Aluno Aprovado.\n");    }
    else
    {   printf ("--- Aluno Reprovado.\n");   }
    cab();
    return 0;
}



int senha ()                                    // Função Senha: Acesso Permitido ou Acesso Negado
{
    int senha = 0;
    
    cab();
    printf("--- Digite sua senha:...");
    scanf("%d", &senha);
    
    if (senha == 1234)
        printf("--- Acesso Permitido\n");
    else
        printf("--- Acesso Negado\n");
    cab();
    return 0;
}


int ano_bissexto()                                      // Função Ano bissexto
{
 int ano = 0;
 
    cab();
    printf("--- Veja se o ano é bissexto.\n  Digite o ano:...");
    scanf("%d", &ano);
    
    if ((ano % 400 == 0) || ((ano % 4 == 0) && (ano % 100 !=0)))
    {   printf("--- O ano é bissexto! \n");     }
    else
    {   printf("--- O ano não é bissexto, não é.\n");     }
    cab();
    return 0;
}

int calculadora()                                           // Função Calculadora
{
    float n1 = 0.00, n2 = 0.00, r = 0.00;
    int opcao_cal = 0;
    
    cab();
    printf("--- Escolha uma opção:\n---(1) soma;\n---(2) Subtração;\n---(3) Multiplicação;\n---(4) Divisão.\n");
    cab();
    scanf("%d", &opcao_cal);
    cab();
    printf("--- Atribua valor a n1:   "); 
    scanf("%f", &n1);
    printf("--- Atribua valor a n2:   ");
    scanf("%f", &n2);
    cab();
    
    switch(opcao_cal)
    {   case 1:
        r = n1 + n2;
        printf("--- Resultado: %.2f\n", r);         
        break;
        case 2:
        r = n1 - n2;
        printf("--- Resultado: %.2f\n", r);         
        break;
        case 3:
        r = n1 * n2;
        printf("--- Resultado: %.2f\n", r);        
        break;
        case 4:
        r = n1 / n2;
        printf("--- Resultado: %.2f\n", r);        
        break;           
        default:
        printf("--- Opção Invalida.\n");                  
    }
    cab();
    return 0;     
}



int progressao_arit_geomet()                                  // Função Progressão Aritmética ou Geométrica
{
    float a1, r, an, sn, q;
    int n;    
    int opcao_pro;

    cab();
    do 
    {
        printf("--- Escolha uma opção: \n---(1) Progressão Aritmética - PA.\n---(2) Progressão Geométrica - PG.\n---(3) Sair\n");
    cab();    
        scanf("%d", &opcao_pro);
    cab();
    switch(opcao_pro)
        {
        case 1:
            printf("--- Progressao Aritmetica - PA\n");
            printf("--- Entre com o valor do primeiro termo: ");
            scanf("%f",&a1);
            printf("--- Entre com o valor da razao: ");
                
            do
            {   scanf("%f",&r);  }
            while(r==0);    
            printf("--- Numero de termos: ");
                
            do
            { scanf("%i",&n);   }
            while(n<=0);    
            an = (a1 + (n - 1) * r);                                    // Cálculo do enésimo termo da PA
            sn = (a1 + an)/2;                                           // Cálculo da soma da PA
            
            cab();
            printf("--- E-nesimo termo da P.A. - an: %.2f",an);
            printf("\n--- A Soma do termos da P.A. - Sn: %.2f\n",sn);
            cab();
            break;
            
      case 2:
            printf("--- Progressao Geometrica - PG\n");
            printf("--- Entre com o valor do primeiro termo: ");
            scanf("%f",&a1);
            printf("--- Entre com o valor da razao: ");
            
            do  
            { scanf("%f",&q);   }
            while(q==0);    
            printf("--- Numero de termos: ");
            
            do  
            { scanf("%i",&n);   }                               //pow: potenciação
            while(n<=0);                                        //pow(base,expoente)
            an = (a1 * pow(q,n-1));                             // Cálculo do enésimo termo da PG
            sn = ((a1*(pow(q,n) - 1))/(q-1));                   // Cálculo da soma da PG
            
            cab();
            printf("--- E-nesimo termo da P.G. - an: %.2f",an);
            printf("\n--- A Soma do termos da P.G. finita - Sn: %.2f\n",sn);
            cab();
            break;
        }
   }
    while(opcao_pro != 3); 
    
    cab();
    return 0;
}

int num_primos()
{
    int n = 0, i = 2, j = 2, z = 2;
    /* n: armazena o limete do intevalo */
    /* i: gerencia a estrutura de repetição */
    /* j: verifica se um número é primo */    
    /* z: armazenar se um número possui ou não mais que dois divisores */ 
    
    cab();
    printf("---Digite o tamanho do intervalo: ... ");
    scanf("%d", &n);

    do
    {   j = 2, z = 0;
        do
        {   if (i % j == 0)
            {   z = 1;
                break;        }
            j ++;                  }
        while ( j < i );
    
        if (!z)
        printf("--- %d \n ", i);
        i++;                    }
    while (i < n);
    
    cab();
    return 0;
}

int operacao_bancaria ()
{
    float saldo = 0, valor_processado = 0;
    int opcao;
    
    cab();
    printf("--- Escolha uma opção: \n--- (1) Consulta. \n--- (2) Saque. \n--- (3) Depósito. \n--- (4) Sair.   \n");
    cab();
    do 
    {   scanf("%d", &opcao);
        switch (opcao)
        {
            case 1:
                cab();
                printf("--- Saldo: %.2f\n", saldo);
                cab();
                printf("--- Escolha uma opção: \n--- (1) Consulta. \n--- (2) Saque. \n--- (3) Depósito. \n--- (4) Sair.   \n");
                cab();
                break;
            case 2:
                cab();
                scanf("%f", &valor_processado);
                cab();
                saldo -= valor_processado;
                printf("--- Saque: %f \n", valor_processado);
                cab();
                printf("--- Escolha uma opção: \n--- (1) Consulta. \n--- (2) Saque. \n--- (3) Depósito. \n--- (4) Sair.   \n");
                cab();                
                break;
            case 3:
                cab();
                scanf("%f", &valor_processado);
                saldo += valor_processado; 
                printf("--- Depósito: %f \n", valor_processado);
                cab();
                printf("--- Escolha uma opção: \n--- (1) Consulta. \n--- (2) Saque. \n--- (3) Depósito. \n--- (4) Sair.   \n");
                cab();                
                break;
            case 4:                                 
                break;
            default:
                printf("--- Opção Invalida.\n");    
    }   }
    while(opcao !=4);
    printf("Finalizando...\n");
    
    cab();
    return 0; 
}



struct infAluno
{   
    char nome[75];
    int matricula;
    char curso[75];      
};


typedef struct infAluno aluno;


int cadastro_de_aluno ()
{   
    int i = 0;
    aluno turma[1];

        cab();
        printf("--- Cadastro de Aluno:-------------------------------------------\n");
        printf("--- Nome:   \n"); 
        printf("--- Matricula:   \n");
        printf("--- Curso:   \n"); 
        
    for (i = 0; i < 1; i++)
    {   
        scanf("%*c%[^\n]",  turma[i].nome);
        scanf("%d",         &turma[i].matricula);
        scanf("%*c%[^\n]",  turma[i].curso);
    }

    for (i = 0; i < 1; i++)
    {
        cab();
        printf("--- Cadastro de Aluno:   \n");
        printf("--- Nome: %s \n", turma[i].nome);        
        printf("--- Matrícula: %d\n", turma[i].matricula);
        printf("--- Curso: %s\n", turma[i].curso);
        cab();
    }
   // break;
    cab();
    return 0;
}


struct dma 
{   int dia;
    int mes;
    int ano;    };
    
typedef struct dma data;

int diferenca_entre_duas_datas()                    // Função de Controle de Temperatura em ºF
{
    data d1;
    data d2;
    data dif;
    
    cab();
    printf("--- Digite o dia da primeira data: \n");
    printf("--- Digite o mês da primeira data: \n");
    printf("--- Digite o ano da primeira data: \n");

    scanf("%d %d %d", &d1.dia, &d1.mes, &d1.ano);
    
    printf("--- Digite o dia da segunda data: \n");
    printf("--- Digite o mês da segunda data: \n");
    printf("--- Digite o ano da segunda data: \n");
    
    scanf("%d %d %d", &d2.dia, &d2.mes, &d2.ano);
    
    dif.dia = d2.dia - d1.dia;
    dif.mes = d2.mes - d1.mes;
    dif.ano = d2.ano - d1.ano;
    
    printf("--- Diferença é de %d anos %d meses %d dias\n", dif.ano, dif.mes, dif.dia);
    cab();
    cab();
    return 0;
}


int limite_de_temperatura()
{
    float c = 0;
    int lim_inferior = 10, lim_superior = 0, incremento = 0, i = 0;
    
    cab();
    printf("--- Digite o limite: ...");
    scanf("%d", &lim_superior);
    printf("--- Digite a faixa:  ...");
    scanf("%d", &incremento);
    cab();
    
    for (i = lim_inferior; i <= lim_superior; i += incremento)
    {
        c = (i - 32)*k;
        printf("%d F = %.2f ºC \n", i, c);
    }
    
    cab();
    cab();
    return 0;    
}
