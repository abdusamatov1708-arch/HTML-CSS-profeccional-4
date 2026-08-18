# HTML-CSS-profeccional-4
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aloqa Formasi</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="form-container">
        <h2>Biz bilan bog'laning</h2>
        <form>
            <div class="form-group">
                <input type="text" placeholder="Ismingizni kiriting" required>
            </div>
            <div class="form-group">
                <input type="email" placeholder="Email manzilingiz" required>
            </div>
            <div class="form-group">
                <textarea placeholder="Xabaringizni yozing..." required></textarea>
            </div>
            
            <div class="checkbox-group">
                <input type="checkbox" id="terms" required>
                <label for="terms">Shartlarga roziman</label>
            </div>
            
            <button type="submit">Yuborish</button>
        </form>
    </div>

</body>
</html>

/* Umumiy sozlamalar */
body {
    font-family: 'Segoe UI', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f8fafc;
    margin: 0;
}

.form-container {
    background: white;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);
    width: 100%;
    max-width: 400px;
}

h2 { margin-bottom: 20px; color: #1e293b; }

.form-group { margin-bottom: 15px; }

input, textarea {
    width: 100%;
    padding: 12px;
    border: 2px solid #e2e8f0;
    border-radius: 8px;
    outline: none;
    transition: border-color 0.3s;
    box-sizing: border-box;
}

/* :focus effekti */
input:focus, textarea:focus {
    border-color: #4f46e5;
}

/* ::placeholder uslubi */
::placeholder { color: #94a3b8; }

/* :valid / :invalid validatsiyasi */
input:invalid:not(:placeholder-shown), 
textarea:invalid:not(:placeholder-shown) {
    border-color: #ef4444;
}

input:valid:not(:placeholder-shown), 
textarea:valid:not(:placeholder-shown) {
    border-color: #22c55e;
}

/* Custom CSS checkbox */
.checkbox-group {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 20px;
}

input[type="checkbox"] {
    appearance: none;
    width: 20px;
    height: 20px;
    border: 2px solid #cbd5e1;
    border-radius: 4px;
    cursor: pointer;
    position: relative;
}

input[type="checkbox"]:checked {
    background-color: #4f46e5;
    border-color: #4f46e5;
}

input[type="checkbox"]:checked::after {
    content: '✓';
    color: white;
    position: absolute;
    left: 4px;
    top: 0px;
    font-weight: bold;
}

button {
    width: 100%;
    padding: 12px;
    background-color: #4f46e5;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s;
}

button:hover { background-color: #4338ca; }
