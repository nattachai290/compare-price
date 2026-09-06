# ถูกกว่ากี่บาท — เทียบราคาต่อน้ำหนัก

เว็บหน้าเดียว (static) สำหรับเทียบราคาต่อหน่วยของสินค้าหลายรายการ
รองรับการเทียบแบบ **น้ำหนัก / ปริมาตร / จำนวนชิ้น** ใส่ราคาได้ทั้งแบบรวมทั้งแพ็คและแยกราคาต่อชิ้น
แล้วสรุปให้ว่าอันไหนคุ้มกว่า และถูกกว่ากี่บาทต่อหน่วย

## ไฟล์

- `index.html` — ตัวเว็บทั้งหมด (HTML + CSS + JS อยู่ในไฟล์เดียว ไม่ต้อง build)
- `.github/workflows/pages.yml` — GitHub Actions สำหรับ deploy ขึ้น GitHub Pages
- `.nojekyll` — ปิดการประมวลผลด้วย Jekyll

## เปิดใช้งาน GitHub Pages (ต้องกดเปิดเองครั้งเดียว)

GitHub ไม่อนุญาตให้ token ของ Actions เปิด Pages ให้เอง เจ้าของ repo ต้องกดเปิดครั้งแรกเอง
ไปที่ **Settings → Pages** แล้วเลือกทางใดทางหนึ่ง

**ทางที่ 1 — GitHub Actions (workflow พร้อมแล้วในนี้)**

- **Build and deployment → Source** เลือก **GitHub Actions**
- แล้วสั่งรัน workflow `Deploy to GitHub Pages` อีกครั้ง (แท็บ Actions → Run workflow)
  หรือ push commit ใหม่ขึ้น `main` ก็ deploy อัตโนมัติ

**ทางที่ 2 — Deploy from a branch (ง่ายสุด ไม่ต้องใช้ Actions)**

- **Source** เลือก **Deploy from a branch** → branch `main`, folder `/ (root)` → Save
- เพราะ `index.html` อยู่ที่ root ของ `main` อยู่แล้ว เว็บจะขึ้นภายในไม่กี่นาที

URL ที่ได้: `https://nattachai290.github.io/compare-price/`

## รันในเครื่อง

เปิดไฟล์ `index.html` ด้วยเบราว์เซอร์ได้เลย หรือ

```bash
python3 -m http.server 8000
# แล้วเปิด http://localhost:8000
```
