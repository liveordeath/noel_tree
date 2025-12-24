# Hướng dẫn Deploy Christmas Tree Project

## Phương án 1: GitHub Pages (Khuyến nghị - Miễn phí)

### Bước 1: Tạo GitHub Repository
1. Đăng nhập vào GitHub
2. Tạo repository mới (ví dụ: `christmas-tree-3d`)
3. **Quan trọng**: Đặt repository là **Public** (GitHub Pages miễn phí chỉ cho public repo)

### Bước 2: Upload code lên GitHub
```bash
# Trong thư mục project
git init
git add .
git commit -m "Initial commit: Christmas Tree 3D with photos"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/christmas-tree-3d.git
git push -u origin main
```

### Bước 3: Enable GitHub Pages
1. Vào repository trên GitHub
2. Settings → Pages
3. Source: chọn `main` branch
4. Folder: chọn `/ (root)`
5. Save

### Bước 4: Truy cập website
- URL sẽ là: `https://YOUR_USERNAME.github.io/christmas-tree-3d/christmas_tree_touch&gesture.html`
- Hoặc có thể đổi tên file thành `index.html` để truy cập trực tiếp

---

## Phương án 2: Netlify (Nhanh nhất - Miễn phí)

### Cách 1: Drag & Drop
1. Truy cập: https://app.netlify.com/drop
2. Kéo thả toàn bộ thư mục project vào
3. Netlify sẽ tự động deploy và cung cấp URL

### Cách 2: Kết nối GitHub
1. Đăng nhập Netlify
2. New site from Git
3. Chọn GitHub repository
4. Deploy settings: Build command để trống, Publish directory: `/`
5. Deploy

**URL sẽ là**: `https://random-name.netlify.app/christmas_tree_touch&gesture.html`

---

## Phương án 3: Vercel (Nhanh - Miễn phí) ⭐ ĐÃ CẤU HÌNH SẴN

### Cách 1: Deploy qua Vercel CLI (Khuyến nghị)

1. **Cài đặt Vercel CLI** (nếu chưa có):
```bash
npm i -g vercel
```

2. **Đăng nhập Vercel**:
```bash
vercel login
```

3. **Deploy project**:
```bash
# Trong thư mục project
vercel
```

4. **Follow các bước**:
   - Set up and deploy? → **Y**
   - Which scope? → Chọn account của bạn
   - Link to existing project? → **N** (lần đầu)
   - Project name? → Nhấn Enter (hoặc đặt tên)
   - Directory? → Nhấn Enter (deploy từ root)
   - Override settings? → **N**

5. **Xong!** Vercel sẽ cung cấp URL như: `https://your-project-name.vercel.app`

### Cách 2: Deploy qua GitHub (Tự động)

1. **Tạo GitHub repository** (nếu chưa có):
```bash
git init
git add .
git commit -m "Initial commit"
# Tạo repo trên GitHub và push code
```

2. **Kết nối với Vercel**:
   - Truy cập: https://vercel.com
   - Đăng nhập bằng GitHub
   - Click "Add New Project"
   - Import GitHub repository
   - Framework Preset: **Other**
   - Root Directory: `./` (để trống)
   - Build Command: để trống
   - Output Directory: để trống
   - Click "Deploy"

3. **Tự động deploy**: Mỗi lần push code lên GitHub, Vercel sẽ tự động deploy lại

### Cách 3: Drag & Drop (Nhanh nhất)

1. Truy cập: https://vercel.com/new
2. Đăng nhập
3. Kéo thả toàn bộ thư mục project vào
4. Vercel sẽ tự động deploy

**URL sẽ là**: `https://your-project-name.vercel.app`
- Trang chủ: `https://your-project-name.vercel.app/` (sẽ redirect đến christmas_tree_touch&gesture.html)
- Trang chính: `https://your-project-name.vercel.app/christmas_tree_touch&gesture.html`

---

## Lưu ý quan trọng

1. **HTTPS bắt buộc**: Camera/Webcam chỉ hoạt động trên HTTPS hoặc localhost
2. **File size**: Đảm bảo các file ảnh không quá lớn (nên optimize trước khi deploy)
3. **CORS**: Nếu gặp lỗi CORS, cần cấu hình server headers

---

## Tối ưu hóa trước khi deploy

Nếu muốn file `christmas_tree_touch&gesture.html` là trang chủ:
- Đổi tên file thành `index.html`
- Hoặc tạo file `index.html` redirect đến `christmas_tree_touch&gesture.html`

