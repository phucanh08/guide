[<- Trở về](../README.md#conventions)

# Commit Conventions 

[Tham khảo](https://viblo.asia/p/lam-the-nao-de-viet-conventional-commits-cho-de-su-dung-07LKXbb2lV4)

### Mục lục
- [Cấu trúc của commit message](#cấu-trúc-của-commit-message)
- [Type Commit](#type-commit)

# Cấu trúc của commit message
```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```
Trong đó:

* Các thành phần type, description là bắt buộc cần có trong commit message, optional là tùy chọn có hoặc không có cũng được
* type: từ khóa để phân loại commit là feature, fix bug, refactor.
* scope: cũng được dùng để phân loại commit, vùng ảnh hưởng của commit, trả lời câu hỏi: commit này refactor|fix cái gì? được đặt trong cặp ngoặc đơn ngay sau type. VD: feat(authentication):, fix(parser):
* description: là mô tả ngắn về những gì sẽ bị sửa đổi trong commit đấy
* body: là mô tả dài và chi tiết hơn, cần thiết khi description chưa thể nói rõ hết được, có thể thêm phần ghi chú bằng các keyword
* footer: một số thông tin mở rộng như số ID của pull request, issue.. được quy định theo conventional

Một số ví dụ ngắn gọn:

```
feat: add validate of A feature

fix: fix die dashboard page

feat(feature_a): add validate of A1 feature
```
# Type Commit

Một số type phổ biến được khuyên sử dụng bao gồm:

* `feat`: thêm một feature
* `fix`: fix bug cho hệ thống, vá lỗi trong codebase
* `refactor`: sửa code nhưng không fix bug cũng không thêm feature hoặc đôi khi bug cũng được fix từ việc refactor.
* `docs`: thêm/thay đổi document
* `chore`: những sửa đổi nhỏ nhặt không liên quan tới code
* `style`: những thay đổi không làm thay đổi ý nghĩa của code như thay đổi css/ui chẳng hạn.
* `perf`: code cải tiến về mặt hiệu năng xử lý
* `vendor`: cập nhật version cho các dependencies, packages.

Ngoài ra, với mỗi dự án type này chúng ta có thể custom thêm được theo ý định (vì cũng chỉ để phân loại thôi), vd: Optimize, Bump, Drop, ...

>Note: Cái này quan trọng, dĩ nhiên phải làm rồi là nội dung của commit phải phù hợp với tương tác và ảnh hưởng của đoạn code được sửa trong commit. Chứ ko phải kiểu fix bug => ghi là feat =)). Rất khó để đọc và hiểu.


<style>
code {
  color: #d22778;
  font-weight: bold;
  background-color: #0e2233;
  border-radius: 2px;
  padding: 2px 5px;
  margin: 0 2px;
}
</style>