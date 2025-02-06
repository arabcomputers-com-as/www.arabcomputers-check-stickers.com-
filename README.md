
function validateForm(event) {
         event.preventDefault(); // منع إعادة تحميل الصفحة
         const allowedCodes = ["123456789012", "987654321098"]; // الأرقام المسموح بها
         const numberInput = document.getElementById("numberInput").value;

         if (allowedCodes.includes(numberInput)) {
             alert("الرقم صحيح!");
         } else {
             alert("الرقم غير صحيح!");
         }
     }
