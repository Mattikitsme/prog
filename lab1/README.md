# Отчет
Задание:\
Вывести частное наименьшей суммы цифр параметров a, b и второго параметра.

Блок-схема:\
![{FD33103B-7E3E-44CD-A7F7-2D5F946753C4}](https://github.com/user-attachments/assets/d044025b-23cd-4da7-9857-1be273e98aad)

```c
#include <stdio.h>

int sum_of_digits(int n) {
    int sum = 0;
    n = (n < 0) ? -n : n;
    while (n > 0) {
        sum += n % 10;
        n /= 10;
    }
    return sum;
}

int main() {
    int a, b;

    printf ("Введите число a -> ");
    scanf ("%d", &a);
    printf ("Введите число b -> ");
    scanf ("%d", &b);

    int sum_a = sum_of_digits(a);
    int sum_b = sum_of_digits(b);

    int min_sum = sum_a < sum_b ? sum_a : sum_b;

    if (min_sum == 0) {
        printf("Ошибка: Сумма равна нулю, деление невозможно.\n");
    } else {
        double quotient = min_sum / (double)b;
        printf ("Частное наименьшей суммы и второго параметра (b): %2f\n", quotient);
    }
    return 0;
}
```

Проверка работы:\
![Изображение](https://github.com/user-attachments/assets/cf10a74e-6d4b-44b4-8675-0c3522b81d31)

[Онлайн редактор блок-схем](https://programforyou.ru/block-diagram-redactor)
