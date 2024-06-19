# Передача файла на сторонний сервер

```javascript
var fileUrl = "https://example.com/path/to/file.jpeg";
var xhr = new XMLHttpRequest();
xhr.open("POST", "/upload", true);
var formData = new FormData();
formData.append("file", fileUrl);

xhr.setRequestHeader("Content-Type", "multipart/form-data");
xhr.onload = function() {
  if (xhr.status === 200) {
    console.log("Файл успешно отправлен");
  } else {
    console.log("Ошибка отправки файла");
  }
};
xhr.send(formData);
```
