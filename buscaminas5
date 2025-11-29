#include <stdio.h>

// ==================================================
//        PARTE 5 — VISUALIZACIÓN Y ARCHIVOS
// ==================================================


// -----------------------------
// IMPRIMIR TABLERO VISIBLE
// -----------------------------
void imprimirVisible(char visible[][30], int filas, int columnas)
{
    printf("\n    ");
    for (int c = 0; c < columnas; c++)
        printf("%d ", c);
    printf("\n");

    for (int f = 0; f < filas; f++) {
        printf("%2d  ", f);
        for (int c = 0; c < columnas; c++) {
            printf("%c ", visible[f][c]);
        }
        printf("\n");
    }
    printf("\n");
}


// -----------------------------
// MOSTRAR TABLERO FINAL (CON MINAS)
// -----------------------------
void mostrarFinal(char real[][30], int filas, int columnas)
{
    printf("\n=== TABLERO FINAL ===\n");

    printf("    ");
    for (int c = 0; c < columnas; c++)
        printf("%d ", c);
    printf("\n");

    for (int f = 0; f < filas; f++) {
        printf("%2d  ", f);
        for (int c = 0; c < columnas; c++) {
            printf("%c ", real[f][c]);
        }
        printf("\n");
    }
    printf("\n");
}


// -----------------------------
// GUARDAR ESTADÍSTICAS
// -----------------------------
void guardarEstadisticas(int gano, int minas, int filas, int columnas)
{
    FILE *archivo = fopen("estadisticas.txt", "a");

    if (archivo == NULL) {
        printf("Error al abrir archivo de estadísticas.\n");
        return;
    }

    fprintf(archivo,
            "Resultado: %s | Minas: %d | Tablero: %dx%d\n",
            gano ? "GANÓ" : "PERDIÓ",
            minas, filas, columnas
    );

    fclose(archivo);
}


// -----------------------------
// OPCIONAL: imprimir el tablero real
// (Sirve para debug)
// -----------------------------
void imprimirReal(char real[][30], int filas, int columnas)
{
    printf("\n--- TABLERO REAL (DEBUG) ---\n");
    for (int f = 0; f < filas; f++) {
        for (int c = 0; c < columnas; c++) {
            printf("%c ", real[f][c]);
        }
        printf("\n");
    }
}

