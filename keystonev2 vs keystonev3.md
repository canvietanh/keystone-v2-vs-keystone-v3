#Cập nhật sự khác biết keystonev3 so với keystonev2


##Ưu điểm với keystone v3:

1) Việc chứng thực hoàn toàn được modul hóa. Bạn hoàn toàn có thể tùy chỉnh việc chứng thực đối với người dùng trong project. Và vì nó là phương thức xác thực mở rông nên keystone hỗ trợ chuẩn mở như oauth1 (open standard for authorization), federation (nhưng đối với federation thì chưa hoàn thiện)

2) Phân quyền đối với V2 chỉ có "admin" hoặc tất cả mọi người, tuy nhiên trên v3 bạn có thể kiểm soát được việc ai muốn sử dụng phương thức nào (Cung cấp khả năng cho phép bạn định nghĩa chính sách riêng của bạn trong file policy)

3) Việc xác định danh tính và phân công được sử dụng driver khác nhau và riêng biệt

4) Hỗ trợ tập lệnh API nhiều hơn so với v2.0

5) Keystonev3 được cập nhật thêm tính tăng về miền (domains) và nhóm(group)

Miền đại diện cho tập hợp những người dùng, nhóm hay dự án. Người dùng liên quan đến nhiều dự án khác nhau bởi những quyền được cấp đối với từng dự án đó bao gồm kể cả những dự án thuộc các miền khác. Người dùng có thể liên quan đến nhiều miền khác nhau theo 1 cách như vậy.

##Keystonev2
Đối với API keystone v2, mọi hoat động đều trên 1 miền mặc định. Ví dụ như nếu bạn tạo 1 người dùng, nhóm hay dự án thì nó đều được tạo trên 1 miền mặc định.
 
 Ví dụ dư trên keystonev2, mỗi người dùng ở trên nhiều dự án khác nhau với quyền khác nhau. Ví dụ người dùng A có quyền admin ở project A nhưng lại có quyền member ở Project B nhưng với Keystonev3, các project được phân vào các domain khác nhau
 

##Keyston v3 sử dụng câu lệnh là OpenStack còn đối với keystonev2 sử dụng Keystone 