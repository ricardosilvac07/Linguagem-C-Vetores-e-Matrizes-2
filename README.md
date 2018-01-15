#include <stdio.h>
int main (void)
{
const int bimestresAnuais = 4;
const int numeroDeAlunos = 4;
float notasAlunos [numeroDeAlunos][bimestresAnuais] = {0};
float mediasAlunos [numeroDeAlunos] = {0};
float media = 0;
int aluno = 0;
int notas = 0;

printf("Insira as notas do aluno 1:\n");

for (aluno = 0; aluno < numeroDeAlunos; ++aluno) {

    for (notas = 0; notas < bimestresAnuais; ++notas) {
        scanf("%f", &notasAlunos[aluno][notas]);
        media += &notasAlunos[aluno][notas];
    }

    mediasAlunos[aluno] = media / bimestresAnuais;
    media = 0;
    printf("Insira as 4 notas do aluno %i:\n", aluno + 2);

}

for (aluno = 0; aluno < numeroDeAlunos; ++aluno) {

    printf("A media do aluno %i eh: %.2f\n", aluno+1, mediaAlunos [aluno]);
}

return 0;
}
