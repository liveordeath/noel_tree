# 🚀 Hướng dẫn Deploy lên Vercel qua GitHub

## ✅ Bước 1: Tạo GitHub Repository

1. **Truy cập GitHub**: https://github.com/new
2. **Điền thông tin**:
   - Repository name: `christmas-tree-3d` (hoặc tên bạn muốn)
   - Description: `3D Christmas Tree with gesture control and photos`
   - **Public** hoặc **Private** (tùy bạn)
   - **KHÔNG** tích vào "Add a README file" (đã có sẵn)
   - **KHÔNG** tích vào "Add .gitignore" (đã có sẵn)
   - **KHÔNG** tích vào "Choose a license" (đã có sẵn)
3. Click **"Create repository"**

---

## ✅ Bước 2: Push Code lên GitHub

Sau khi tạo repository, GitHub sẽ hiển thị hướng dẫn. Chạy các lệnh sau trong terminal:

```bash
# Thay YOUR_USERNAME và REPO_NAME bằng thông tin của bạn
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git push -u origin main
```

**Hoặc nếu bạn dùng SSH:**
```bash
git remote add origin git@github.com:YOUR_USERNAME/REPO_NAME.git
git push -u origin main
```

**Ví dụ:**
```bash
git remote add origin https://github.com/joker/christmas-tree-3d.git
git push -u origin main
```

---

## ✅ Bước 3: Kết nối với Vercel

### Cách 1: Qua Web Interface (Khuyến nghị)

1. **Truy cập Vercel**: https://vercel.com
2. **Đăng nhập** bằng GitHub account
3. Click **"Add New Project"** hoặc **"Import Project"**
4. **Chọn GitHub repository** vừa tạo
5. **Cấu hình Project**:
   - **Framework Preset**: `Other` hoặc `Other`
   - **Root Directory**: `./` (để trống)
   - **Build Command**: để trống
   - **Output Directory**: để trống
   - **Install Command**: để trống
6. Click **"Deploy"**

### Cách 2: Qua Vercel CLI

```bash
# Cài đặt Vercel CLI (nếu chưa có)
npm i -g vercel

# Đăng nhập
vercel login

# Deploy
vercel

# Follow các bước:
# - Set up and deploy? → Y
# - Which scope? → Chọn account
# - Link to existing project? → N (lần đầu)
# - Project name? → Enter
# - Directory? → Enter
```

---

## ✅ Bước 4: Xem Website

Sau khi deploy xong, Vercel sẽ cung cấp URL:
- **Production URL**: `https://your-project-name.vercel.app`
- **Trang chủ**: `https://your-project-name.vercel.app/` (tự động redirect)
- **Trang chính**: `https://your-project-name.vercel.app/christmas_tree_touch&gesture.html`

---

## 🔄 Tự động Deploy

Sau khi kết nối với GitHub, mỗi lần bạn:
- Push code mới lên GitHub
- Merge Pull Request

Vercel sẽ **tự động deploy lại** website với code mới nhất!

---

## 📝 Lưu ý

1. **HTTPS**: Vercel tự động cung cấp HTTPS, camera sẽ hoạt động bình thường
2. **Custom Domain**: Có thể thêm domain riêng trong Vercel Dashboard
3. **Environment Variables**: Nếu cần, thêm trong Vercel Dashboard → Settings → Environment Variables

---

## 🆘 Troubleshooting

### Lỗi: "Build failed"
- Kiểm tra `vercel.json` đã đúng chưa
- Đảm bảo file `index.html` tồn tại

### Lỗi: "404 Not Found"
- Kiểm tra đường dẫn file trong HTML
- Đảm bảo file `assets/` được upload đầy đủ

### Camera không hoạt động
- Đảm bảo đang dùng HTTPS (Vercel tự động có)
- Cho phép quyền camera trong browser

