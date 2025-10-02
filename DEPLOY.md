# 🚀 วิธีการ Deploy บน GitHub Pages

## ขั้นตอนการอัปโหลดไปยัง GitHub

### 1. สร้าง Repository บน GitHub
1. ไปที่ [GitHub.com](https://github.com)
2. คลิก **"New repository"**
3. ตั้งชื่อ repository เช่น `training-dashboard-pwa`
4. เลือก **Public** (สำหรับ GitHub Pages ฟรี)
5. **ไม่ต้อง** เลือก "Initialize with README"
6. คลิก **"Create repository"**

### 2. เชื่อมต่อ Local Repository กับ GitHub
```powershell
# เพิ่ม remote origin (แทนที่ YOUR_USERNAME และ YOUR_REPO_NAME)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# ตั้งชื่อ branch หลักเป็น main
git branch -M main

# Push ไฟล์ทั้งหมดขึ้น GitHub
git push -u origin main
```

### 3. เปิดใช้งาน GitHub Pages
1. ไปที่หน้า repository บน GitHub
2. คลิก **Settings** (แท็บด้านบน)
3. เลื่อนลงหา **"Pages"** ในเมนูซ้าย
4. ในส่วน **Source** เลือก **"Deploy from a branch"**
5. เลือก **branch: main** และ **folder: / (root)**
6. คลิก **Save**

### 4. เข้าถึงเว็บไซต์
- GitHub จะสร้าง URL ให้อัตโนมัติ: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME`
- อาจใช้เวลา 5-10 นาทีในการ deploy ครั้งแรก

## 📋 ไฟล์ที่มีใน Repository

- `index.html` - หน้าหลักของ Dashboard (Interactive)
- `training-dashboard.html` - ไฟล์ต้นฉบับ
- `home.html` - หน้า Landing Page
- `README.md` - คำอธิบายโครงการ
- `.gitignore` - ไฟล์ที่ไม่ต้อง track ใน Git

## 🔄 การอัปเดตเว็บไซต์

เมื่อมีการแก้ไข:
```powershell
# เพิ่มไฟล์ที่แก้ไข
git add .

# Commit การเปลี่ยนแปลง
git commit -m "Update: คำอธิบายการแก้ไข"

# Push ขึ้น GitHub
git push origin main
```

## 🌟 คุณสมบัติ GitHub Pages

✅ **ฟรี** สำหรับ public repository  
✅ **Custom Domain** สามารถใช้โดเมนตัวเองได้  
✅ **HTTPS** รองรับ SSL อัตโนมัติ  
✅ **Auto Deploy** อัปเดตทุกครั้งที่ push  
✅ **CDN** เร็วทั่วโลก  

## 🎯 ตัวอย่าง URL
- หลังจาก deploy แล้ว: `https://yourusername.github.io/training-dashboard-pwa`
- หน้าหลัก (Dashboard): `/` 
- Landing Page: `/home.html`

---
🚀 **พร้อมใช้งานแล้ว!** Dashboard จะพร้อมใช้งานบนอินเทอร์เน็ต