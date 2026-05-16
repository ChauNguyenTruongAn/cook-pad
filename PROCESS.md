# Tuần 1

## Authentication Module

### 🗓 15/05/2026

* Xây dựng API cho chức năng Login
* Tích hợp ASP.NET Identity
* Xử lý xác thực bằng Email + Password
* Sinh JWT Token cho người dùng sau khi đăng nhập thành công

---

# Recipe Feature Development

## Bước 1: Xây dựng Backend cho Module Recipes

Dựa trên database schema, một bài viết công thức không chỉ nằm ở bảng `Recipes` mà còn liên quan đến:

* Recipe Images
* Recipe Ingredients
* Instruction Steps
* Categories
* Tags

### Categories & Tags API

Tạo các API hỗ trợ frontend lấy dữ liệu danh mục và thẻ:

```http
GET /api/categories
GET /api/tags
```

Frontend sẽ sử dụng dữ liệu này để hiển thị:

* Dropdown danh mục (`<select>`)
* Tag selector khi người dùng viết công thức

---

### Recipes CRUD API

#### Tạo các Entity:

* `RecipeEntity`
* `RecipeIngredient`
* `InstructionStep`
* `RecipeImage`

#### Xây dựng API:

```http
POST /api/recipes
```

### Yêu cầu:

* Nhận dữ liệu từ form tạo công thức
* Lưu Recipe chính
* Đồng thời xử lý:

  * Danh sách nguyên liệu (`RecipeIngredients`)
  * Các bước thực hiện (`InstructionSteps`)
  * Hình ảnh công thức (`RecipeImages`)

### Lưu ý:

Cần xử lý transaction hoặc save đồng bộ để đảm bảo dữ liệu nhất quán.

---

# Bước 2: Xây dựng Frontend - Trang Khám Phá (Home Page)

Thay vì làm form phức tạp trước, ưu tiên xây dựng giao diện hiển thị để có trải nghiệm trực quan sớm hơn.

## Micro Component: `RecipeCard`

Hiển thị:

* Ảnh bìa (`CoverImageUrl`)
* Tiêu đề món ăn (`Title`)
* Tên tác giả (`Author.DisplayName`)
* Thời gian nấu (`CookTimeMinutes`)
* Lượt yêu thích (`FavoriteCount`)

---

## HomePage

### API sử dụng:

```http
GET /api/recipes
```

### Yêu cầu:

* Fetch danh sách công thức từ backend
* Render danh sách bằng `RecipeCard`
* Hiển thị dạng Grid Layout
* Tích hợp vào `UserLayout`

---

# Bước 3: Xây dựng Frontend - Form "Viết Công Thức"

Đây là phần phức tạp nhất của phía User Frontend.

## Dynamic Form Features

### Người dùng có thể:

* Thêm/Xóa nguyên liệu động
* Thêm/Xóa bước nấu động
* Upload ảnh cho:

  * Ảnh bìa món ăn
  * Ảnh minh họa từng bước

---

## Recipe Ingredients

Cho phép:

```text
+ Thêm nguyên liệu
+ Xóa nguyên liệu
```

Ví dụ:

* 200g thịt bò
* 2 quả trứng
* 1 muỗng muối

---

##  Instruction Steps

Cho phép:

```text
+ Thêm bước làm
+ Upload ảnh cho từng bước
```

Ví dụ:

1. Sơ chế nguyên liệu
2. Ướp gia vị
3. Nấu trong 20 phút

---

## Upload Ảnh

Tích hợp dịch vụ upload ảnh:

* Cloudinary (khuyến nghị)

### Dữ liệu cần lưu:

* `CoverImageUrl`
* `InstructionStep.ImageUrl`

---

# Mục tiêu

## Backend

* Hoàn thành Authentication API
* Hoàn thành Recipes CRUD cơ bản
* Hoàn thành Categories & Tags API

## Frontend

* Hoàn thành Home Page
* Hoàn thành RecipeCard component
* Hoàn thành Dynamic Recipe Form cơ bản

---

# 🛠 Tech Stack

## Backend

* ASP.NET Core Web API
* Entity Framework Core
* ASP.NET Identity
* JWT Authentication

## Frontend

* React
* React Router
* Axios
* CSS Modules / Tailwind / SCSS

## Cloud

* Cloudinary (Image Upload)
