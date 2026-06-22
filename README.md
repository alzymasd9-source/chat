# Chat - شات دردشة فورية

مشروع دردشة فورية بواجهة بسيطة وسهلة الاستخدام، يهدف إلى توفير تجربة محادثة مباشرة وسريعة مع إمكانية تطويره لاحقًا وإضافة خصائص أكثر تقدمًا.

---

## نبذة عن المشروع

هذا المشروع عبارة عن واجهة دردشة (Chat Interface) مبنية بتقنيات الويب الأساسية، ومناسبة كنقطة بداية لتطوير تطبيق شات متكامل يدعم الرسائل الفورية، المستخدمين، المجموعات، والإشعارات.

---

## المميزات

- واجهة دردشة بسيطة وسهلة الاستخدام
- تصميم خفيف وسريع
- مناسب للتطوير والتخصيص
- قابل للربط مع Back-End مستقبلًا
- هيكل بسيط للمبتدئين

---

## التقنيات المستخدمة

- HTML
- CSS
- JavaScript
- XML

---

## هيكل المشروع

```bash
chat/
│
├── README.md
├── index.html
├── style.css
├── script.js
├── group_admin_background_v2.xml
└── assets/
```

> ملاحظة: يفضل إعادة تسمية الملفات ذات الأسماء العشوائية داخل المستودع إلى أسماء واضحة ومنظمة.

---

## التثبيت

### 1) استنساخ المشروع

```bash
git clone https://github.com/alzymasd9-source/chat.git
cd chat
```

### 2) فتح المشروع

يمكنك فتح المشروع مباشرة من خلال ملف:

```bash
index.html
```

أو باستخدام **Live Server** داخل VS Code.

---

## التشغيل

### تشغيل مباشر

افتح ملف `index.html` في أي متصفح مثل:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge

### تشغيل باستخدام Live Server

إذا كنت تستخدم VS Code:

1. افتح مجلد المشروع
2. ثبّت إضافة **Live Server**
3. اضغط بزر الفأرة الأيمن على `index.html`
4. اختر **Open with Live Server**

---

## الاستخدام

بعد تشغيل المشروع ستظهر واجهة الدردشة، ويمكنك من خلالها:

- كتابة الرسائل
- عرض الرسائل داخل نافذة المحادثة
- تعديل شكل الواجهة
- تطوير المشروع لاحقًا ليتصل بخادم أو قاعدة بيانات

---

## مثال على الملفات الأساسية

### `index.html`

```html
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>شات دردشة فورية</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="chat-container">
    <h1>شات دردشة فورية</h1>
    <div class="messages" id="messages"></div>
    <div class="input-area">
      <input type="text" id="messageInput" placeholder="اكتب رسالتك هنا..." />
      <button onclick="sendMessage()">إرسال</button>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

### `style.css`

```css
body {
  font-family: Arial, sans-serif;
  background: #f5f5f5;
  direction: rtl;
  margin: 0;
  padding: 0;
}

.chat-container {
  width: 90%;
  max-width: 600px;
  margin: 40px auto;
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.messages {
  height: 300px;
  overflow-y: auto;
  border: 1px solid #ddd;
  padding: 10px;
  margin-bottom: 15px;
  background: #fafafa;
}

.input-area {
  display: flex;
  gap: 10px;
}

input {
  flex: 1;
  padding: 10px;
  font-size: 16px;
}

button {
  padding: 10px 16px;
  cursor: pointer;
  background: #0084ff;
  color: white;
  border: none;
  border-radius: 6px;
}

button:hover {
  background: #006fd6;
}
```

### `script.js`

```javascript
function sendMessage() {
  const input = document.getElementById("messageInput");
  const messages = document.getElementById("messages");

  if (input.value.trim() !== "") {
    const msg = document.createElement("p");
    msg.textContent = input.value;
    messages.appendChild(msg);
    input.value = "";
  }
}
```

---

## التخصيص والتطوير

يمكنك تطوير المشروع مستقبلًا بإضافة:

- تسجيل الدخول وإنشاء الحسابات
- دعم الرسائل الفورية باستخدام WebSocket
- ربط بقاعدة بيانات
- إنشاء محادثات جماعية
- رفع الصور والملفات
- إضافة الإشعارات
- تحسين واجهة المستخدم

---

## المساهمة

نرحب بجميع المساهمات لتحسين المشروع.

### خطوات المساهمة

1. اعمل Fork للمشروع
2. أنشئ فرع جديد:

```bash
git checkout -b feature/new-feature
```

3. أضف التعديلات المطلوبة
4. اعمل Commit:

```bash
git commit -m "Add new feature"
```

5. ارفع التعديلات:

```bash
git push origin feature/new-feature
```

6. افتح Pull Request

---

## أفضل الممارسات

- استخدم أسماء ملفات واضحة
- حافظ على تنظيم ملفات CSS وJavaScript
- اختبر المشروع على الهاتف والكمبيوتر
- اكتب تعليقات داخل الكود عند الحاجة
- اجعل الواجهة بسيطة وسهلة للمستخدم

---

## المشاكل المعروفة

إذا واجهت أي مشكلة، يمكنك فتح **Issue** داخل المستودع مع توضيح:

- وصف المشكلة
- خطوات ظهورها
- المتصفح المستخدم
- صورة توضيحية إن أمكن

---

## خارطة الطريق

- [ ] تحسين تصميم واجهة الدردشة
- [ ] دعم الرسائل الفورية
- [ ] إضافة نظام مستخدمين
- [ ] ربط المشروع بـ Back-End
- [ ] دعم رفع الملفات والصور
- [ ] دعم الإشعارات

---

## الترخيص

هذا المشروع متاح للاستخدام والتطوير.  
يمكنك إضافة ترخيص مثل:

```text
MIT License
```

---

## المطور

تم تطوير هذا المشروع بواسطة صاحب المستودع.

- GitHub: https://github.com/alzymasd9-source

---

## ملاحظات

إذا كان المشروع يحتوي على ملفات غير منظمة أو أسماء تلقائية، فيُفضل إعادة ترتيب المشروع بالشكل التالي:

```bash
chat/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── assets/
├── images/
└── README.md
```

