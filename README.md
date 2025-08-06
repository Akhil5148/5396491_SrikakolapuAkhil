<img width="1918" height="901" alt="greatlearning" src="https://github.com/user-attachments/assets/ff7cc124-11ce-46b3-b481-ccb7dfa003eb" />
<img width="1096" height="775" alt="Screenshot 2025-08-06 130552" src="https://github.com/user-attachments/assets/343f2c16-bdcd-4c4f-af3c-f620cd479278" />
<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/c6ff8de4-1098-48c4-b678-c7945b0a1bd6" />
<img width="1920" height="1080" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/7acd9d08-f3d4-4a1a-9774-0236c293b192" />
<img width="1920" height="1080" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/969fd78c-c9f1-4a48-aa94-93339de3452a" />
<img width="1920" height="1080" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/a46290d7-ff86-4787-82fe-8ad704fc0ba3" />
<img width="1920" height="1080" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/65086560-88c8-4124-b894-ff69bfc22f44" />
<img width="1920" height="1080" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/39751fdd-23f8-4f3c-88a6-be4b912ab2d2" />
<img width="1920" height="1080" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/fb451543-a450-478a-b9ec-daa3ab563dcd" />
<img width="1920" height="1080" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/5e5b8c68-288c-4d87-9555-f66070dcd201" />
<img width="1920" height="1080" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/f980330c-edb9-4ff7-b946-c7f9bc1c528a" />
<img width="1920" height="1080" alt="Screenshot (16)" src="https://github.com/user-attachments/assets/2c5f9395-67c9-4c70-9985-997895398548" />
<img width="1920" height="1080" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/9997a7db-c3ed-4cbf-82d4-d16f38aa25f5" />
<img width="1920" height="1080" alt="Screenshot (18)" src="https://github.com/user-attachments/assets/aaec897a-f830-411b-8dbf-9f5cb3476097" />
[Plus Minus.c.txt](https://github.com/user-attachments/files/21613258/Plus.Minus.c.txt)#include <stdio.h>

void plusMinus(int arr[], int n) {
    int positive = 0, negative = 0, zero = 0;
    for(int i = 0; i < n; i++) {
        if(arr[i] > 0)
            positive++;
        else if(arr[i] < 0)
            negative++;
        else
            zero++;
    }
    printf("%.6f\n", (float)positive / n);
    printf("%.6f\n", (float)negative / n);
    printf("%.6f\n", (float)zero / n);
}

int main() {
    int n;
    scanf("%d", &n);
    int arr[n];
    for(int i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    plusMinus(arr, n);
    return 0;
}
[Mini-Max Sum.c.txt](https://github.com/user-attachments/files/21613261/Mini-Max.Sum.c.txt)
#include <stdio.h>

int main() {
    long arr[5];
    long sum = 0, min, max;
    
    // Input 5 numbers
    for (int i = 0; i < 5; i++) {
        scanf("%ld", &arr[i]);
        sum += arr[i];
    }

    min = arr[0];
    max = arr[0];
    
    // Find min and max
    for (int i = 1; i < 5; i++) {
        if (arr[i] < min) min = arr[i];
        if (arr[i] > max) max = arr[i];
    }

    // Calculate the required sums
    long min_sum = sum - max;
    long max_sum = sum - min;

    printf("%ld %ld\n", min_sum, max_sum);

    return 0;
}
[Time Conversion.c.txt](https://github.com/user-attachments/files/21613264/Time.Conversion.c.txt)#include <stdio.h>
#include <string.h>

int main() {
    char s[11];
    int hour, minute, second;
    char period[3];

    // Read input as string
    scanf("%s", s);

    // Parse input: hour, minute, second, AM/PM
    sscanf(s, "%2d:%2d:%2d%2s", &hour, &minute, &second, period);

    // Convert to 24-hour format
    if (strcmp(period, "PM") == 0 && hour != 12) {
        hour += 12;
    }
    if (strcmp(period, "AM") == 0 && hour == 12) {
        hour = 0;
    }

    // Print in 24-hour format (with leading zeroes)
    printf("%02d:%02d:%02d\n", hour, minute, second);

    return 0;
}

