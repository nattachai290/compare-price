# ถูกกว่ากี่บาท — เทียบราคาต่อน้ำหนัก

เว็บหน้าเดียว (static) สำหรับเทียบราคาต่อหน่วยของสินค้าหลายรายการ
รองรับการเทียบแบบ **น้ำหนัก / ปริมาตร / จำนวนชิ้น** ใส่ราคาได้ทั้งแบบรวมทั้งแพ็คและแยกราคาต่อชิ้น
แล้วสรุปให้ว่าอันไหนคุ้มกว่า และถูกกว่ากี่บาทต่อหน่วย

## ไฟล์

- `index.html` — ตัวเว็บทั้งหมด (HTML + CSS + JS อยู่ในไฟล์เดียว ไม่ต้อง build)
- `.github/workflows/pages.yml` — GitHub Actions สำหรับ deploy ขึ้น GitHub Pages
- `.nojekyll` — ปิดการประมวลผลด้วย Jekyll

## เปิดใช้งาน GitHub Pages

1. ไปที่ **Settings → Pages** ของ repo นี้
2. ที่หัวข้อ **Build and deployment → Source** เลือก **GitHub Actions**
3. ทุกครั้งที่ push ขึ้น branch `main` เว็บจะถูก deploy อัตโนมัติ

URL ที่ได้: `https://nattachai290.github.io/compare-price/`

## รันในเครื่อง

เปิดไฟล์ `index.html` ด้วยเบราว์เซอร์ได้เลย หรือ

```bash
python3 -m http.server 8000
# แล้วเปิด http://localhost:8000
```
