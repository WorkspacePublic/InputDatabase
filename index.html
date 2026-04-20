html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Scanner Kontak - Multi Extract</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: linear-gradient(135deg, #f6f8ff 0%, #f1f4ff 100%);
            min-height: 100vh;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.4);
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.07);
        }
        .loader {
            width: 24px;
            height: 24px;
            border: 3px solid #E2E8F0;
            border-bottom-color: #3B82F6;
            border-radius: 50%;
            display: inline-block;
            animation: rotation 1s linear infinite;
        }
        @keyframes rotation {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .gradient-text {
            background: linear-gradient(90deg, #2563eb, #7c3aed);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .contact-item {
            transition: all 0.2s ease;
            animation: fadeIn 0.4s ease-out forwards;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="p-4 md:p-8">
    <div class="max-w-4xl mx-auto">
        <!-- Header -->
        <header class="text-center mb-10">
            <h1 class="text-4xl font-extrabold mb-2 tracking-tight">
                <span class="gradient-text">Contact Scanner AI</span>
            </h1>
            <p class="text-gray-500 font-medium italic">Satu foto, banyak kontak otomatis</p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
            <!-- Left Side: Upload -->
            <div class="lg:col-span-5 space-y-6">
                <div class="glass-card rounded-3xl p-6">
                    <div id="drop-zone" class="relative group border-2 border-dashed border-blue-200 rounded-2xl p-8 text-center transition-all hover:border-blue-400 hover:bg-blue-50/50 cursor-pointer">
                        <input type="file" id="file-input" accept="image/*" class="hidden">
                        <div id="upload-ui">
                            <div class="w-16 h-16 bg-blue-100 rounded-2xl flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform">
                                <svg class="w-8 h-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
                            </div>
                            <p class="text-sm font-bold text-gray-700">Ambil/Pilih Foto</p>
                            <p class="text-xs text-gray-400 mt-1">Daftar nama akan dideteksi otomatis</p>
                        </div>
                        <img id="preview" class="hidden w-full h-auto rounded-xl shadow-md border border-white">
                    </div>

                    <button id="scan-btn" disabled class="w-full mt-6 bg-blue-600 text-white py-4 rounded-2xl font-bold shadow-lg shadow-blue-200 hover:bg-blue-700 disabled:bg-gray-200 disabled:shadow-none transition-all flex items-center justify-center gap-3">
                        <span>Mulai Scan Foto</span>
                    </button>
                </div>
            </div>

            <!-- Right Side: Results -->
            <div class="lg:col-span-7">
                <div class="glass-card rounded-3xl p-6 min-h-[400px]">
                    <div class="flex items-center justify-between mb-6">
                        <h2 class="text-xl font-bold text-gray-800">Kontak Terdeteksi</h2>
                        <span id="badge-count" class="hidden bg-blue-600 text-white text-[10px] px-2.5 py-1 rounded-full font-black">0</span>
                    </div>

                    <!-- Loading State -->
                    <div id="loading-state" class="hidden flex flex-col items-center justify-center py-20 text-center">
                        <span class="loader mb-4"></span>
                        <p class="text-gray-500 font-medium">AI sedang membaca nama-nama...</p>
                    </div>

                    <!-- Empty State -->
                    <div id="empty-state" class="flex flex-col items-center justify-center py-20 text-center text-gray-400 border-2 border-dashed border-gray-100 rounded-2xl">
                        <svg class="w-12 h-12 mb-3 opacity-20" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                        <p class="text-sm">Belum ada data. Silakan scan foto.</p>
                    </div>

                    <!-- Results List -->
                    <div id="results-list" class="space-y-3"></div>

                    <!-- Bulk Actions -->
                    <div id="bulk-actions" class="hidden mt-8 pt-6 border-t border-gray-100">
                        <button id="download-all" class="w-full bg-gray-900 text-white py-4 rounded-2xl font-bold hover:bg-black transition-all flex items-center justify-center gap-2">
                            Unduh Semua (Satu File)
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const apiKey = ""; // Disuntikkan otomatis
        const fileInput = document.getElementById('file-input');
        const dropZone = document.getElementById('drop-zone');
        const scanBtn = document.getElementById('scan-btn');
        const preview = document.getElementById('preview');
        const uploadUi = document.getElementById('upload-ui');
        const resultsList = document.getElementById('results-list');
        const loadingState = document.getElementById('loading-state');
        const emptyState = document.getElementById('empty-state');
        const badgeCount = document.getElementById('badge-count');
        const bulkActions = document.getElementById('bulk-actions');

        let detectedNames = [];

        // Interaction
        dropZone.onclick = () => fileInput.click();
        
        fileInput.onchange = (e) => {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (ev) => {
                    preview.src = ev.target.result;
                    preview.classList.remove('hidden');
                    uploadUi.classList.add('hidden');
                    scanBtn.disabled = false;
                };
                reader.readAsDataURL(file);
            }
        };

        const getFormattedDate = () => {
            const n = new Date();
            const d = String(n.getDate()).padStart(2, '0');
            const m = String(n.getMonth() + 1).padStart(2, '0');
            const y = String(n.getFullYear()).slice(-2);
            return d + m + y;
        };

        async function analyzeImage(base64) {
            const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
            
            const prompt = `Analisis gambar ini dan temukan SEMUA nama orang yang ada. Kembalikan data dalam format JSON murni: {"names": ["Nama 1", "Nama 2", ...]}. Jangan beri teks lain.`;

            const payload = {
                contents: [{
                    parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: base64 } }]
                }],
                generationConfig: { responseMimeType: "application/json" }
            };

            const response = await fetch(url, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            });

            if (!response.ok) throw new Error("AI Error");
            const data = await response.json();
            return JSON.parse(data.candidates[0].content.parts[0].text).names;
        }

        scanBtn.onclick = async () => {
            const base64 = preview.src.split(',')[1];
            
            scanBtn.disabled = true;
            loadingState.classList.remove('hidden');
            emptyState.classList.add('hidden');
            resultsList.innerHTML = '';
            bulkActions.classList.add('hidden');
            badgeCount.classList.add('hidden');

            try {
                const names = await analyzeImage(base64);
                const dateStr = getFormattedDate();
                detectedNames = names.map(n => `CN ${n} ${dateStr}`);

                loadingState.classList.add('hidden');
                
                if (detectedNames.length === 0) {
                    emptyState.classList.remove('hidden');
                } else {
                    renderNames();
                    badgeCount.innerText = detectedNames.length;
                    badgeCount.classList.remove('hidden');
                    bulkActions.classList.remove('hidden');
                }
            } catch (err) {
                alert("Gagal memproses foto. Pastikan koneksi internet aktif.");
                loadingState.classList.add('hidden');
                emptyState.classList.remove('hidden');
            } finally {
                scanBtn.disabled = false;
            }
        };

        function renderNames() {
            detectedNames.forEach((fullName, index) => {
                const item = document.createElement('div');
                item.className = "contact-item flex items-center justify-between p-4 bg-white border border-gray-100 rounded-2xl shadow-sm hover:border-blue-300 group";
                item.style.animationDelay = `${index * 0.1}s`;
                
                item.innerHTML = `
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 bg-blue-50 text-blue-600 rounded-full flex items-center justify-center font-bold text-xs">
                            ${index + 1}
                        </div>
                        <div>
                            <p class="text-sm font-bold text-gray-800">${fullName}</p>
                            <p class="text-[10px] text-gray-400 font-medium tracking-tight">READY TO EXPORT</p>
                        </div>
                    </div>
                    <button class="download-single p-2 text-blue-500 hover:bg-blue-50 rounded-xl transition-colors">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path></svg>
                    </button>
                `;

                item.querySelector('.download-single').onclick = () => downloadVCF(fullName, fullName);
                resultsList.appendChild(item);
            });
        }

        function downloadVCF(content, filename, isBulk = false) {
            let vcf = "";
            if(Array.isArray(content)) {
                content.forEach(name => {
                    vcf += `BEGIN:VCARD\nVERSION:3.0\nFN:${name}\nN:${name};;;;\nEND:VCARD\n`;
                });
            } else {
                vcf = `BEGIN:VCARD\nVERSION:3.0\nFN:${content}\nN:${content};;;;\nEND:VCARD`;
            }

            const blob = new Blob([vcf], { type: 'text/vcard' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `${filename.replace(/\s+/g, '_')}.vcf`;
            a.click();
            URL.revokeObjectURL(url);
        }

        document.getElementById('download-all').onclick = () => {
            downloadVCF(detectedNames, `Contact_Batch_${getFormattedDate()}`, true);
        };
    </script>
</body>
</html>
