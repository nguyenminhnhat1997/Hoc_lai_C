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

```javacript
  char note[100];
  printf("Nhap vào kí tự ");
  gets(note); -> Nhap vào 'abc de'
  printf("%s",note); -> in ra 'abc de'
```

### 1 số hàm của thư viện <string.h>

- Sao chép chuỗi với hàm `strcpy()`

```javascript
   char note[100], ok[100];
  printf("Nhap vào kí tự ");
  gets(note); -> Nhap vào 'abc de'
  printf("%s",note); -> in ra 'abc de'
  strcopy(ok,"Nguyen minh nhat");
  printf("%s",ok); -> in ra 'Nguyễn Minh Nhật'
```

- Tạo bản sao của 1 chuỗi với hàm `strdup()`, tự tạo vùng nhớ chứa chuỗi s

```javascript
char *s;
s = strdup("Nguyen Minh Nhat");
printf("%s",s);
```
- Chuyển chuỗi  hoa thành chuỗi thường với hàm `strlwr`

```javascript
char note[]="MINH NHAT";
strlwr(note);
puts(note); -> in ra minh nhat.

```

- Chuyển chuỗi thường thành chuỗi hoa.

```javascript
char note[];
strupr(note);
puts(note);
```

- Đảo ngược thứ tự các kí tự trong chuỗi với hàm `strrev`.

```javascript
char note[] = "abc";
strrev(note);
puts(note);
```

- So sánh 2 chuỗi với hàm với hàm `strcmp(tr1,str2)`.

  -- trả về 0 nếu s1 = s2.

  -- trả về 1 nếu s1 > s2.

  -- trả về -1 nếu s1 < s2.


```javascript
char s1[] = "ABC";
char s2[] = "abc";
int kq = strcmp(s1,s2);
printf("%d",kq); -> trả -1
```

- So sánh 2 chuỗi không phân biệt hoa thường với hàm `stricmp`


```javascript
char s1[] = "ABC";
char s2[] = "abc";
int kq = strcmp(s1,s2);
printf("%d",kq); -> trả 0
```

- Nối chuỗi vs hàm `strcat(s1,s2)`.

```javascript
char s1[] = "ABC";
char s2[] = "abc";
char *s3;
s3 = strcat(s1,s2);
puts(s3);
```

- Tính độ dài của chuỗi với hàm `strlen()`.

```javascript
  char s1[] = "abc";
  int len = strlen(s1);
  printf("%d",len);
```

- Tìm vị trí xuất hiện đầu tiên của s1  trong s2 với hàm strstr(s1,s2) .

  -- trả về con trỏ đến đến vị trí xuất hiện đầu tiên của s2
  
  -- trả về null nếu không tìm thấy.
  
```javascript
char s1[] = "abc";
char s2[] = "a";
if(strstr(s1,s2))
{
  printf("Tim thay"); -> in ra tìm thấy
}else
printf("khong tim thay");
```


