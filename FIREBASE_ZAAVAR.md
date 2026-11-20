# Firebase холбох заавар (нэг удаа, ~10 минут)

Хоёр сайт («Түргэн Тоншуул», «Оддын хөтөч») **нэг Firebase төсөл** ашиглана.

## 1. Төсөл үүсгэх
1. https://console.firebase.google.com руу Google бүртгэлээрээ орно.
2. **Add project** → нэр: `surguuli130-mit` (дурын) → Google Analytics-ийг унтраагаад **Create**.

## 2. Нэргүй нэвтрэлтийг асаах
**Build → Authentication → Get started → Sign-in method → Anonymous → Enable → Save**.

## 3. Realtime Database үүсгэх
1. **Build → Realtime Database → Create Database**.
2. Байршил: **Singapore (asia-southeast1)** → **Start in locked mode** → Enable.
3. **Rules** таб дээр `database.rules.json` файлын агуулгыг бүхэлд нь хуулж тавиад **Publish** дарна.

## 4. Тохиргоогоо авах
1. Төслийн нүүр → **</> (Web)** дүрс → app nickname: `site` → **Register app**.
2. Гарч ирэх `firebaseConfig` дотроос **apiKey** ба **databaseURL** хоёрыг хуулна.
   (databaseURL харагдахгүй бол Realtime Database хуудасны дээд талд байгаа `https://...firebasedatabase.app` хаяг.)

## 5. Сайтдаа оруулах
Хоёр сайтын `firebase-config.js` файлыг нээгээд:
```js
window.FIREBASE_CONFIG = {
  apiKey: "AIza....",
  databaseURL: "https://surguuli130-mit-default-rtdb.asia-southeast1.firebasedatabase.app"
};
```
GitHub дээр хоёр repository-д `index.html`, `sync.js`, `firebase-config.js` болон `data` хавтсыг шинэчилнэ.

## 6. Шалгах
- Багшийн самбарын дээд буланд **● Шууд холбогдсон** гэж ногоон гарна.
- Шинэ сан хоосон эхэлнэ: багш `bagsh` / `1234`-өөр нэвтэрч, **нууц үгээ заавал солино**.
- Сурагчид шинээр бүртгүүлнэ (хуучин зөвхөн нэг компьютерт хадгалагдсан бүртгэл орохгүй).

## Хэрхэн ажилладаг вэ
- Сурагч бүртгүүлэх, дасгал, шалгалт, үнэлгээ хийх бүрт зөвхөн тэр сурагчийн өөрчлөлт сан руу илгээгдэнэ.
- Багшийн самбар нээлттэй байхад шинэ дүн автоматаар (1–2 секундэд) гарч ирнэ.
- Багш хичээл/шалгалт нээхэд сурагчдын дэлгэц автоматаар шинэчлэгдэнэ.
- Интернэт тасарвал ажил тухайн компьютерт түр хадгалагдаж, холболт сэргэмэгц илгээгдэнэ.
