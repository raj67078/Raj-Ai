# Raj-Ai
Image genetor 
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raj AI - Pro 4K Generator</title>
    <style>
        :root { --gold: #fccb00; --bg: #050505; --card: #121212; }
        body { font-family: 'Segoe UI', sans-serif; background: var(--bg); color: white; display: flex; flex-direction: column; align-items: center; padding: 20px; margin: 0; }
        
        header { text-align: center; margin: 20px 0; }
        .logo-box { font-size: 50px; filter: drop-shadow(0 0 10px var(--gold)); }
        h1 { color: var(--gold); margin: 0; font-size: 2.5rem; letter-spacing: 2px; }

        .app-card { width: 100%; max-width: 500px; background: var(--card); padding: 25px; border-radius: 25px; border: 1px solid #222; box-shadow: 0 15px 35px rgba(0,0,0,0.7); box-sizing: border-box; }
        
        .token-section { margin-bottom: 20px; }
        .token-input { width: 100%; background: #000; border: 1px solid #333; border-radius: 10px; color: var(--gold); padding: 10px; font-size: 14px; box-sizing: border-box; outline: none; }
        
        .upload-section { margin-bottom: 15px; text-align: center; }
        #imageUpload { display: none; }
        .upload-label { display: block; padding: 12px; background: #222; border: 2px dashed #444; border-radius: 12px; cursor: pointer; color: #888; }
        #previewImg { width: 100px; height: 100px; object-fit: cover; border-radius: 10px; margin-top: 10px; display: none; border: 1px solid var(--gold); }

        textarea { width: 100%; height: 100px; background: #000; border: 1px solid #333; border-radius: 15px; color: #fff; padding: 15px; font-size: 16px; box-sizing: border-box; outline: none; margin-bottom: 15px; }
        
        .gen-btn { width: 100%; background: var(--gold); color: #000; border: none; padding: 16px; border-radius: 15px; font-weight: 800; font-size: 1.1rem; cursor: pointer; }

        #result { margin-top: 30px; width: 100%; max-width: 500px; text-align: center; }
        .output-img { width: 100%; border-radius: 20px; border: 2px solid #333; }
        .dl-btn { background: #00c853; color: white; padding: 12px 25px; text-decoration: none; border-radius: 10px; display: inline-block; margin-top: 15px; font-weight: bold; }
        
        .loader { display: none; width: 45px; height: 45px; border: 5px solid #222; border-top: 5px solid var(--gold); border-radius: 50%; animation: spin 1s linear infinite; margin: 20px auto; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    </style>
</head>
<body>

    <header>
        <div class="logo-box">🍌</div>
        <h1>RAJ AI</h1>
        <p style="color: #888;">Update Token + Photo Generation</p>
    </header>

    <div class="app-card">
        <div class="token-section">
            <label style="font-size: 12px; color: #666; display: block; margin-bottom: 5px;">Hugging Face API Token:</label>
            <input type="password" id="apiToken" class="token-input" placeholder="Enter HF Token" onchange="saveToken()">
        </div>

        <div class="upload-section">
            <label for="imageUpload" class="upload-label" id="uploadLabel">📷 আপলোড ইমেজ (ঐচ্ছিক)</label>
            <input type="file" id="imageUpload" accept="image/*" onchange="previewFile()">
            <img id="previewImg" src="" alt="Preview">
        </div>

        <textarea id="promptInput" placeholder="ছবির বর্ণনা দিন..."></textarea>
        
        <button class="gen-btn" id="genBtn" onclick="generate()">GENERATE 4K IMAGE</button>
        <div class="loader" id="loader"></div>
    </div>

    <div id="result"></div>

    <script>
        const MODEL = "black-forest-labs/FLUX.1-schnell";

        // টোকেন সেভ করে রাখা
        window.onload = () => {
            const savedToken = localStorage.getItem('hf_token');
            if (savedToken) document.getElementById('apiToken').value = savedToken;
        };

        function saveToken() {
            localStorage.setItem('hf_token', document.getElementById('apiToken').value);
        }

        function previewFile() {
            const preview = document.getElementById('previewImg');
            const file = document.getElementById('imageUpload').files[0];
            const reader = new FileReader();
            reader.onloadend = () => { preview.src = reader.result; preview.style.display = "inline-block"; };
            if (file) reader.readAsDataURL(file);
        }

        async function generate() {
            const prompt = document.getElementById('promptInput').value;
            const currentToken = document.getElementById('apiToken').value.trim();
            const loader = document.getElementById('loader');
            const resultDiv = document.getElementById('result');
            const btn = document.getElementById('genBtn');

            if (!prompt || !currentToken) return alert("প্রম্পট এবং টোকেন উভয়ই প্রয়োজন!");

            loader.style.display = "block";
            btn.disabled = true;
            resultDiv.innerHTML = "";

            try {
                const response = await fetch(`https://api-inference.huggingface.co/models/${MODEL}`, {
                    headers: { "Authorization": `Bearer ${currentToken}`, "Content-Type": "application/json" },
                    method: "POST",
                    body: JSON.stringify({ inputs: prompt + ", 4k, cinematic, high detail" }),
                });

                if (response.status === 401) throw new Error("টোকেনটি ভুল! পুনরায় চেক করুন।");
                if (response.status === 429) throw new Error("লিমিট শেষ! কিছুক্ষণ পর চেষ্টা করুন।");
                if (!response.ok) throw new Error("সার্ভারে সমস্যা।");

                const blob = await response.blob();
                const url = URL.createObjectURL(blob);
                resultDiv.innerHTML = `<img src="${url}" class="output-img"><br><a href="${url}" download="RajAI.png" class="dl-btn">📥 Download 4K</a>`;
            } catch (err) {
                alert("এরর: " + err.message);
            } finally {
                loader.style.display = "none";
                btn.disabled = false;
            }
        }
    </script>
</body>
</html>
