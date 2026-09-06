# ถูกกว่ากี่บาท — เทียบราคาต่อน้ำหนัก

เว็บหน้าเดียว (static) สำหรับเทียบราคาต่อหน่วยของสินค้าหลายรายการ
รองรับการเทียบแบบ **น้ำหนัก / ปริมาตร / จำนวนชิ้น** ใส่ราคาได้ทั้งแบบรวมทั้งแพ็คและแยกราคาต่อชิ้น
แล้วสรุปให้ว่าอันไหนคุ้มกว่า และถูกกว่ากี่บาทต่อหน่วย

## ไฟล์

- `index.html` — ตัวเว็บทั้งหมด (HTML + CSS + JS อยู่ในไฟล์เดียว ไม่ต้อง build)
- `.github/workflows/pages.yml` — GitHub Actions สำหรับ deploy ขึ้น GitHub Pages
- `.nojekyll` — ปิดการประมวลผลด้วย Jekyll

## Auto deploy

ทุกครั้งที่ push ขึ้น branch `main` workflow `Deploy to GitHub Pages`
จะคัดลอก `index.html` (พร้อม `.nojekyll`) ไปวางที่ branch `gh-pages` ให้อัตโนมัติ
ไม่ต้องแตะอะไรอีก แก้ไฟล์แล้ว push อย่างเดียว

### ต้องกดเปิด Pages เองครั้งแรกครั้งเดียว

GitHub ไม่ยอมให้ token ของ Actions สร้าง Pages site ให้ (`Resource not accessible by
integration`) เจ้าของ repo ต้องเปิดเองรอบแรก

1. ไปที่ **Settings → Pages**
2. **Build and deployment → Source** เลือก **Deploy from a branch**
3. เลือก branch `gh-pages` folder `/ (root)` แล้วกด **Save**

จากนั้นทุก push เข้า `main` จะขึ้นเว็บให้เองภายในไม่กี่นาที

URL ที่ได้: `https://nattachai290.github.io/compare-price/`

## รันในเครื่อง

เปิดไฟล์ `index.html` ด้วยเบราว์เซอร์ได้เลย หรือ

```bash
python3 -m http.server 8000
# แล้วเปิด http://localhost:8000
```
