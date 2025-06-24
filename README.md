<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>سجل العقارات مع تحكم</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f5f5f5;
      direction: rtl;
      padding: 40px;
    }
    h1, h2 {
      text-align: center;
      color: #333;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 40px;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    th, td {
      border: 1px solid #ccc;
      padding: 12px;
      text-align: center;
      vertical-align: middle;
    }
    thead {
      background-color: #007bff;
      color: white;
    }
    tbody tr:nth-child(even) {
      background-color: #f9f9f9;
    }
    img {
      max-width: 100px;
      border-radius: 8px;
    }
    .btn {
      padding: 6px 12px;
      margin: 2px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 14px;
    }
    .contact-btn { background-color: #28a745; color: white; }
    .book-btn { background-color: #17a2b8; color: white; }
    .delete-btn { background-color: #dc3545; color: white; }
    .add-btn {
      background-color: #ffc107;
      color: black;
      margin-bottom: 30px;
      display: block;
      width: 200px;
      margin: auto;
      text-align: center;
    }
  </style>
  <script>
    function deleteRow(btn) {
      var row = btn.closest("tr");
      row.remove();
    }
    function addProperty() {
      alert("نموذج إضافة عقار سيُفعّل لاحقًا.");
    }
    function contactAgent() {
      alert("تم إرسال طلب التواصل.");
    }
    function bookNow() {
      alert("تم إرسال طلب الحجز.");
    }
  </script>
</head>
<body>

  <h1>سجل العقارات حسب التصنيف</h1>
  <button class="btn add-btn" onclick="addProperty()">➕ إضافة عقار</button>

  <h2>فلل</h2>
  <table>
    <thead>
      <tr><th>صورة</th><th>الكود</th><th>الموقع</th><th>المواصفات</th><th>السعر</th><th>الحالة</th><th>خيارات</th></tr>
    </thead>
    <tbody>
      <tr>
        <td><img src="https://via.placeholder.com/100"></td>
        <td>VILLA-001</td>
        <td>الرياض - الياسمين</td>
        <td>فيلا 5 غرف - مسبح - مدخل سيارة</td>
        <td>1,900,000 ريال</td>
        <td>متاح</td>
        <td>
          <button class="btn contact-btn" onclick="contactAgent()">تواصل</button>
          <button class="btn book-btn" onclick="bookNow()">احجز</button>
          <button class="btn delete-btn" onclick="deleteRow(this)">حذف</button>
        </td>
      </tr>
    </tbody>
  </table>

</body>
</html>
