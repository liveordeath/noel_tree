# 🔍 Hướng dẫn Kiểm tra Project trên Vercel

## Bước 1: Truy cập Vercel Dashboard

1. **Mở trình duyệt** và truy cập: **https://vercel.com/dashboard**
2. **Đăng nhập** bằng GitHub account (nếu chưa đăng nhập)

---

## Bước 2: Tìm Project

Sau khi đăng nhập, bạn sẽ thấy:
- **Danh sách tất cả projects** của bạn
- Tìm project có tên: `noel_tree` hoặc `noel-tree`
- Hoặc project được kết nối với repository: `liveordeath/noel_tree`

---

## Bước 3: Xem Chi tiết Project

Click vào project để xem:

### Tab "Deployments"
- Danh sách tất cả các lần deploy
- Mỗi deployment có:
  - **Status**: ✅ Ready, 🔄 Building, ❌ Error
  - **Commit message**: Thông điệp commit
  - **Branch**: main, develop...
  - **URL**: Link để truy cập
  - **Time**: Thời gian deploy

### Tab "Settings"
- **General**: Tên project, framework
- **Git**: Repository được kết nối
- **Domains**: Domain tùy chỉnh
- **Environment Variables**: Biến môi trường

### Tab "Analytics" (nếu có)
- Số lượt truy cập
- Performance metrics

---

## Bước 4: Xem Logs

1. Click vào một **deployment** cụ thể
2. Xem **Build Logs**:
   - Quá trình build
   - Lỗi (nếu có)
   - Thời gian build

---

## Bước 5: Truy cập Website

### Production URL
- Thường là: `https://noel-tree.vercel.app`
- Hoặc: `https://noel-tree-[random].vercel.app`
- URL này được hiển thị ở đầu mỗi deployment

### Preview URLs
- Mỗi commit/pull request có URL riêng
- Format: `https://noel-tree-[hash].vercel.app`

---

## Nếu Chưa Thấy Project

### Cách 1: Import từ GitHub
1. Vào **https://vercel.com/new**
2. Click **"Import Git Repository"**
3. Chọn repository: `liveordeath/noel_tree`
4. Click **"Import"**
5. Cấu hình:
   - Framework Preset: **Other**
   - Root Directory: `./` (để trống)
   - Build Command: để trống
   - Output Directory: để trống
6. Click **"Deploy"**

### Cách 2: Kiểm tra GitHub Integration
1. Vào **Vercel Dashboard** → **Settings** → **Git**
2. Đảm bảo GitHub account đã được kết nối
3. Nếu chưa, click **"Connect GitHub"**

---

## Troubleshooting

### Không thấy project
- Kiểm tra đã đăng nhập đúng GitHub account chưa
- Kiểm tra repository đã public chưa (nếu là private repo, cần Vercel Pro)

### Deploy bị lỗi
- Xem **Build Logs** để biết lỗi cụ thể
- Kiểm tra `vercel.json` có đúng cấu hình không
- Đảm bảo file `index.html` tồn tại

### Website không load
- Kiểm tra URL có đúng không
- Hard refresh (Ctrl+F5 / Cmd+Shift+R)
- Kiểm tra console browser có lỗi không

---

## Quick Links

- **Vercel Dashboard**: https://vercel.com/dashboard
- **New Project**: https://vercel.com/new
- **Documentation**: https://vercel.com/docs

