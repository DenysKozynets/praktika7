Практична робота №7 Козинець Денис КН23001б
    
    
    #include <stdio.h>
    #include <math.h>

    int main() {
    double x1, y1, r1, x2, y2, r2;
    scanf("%lf %lf %lf %lf %lf %lf", &x1, &y1, &r1, &x2, &y2, &r2);

    // Вычисляем расстояние между центрами кругов
    double d = sqrt((x2 - x1) * (x2 - x1) + (y2 - y1) * (y2 - y1));

    if (d == 0 && r1 == r2) {
        // Круги совпадают
        printf("-1\n");
    } else if (d > r1 + r2 || d < fabs(r1 - r2)) {
        // Круги не пересекаются
        printf("0\n");
    } else if (d == r1 + r2 || d == fabs(r1 - r2)) {
        // Круги касаются в одной точке
        printf("1\n");
    } else {
        // Круги пересекаются в двух точках
        printf("2\n");
    }

    return 0;
    }
