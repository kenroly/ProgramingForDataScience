<h1>Programming For Data Science</h1>

<h2>Quy trình sử dụng git</h2>

*Quy trình bắt đầu code một tính năng mới
git checkout master
git pull
git checkout -b <ten branch>

tên branch đặt theo quy tắc: <tên người code>/<chức năng code>

*Quy trình merge code vào master
Trong quá trình code, cần commit nhiều lần (mỗi tính năng) để chắc chắn rằng mình không bị sai. Và để hạn chế tình trạng mất dữ liệu do một nguyên nhân nào đó thì nên commit và push luôn.

**Quy trình commit code
git commit -m "message"     (Mô tả những gì mình đã code trong message trong cặp dấu nháy kép, nhớ save hết trước khi commit)
git push
Nếu push code lần đầu sau khi tạo branch sẽ cần set upstream thì khi git push sẽ hiện thông báo, chỉ cần copy câu thông báo paste lại vào terminal là được.

Sau khi code xong:
Bước 1: Kiểm tra kỹ xem các tính năng đã được commit hết chưa, đã push lên remote repository hết chưa.
Bước 2: Đem code qua Test-Branch để test, nếu ổn thì chuyển sang bước 3.
  Quy trình chuyển code để test
  git checkout Test-Branch
  git pull
  git pull origin <ten branch>
  Resolve Conflict nếu có
Bước 3: Sau khi test ổn, tạo Pull Request trên github, báo Hoàng test lại.
Bước 4: Nếu Hoàng test thấy ổn thì báo Đạt merge code vào master.