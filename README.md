#include <stdio.h>
#include <conio.h>
#include <stdlib.h>

void recursiveArray(int arr[], int n, int index);
void inputStudentsAndSort();

int main() {
    int choice;
    do {
        system("cls"); // Xóa màn hình console
        printf("===== MENU =====\n");
        printf("1. Sử dụng đệ quy để nhập xuất mảng và tính tổng số nguyên tố\n");
        printf("2. Nhập và sắp xếp danh sách sinh viên\n");
        printf("0. Thoát\n");
        printf("Nhập lựa chọn: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1: {
                int n;
                printf("Nhập số phần tử của mảng: ");
                scanf("%d", &n);
                int arr[n];

                printf("Nhập các phần tử của mảng:\n");
                recursiveArray(arr, n, 0);

                // Hiển thị mảng và tính tổng số nguyên tố
                // Bạn có thể viết các hàm khác để thực hiện công việc này
                // Tạm thời, mình sẽ in ra các giá trị để bạn hiểu cấu trúc chương trình
                printf("\nMảng vừa nhập: ");
                for (int i = 0; i < n; i++) {
                    printf("%d ", arr[i]);
                }
                printf("\n");
                break;
            }
            case 2: {
                inputStudentsAndSort();
                break;
            }
            case 0: {
                printf("Chương trình kết thúc.\n");
                break;
            }
            default:
                printf("Lựa chọn không hợp lệ. Vui lòng chọn lại.\n");
        }

        printf("\nNhấn phím bất kỳ để tiếp tục...");
        getch(); // Đợi người dùng nhấn một phím bất kỳ
    } while (choice != 0);

    return 0;
}

// Hàm đệ quy để nhập xuất mảng và tính tổng số nguyên tố
void recursiveArray(int arr[], int n, int index) {
    if (index < n) {
        printf("Nhập phần tử thứ %d: ", index + 1);
        scanf("%d", &arr[index]);
        recursiveArray(arr, n, index + 1);
    }
}

// Hàm nhập và sắp xếp danh sách sinh viên
void inputStudentsAndSort() {
    // Bạn có thể thêm mã nguồn cho chức năng này tương tự như bài tập trước
    // Sử dụng các hàm để nhập thông tin sinh viên và sắp xếp danh sách
    // In danh sách sinh viên ra màn hình
    printf("Chức năng này chưa được triển khai. Bạn có thể thêm mã nguồn cho chức năng này.\n");
}
