# z-para_.c
A c program for z-parameters
#include <stdio.h>

int main()
{
    float V1_open, V2_open, I1;
    float V1_short, V2_short, I2;
    float Z11, Z12, Z21, Z22;

    printf("Z-PARAMETERS OF TWO-PORT NETWORK\n");

    // Test 1: I2 = 0
    printf("\nWhen I2 = 0 (Output Port Open):\n");

    printf("Enter V1 (V): ");
    scanf("%f", &V1_open);

    printf("Enter V2 (V): ");
    scanf("%f", &V2_open);

    printf("Enter I1 (A): ");
    scanf("%f", &I1);

    Z11 = V1_open / I1;
    Z21 = V2_open / I1;

    // Test 2: I1 = 0
    printf("\nWhen I1 = 0 (Input Port Open):\n");

    printf("Enter V1 (V): ");
    scanf("%f", &V1_short);

    printf("Enter V2 (V): ");
    scanf("%f", &V2_short);

    printf("Enter I2 (A): ");
    scanf("%f", &I2);

    Z12 = V1_short / I2;
    Z22 = V2_short / I2;

    // Display results
    printf("\n--- Z-PARAMETERS ---\n");
    printf("Z11 = %.2f Ohm\n", Z11);
    printf("Z12 = %.2f Ohm\n", Z12);
    printf("Z21 = %.2f Ohm\n", Z21);
    printf("Z22 = %.2f Ohm\n", Z22);

    return 0;
}