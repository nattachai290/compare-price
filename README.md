# ถูกกว่ากี่บาท — เทียบราคาต่อน้ำหนัก

เว็บหน้าเดียว (static) สำหรับเทียบราคาต่อหน่วยของสินค้าหลายรายการ
รองรับการเทียบแบบ **น้ำหนัก / ปริมาตร / จำนวนชิ้น** ใส่ราคาได้ทั้งแบบรวมทั้งแพ็คและแยกราคาต่อชิ้น
แล้วสรุปให้ว่าอันไหนคุ้มกว่า และถูกกว่ากี่บาทต่อหน่วย

## ไฟล์

- `index.html` — ตัวเว็บทั้งหมด (HTML + CSS + JS อยู่ในไฟล์เดียว ไม่ต้อง build)
- `.nojekyll` — ปิดการประมวลผลด้วย Jekyll

## Auto deploy

เปิด GitHub Pages ไว้แล้วแบบ **Deploy from a branch → `main` / `(root)`**
เพราะ `index.html` อยู่ที่ root ของ `main` อยู่แล้ว ทุกครั้งที่ push เข้า `main`
GitHub จะ build และขึ้นเว็บให้เองภายในไม่กี่นาที ไม่ต้องมี workflow อะไรเพิ่ม

ดูสถานะการ deploy แต่ละครั้งได้ที่แท็บ **Actions** (`pages-build-deployment`)
หรือที่ **Settings → Pages**

URL: `https://nattachai290.github.io/compare-price/`

## รันในเครื่อง

เปิดไฟล์ `index.html` ด้วยเบราว์เซอร์ได้เลย หรือ

```bash
python3 -m http.server 8000
# แล้วเปิด http://localhost:8000
```
