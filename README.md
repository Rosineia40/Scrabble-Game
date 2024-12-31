// Scrabble-Game CC50
// Exercício - MOD2 CC50 - O Curso de Ciência da Computação de Harvard no Brasil

#include <ctype.h>
#include <cs50.h>
#include <stdio.h>
#include <string.h>

// Pontuação para cada letra do alfabeto
int POINTS[] = {1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 1, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10};

// Função para calcular a pontuação de uma palavra
int compute_score(string word);

int main(void)
{
    // Solicitar palavras dos jogadores
    string player1 = get_string("Player 1: ");
    string player2 = get_string("Player 2: ");

    // Calcular as pontuações
    int score1 = compute_score(player1);
    int score2 = compute_score(player2);

    // Determinar o vencedor
    if (score1 > score2)
    {
        printf("Player 1 wins!\n");
    }
    else if (score2 > score1)
    {
