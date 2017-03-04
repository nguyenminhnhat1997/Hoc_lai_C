## Chuỗi

- Biến char chỉ lưu được 1 kí tự, -> ta phải sử dụng mảng.

- Chuỗi kí tự kết thúc bằng "\0" (null)

- Độ dài của chuỗi = độ dài của mảng - 1.

*Ví dụ*: ten[30]; / độ dài 29.

### Khởi tạo.

1 Khởi tạo thông thường:

char[10] = {'N','h','\0'};

char[10] = "Nh k"; tự thêm \0.

2 Khởi tạo tự xác định độ dài

char[] = "ok ok ok ok";

### In ra màn hình

- printf với `%s`

```javascript
  char note[] = "Minh nhat";
  printf("%s",note); -> không xuống dòng
```
- sử dụng `puts`.

```javascript
  char note[] = "Minh nhat";
  puts(note);
  printf("%s",note); -> tự xuống dòng
```

- nhập chuỗi sử dụng `scanf` in ra chỉ nhận kí tự nhưng khi gặp dấu `space` thì nó in ra bỏ qua các kí tự phía sau.

```javascript
  char note[100];
  printf("Nhap vao ki tự"); 
  scanf("%s",note); -> nhập vào 'abc d'
  printf("%s",note); -> in ra 'abc'
```

- Nhập chuỗi sử dụng `gets` in rakis tự cho đến khi gặp kí tự xuống dòng.

```javacrip
