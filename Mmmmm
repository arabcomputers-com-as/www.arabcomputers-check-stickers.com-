<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>التحقق من الباركود</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        #result {
            margin-top: 20px;
            font-size: 20px;
        }
    </style>
</head>
<body>
    <h1>التحقق من الباركود</h1>
    <p>أدخل الرقم للتحقق:</p>
    <form onsubmit="validateForm(event)">
        <input type="text" id="numberInput" placeholder="أدخل الرقم هنا">
        <button type="submit">تحقق</button>
    </form>
    <p id="result"></p>

    <script>
        function validateForm(event) {
            event.preventDefault(); // منع إعادة تحميل الصفحة
            const allowedCodes = ["123456789012", "112233", "123456", "987654321098"]; // الأرقام المسموح بها
            const numberInput = document.getElementById("numberInput").value;

            console.log("الرقم المدخل:", numberInput); // مراقبة الرقم المدخل

            // استرجاع الأرقام التي تم استخدامها مسبقًا من التخزين المحلي
            const usedCodes = JSON.parse(localStorage.getItem("usedCodes")) || [];
            console.log("الأرقام المستخدمة:", usedCodes); // مراقبة الأرقام المستخدمة

            if (usedCodes.includes(numberInput)) {
                alert("هذا الرقم تم استخدامه مسبقًا!"); // رسالة إذا كان الرقم مستخدمًا
                return; // إيقاف الدالة إذا كان الرقم مستخدمًا
            }

            if (allowedCodes.includes(numberInput)) {
                // إضافة الرقم إلى قائمة الأرقام المستخدمة
                usedCodes.push(numberInput);
                localStorage.setItem("usedCodes", JSON.stringify(usedCodes));
                console.log("تم إضافة الرقم إلى الأرقام المستخدمة:", usedCodes); // مراقبة الأرقام المستخدمة بعد الإضافة

                // توجيه المستخدم إلى موقعك إذا كان الرقم صحيحًا
                window.location.href = "https://arabcomputrs.wordpress.com/";
            } else {
                alert("الرقم غير صحيح!"); // رسالة إذا كان الرقم غير صحيح
            }
        }
    </script>
</body>
</html>
