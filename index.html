<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>YU.ZZZ LIST</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;700;900&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        body { font-family: 'Noto Sans TC', sans-serif; background-color: #F1F5F9; color: #334155; -webkit-tap-highlight-color: transparent; }
        .purchased-overlay { background: rgba(224, 242, 254, 0.9); backdrop-filter: blur(2px); }
        .modal-animate { animation: slideUp 0.2s ease-out; }
        @keyframes slideUp { from { transform: translateY(20px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        input { -webkit-appearance: none; border-radius: 1rem; }
        /* 防止圖片未加載時撐破佈局 */
        .img-container { min-height: 224px; display: flex; align-items: center; justify-content: center; background: #f8fafc; }
    </style>
</head>
<body class="pb-10">

    <header class="sticky top-0 z-30 bg-slate-500/95 backdrop-blur-md border-b border-white/10 shadow-sm">
        <div class="max-w-5xl mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-white font-black tracking-[0.2em] text-lg uppercase">YU.ZZZ LIST</h1>
            <div id="status" class="text-[10px] text-white/60 font-bold uppercase tracking-widest flex items-center gap-2">
                <div class="w-2.5 h-2.5 rounded-full bg-white/20 transition-all duration-500" id="statusDot"></div>
                <span id="statusText">Connecting</span>
            </div>
        </div>
    </header>

    <main class="max-w-5xl mx-auto px-6 py-8">
        <div class="flex flex-col md:flex-row gap-4 mb-10">
            <div class="relative flex-1">
                <i data-lucide="search" class="absolute left-4 top-1/2 -translate-y-1/2 text-slate-400 w-5 h-5"></i>
                <input type="text" id="searchInput" placeholder="搜尋商品或客戶..."
                    class="w-full pl-12 pr-4 py-4 rounded-2xl bg-white border-none shadow-sm focus:ring-4 focus:ring-slate-200 outline-none transition-all font-bold text-slate-600">
            </div>
            <button id="addBtn" class="px-10 py-4 bg-yellow-100 text-yellow-800 rounded-2xl font-black shadow-md border-b-4 border-yellow-200 active:scale-95 transition-all flex items-center justify-center gap-2 uppercase tracking-widest">
                <span class="text-yellow-800 text-xl font-black">+</span> ADD ITEM
            </button>
        </div>

        <div id="itemsGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
            <div class="col-span-full text-center py-20 text-slate-300 animate-pulse">
                <div class="text-4xl font-black mb-2">LOADING...</div>
                <div class="text-xs tracking-widest uppercase">正在同步雲端資料</div>
            </div>
        </div>
    </main>

    <!-- Modal -->
    <div id="modal" class="fixed inset-0 z-50 hidden flex items-center justify-center p-6">
        <div class="absolute inset-0 bg-slate-900/40 backdrop-blur-md" id="modalOverlay"></div>
        <div class="bg-white rounded-[3rem] w-full max-w-md relative z-10 overflow-hidden shadow-2xl modal-animate border border-white/50">
            <div class="p-8 text-white flex justify-between items-center bg-slate-500">
                <h2 id="modalTitle" class="text-xl font-black tracking-widest uppercase">ADD ITEM</h2>
                <button id="closeModal" class="p-2 hover:bg-white/10 rounded-full transition-all">
                    <i data-lucide="x" class="w-6 h-6"></i>
                </button>
            </div>
            
            <form id="itemForm" class="p-8 space-y-5">
                <input type="hidden" id="editId">
                <div>
                    <label class="block text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 ml-1">Name</label>
                    <input type="text" id="name" required class="w-full px-6 py-4 bg-slate-50 rounded-2xl border-none font-bold text-slate-600 focus:ring-4 focus:ring-slate-100 outline-none transition-all">
                </div>
                <div class="grid grid-cols-2 gap-4">
                    <div>
                        <label class="block text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 ml-1">Customer</label>
                        <input type="text" id="customer" class="w-full px-6 py-4 bg-slate-50 rounded-2xl border-none font-bold text-slate-600 focus:ring-4 focus:ring-slate-100 outline-none transition-all">
                    </div>
                    <div>
                        <label class="block text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 ml-1">Tags</label>
                        <input type="text" id="tags" placeholder="用逗號隔開" class="w-full px-6 py-4 bg-slate-50 rounded-2xl border-none font-bold text-slate-600 focus:ring-4 focus:ring-slate-100 outline-none transition-all">
                    </div>
                </div>
                <div>
                    <label class="block text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 ml-1">Photo</label>
                    <div class="relative border-2 border-dashed border-slate-100 rounded-3xl py-10 text-center bg-slate-50 hover:bg-slate-100 transition-all cursor-pointer group">
                        <img id="previewImg" class="hidden max-h-32 mx-auto rounded-xl shadow-lg mb-2">
                        <div id="uploadText">
                            <i data-lucide="camera" class="mx-auto w-10 h-10 text-slate-200"></i>
                            <p class="text-[10px] mt-2 font-black text-slate-300 uppercase">Upload</p>
                        </div>
                        <input type="file" id="imageInput" class="absolute inset-0 opacity-0 cursor-pointer" accept="image/*">
                    </div>
                </div>
                <button type="submit" id="saveBtn" class="w-full py-5 bg-slate-500 text-white font-black rounded-3xl shadow-lg active:scale-95 border-b-4 border-slate-600 transition-all uppercase tracking-widest flex items-center justify-center gap-2">
                    <span class="text-white text-xl font-black">+</span> SAVE
                </button>
            </form>
        </div>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getFirestore, collection, addDoc, onSnapshot, doc, deleteDoc, updateDoc, enableIndexedDbPersistence } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";
        import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";

        const firebaseConfig = JSON.parse(__firebase_config);
        const app = initializeApp(firebaseConfig);
        const db = getFirestore(app);
        const auth = getAuth(app);
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'yu-zzz-manager';

        let items = [], base64Img = null, currentUser = null;
        let unsubscribeItems = null;

        // 認證初始化
        const initAuth = async () => {
            return new Promise((resolve) => {
                const unsubscribe = onAuthStateChanged(auth, (user) => {
                    if (user) {
                        currentUser = user;
                        document.getElementById('statusText').innerText = "ONLINE";
                        document.getElementById('statusDot').className = 'w-2.5 h-2.5 rounded-full bg-emerald-400 shadow-[0_0_8px_rgba(52,211,153,0.8)]';
                        startListening();
                        resolve(user);
                        unsubscribe();
                    }
                });

                const performSignIn = async () => {
                    try {
                        if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
                            await signInWithCustomToken(auth, __initial_auth_token);
                        } else {
                            await signInAnonymously(auth);
                        }
                    } catch (err) {
                        console.error("Auth Error:", err);
                        document.getElementById('statusText').innerText = "AUTH ERROR";
                    }
                };
                performSignIn();
            });
        };

        // 監聽資料
        const startListening = () => {
            if (!currentUser) return;
            if (unsubscribeItems) unsubscribeItems();

            const colRef = collection(db, 'artifacts', appId, 'public', 'data', 'products');
            
            unsubscribeItems = onSnapshot(colRef, (s) => {
                items = s.docs.map(d => ({ id: d.id, ...d.data() }));
                items.sort((a,b) => new Date(b.updatedAt || 0) - new Date(a.updatedAt || 0));
                render();
            }, (e) => {
                console.error("Firestore Error:", e);
                document.getElementById('statusText').innerText = "SYNC ERROR";
            });
        };

        function render() {
            const grid = document.getElementById('itemsGrid');
            const q = document.getElementById('searchInput').value.toLowerCase();
            const list = items.filter(i => 
                (i.name||'').toLowerCase().includes(q) || 
                (i.customer||'').toLowerCase().includes(q) ||
                (i.tags || []).some(t => t.toLowerCase().includes(q))
            );

            if (items.length === 0) {
                grid.innerHTML = `<div class="col-span-full text-center py-20 text-slate-200 font-black text-4xl opacity-50 tracking-[0.4em] uppercase">NO ITEMS</div>`;
                return;
            }

            grid.innerHTML = list.map(i => {
                const done = i.status === '已採購';
                const tagsHtml = (i.tags || []).map(t => `<span class="bg-slate-800 text-white px-3 py-1.5 rounded-lg text-[10px] font-black uppercase tracking-wider shadow-sm">#${t}</span>`).join(' ');
                
                return `
                <div class="bg-white rounded-[2.5rem] overflow-hidden shadow-xl border border-slate-100 flex flex-col relative transition-all active:scale-[0.98]">
                    <div class="h-56 bg-slate-50 relative overflow-hidden img-container">
                        ${i.image ? `<img src="${i.image}" class="w-full h-full object-cover" loading="lazy">` : `<div class="w-full h-full flex items-center justify-center text-slate-100"><i data-lucide="image" class="w-14 h-14"></i></div>`}
                        ${done ? `
                        <div class="absolute inset-0 purchased-overlay flex items-center justify-center font-black">
                            <div class="bg-white/90 border border-sky-200 px-6 py-2 rounded-full shadow-md text-xs tracking-widest uppercase text-sky-700 font-black">DONE</div>
                        </div>` : ''}
                    </div>
                    <div class="p-8 flex-1 flex flex-col">
                        <div class="flex justify-between items-start gap-3 mb-2">
                            <div class="font-black text-slate-700 text-xl line-clamp-2 flex-1 leading-tight">${i.name}</div>
                            <div class="flex flex-wrap justify-end gap-1.5 shrink-0 pt-1">${tagsHtml}</div>
                        </div>
                        <div class="text-[11px] text-slate-400 font-black uppercase tracking-widest mb-6">${i.customer || '匿名客戶'}</div>
                        <div class="mt-auto pt-6 flex items-center justify-between gap-4 border-t border-slate-50">
                            <button onclick="window.toggle('${i.id}')" class="flex-1 py-4 rounded-2xl text-[10px] font-black tracking-widest uppercase shadow-sm transition-all ${done ? 'bg-yellow-100 text-yellow-800 border-b-2 border-yellow-200' : 'bg-slate-50 text-slate-400 border border-slate-100'}">
                                ${done ? 'REVERT' : 'MARK DONE'}
                            </button>
                            <div class="flex gap-1">
                                <button onclick="window.edit('${i.id}')" class="p-3.5 text-slate-300 active:text-slate-600 transition-colors"><i data-lucide="edit-3" class="w-5 h-5"></i></button>
                                <button onclick="window.del('${i.id}')" class="p-3.5 text-red-100 active:text-red-400 transition-colors"><i data-lucide="trash-2" class="w-5 h-5"></i></button>
                            </div>
                        </div>
                    </div>
                </div>`;
            }).join('');
            lucide.createIcons();
        }

        // Window Globals
        window.toggle = async (id) => {
            if (!currentUser) return;
            const i = items.find(x => x.id === id);
            await updateDoc(doc(db, 'artifacts', appId, 'public', 'data', 'products', id), {
                status: i.status === '已採購' ? '待購' : '已採購',
                updatedAt: new Date().toISOString()
            });
        };

        window.del = (id) => {
            if (!currentUser) return;
            if (confirm('確定刪除此商品？')) {
                deleteDoc(doc(db, 'artifacts', appId, 'public', 'data', 'products', id));
            }
        };

        window.edit = (id) => {
            const i = items.find(x => x.id === id);
            document.getElementById('editId').value = i.id;
            document.getElementById('name').value = i.name;
            document.getElementById('customer').value = i.customer || '';
            document.getElementById('tags').value = (i.tags || []).join(',');
            base64Img = i.image;
            if(base64Img) {
                document.getElementById('previewImg').src = base64Img;
                document.getElementById('previewImg').classList.remove('hidden');
                document.getElementById('uploadText').classList.add('hidden');
            }
            document.getElementById('modalTitle').innerText = 'EDIT ITEM';
            document.getElementById('saveBtn').innerHTML = '<span class="text-white text-xl font-black">+</span> UPDATE';
            document.getElementById('modal').classList.remove('hidden');
        };

        // Form Logic
        document.getElementById('itemForm').onsubmit = async (e) => {
            e.preventDefault();
            if (!currentUser) return;
            const id = document.getElementById('editId').value;
            const data = {
                name: document.getElementById('name').value,
                customer: document.getElementById('customer').value,
                tags: document.getElementById('tags').value.split(',').map(t => t.trim()).filter(t => t),
                image: base64Img,
                updatedAt: new Date().toISOString()
            };
            
            try {
                if(id) await updateDoc(doc(db, 'artifacts', appId, 'public', 'data', 'products', id), data);
                else await addDoc(collection(db, 'artifacts', appId, 'public', 'data', 'products'), {...data, status:'待購', createdAt: new Date().toISOString()});
                close();
            } catch (err) {
                console.error("Save error:", err);
            }
        };

        document.getElementById('imageInput').onchange = (e) => {
            const f = e.target.files[0];
            if (!f) return;
            const reader = new FileReader();
            reader.onload = (ev) => {
                const img = new Image();
                img.onload = () => {
                    const canvas = document.createElement('canvas');
                    const w = 400; // 壓縮圖片寬度以提升手機加載速度
                    canvas.width = w; canvas.height = img.height * (w/img.width);
                    canvas.getContext('2d').drawImage(img, 0, 0, canvas.width, canvas.height);
                    base64Img = canvas.toDataURL('image/jpeg', 0.6); // 使用 jpeg 並降低質量提升性能
                    document.getElementById('previewImg').src = base64Img;
                    document.getElementById('previewImg').classList.remove('hidden');
                    document.getElementById('uploadText').classList.add('hidden');
                };
                img.src = ev.target.result;
            };
            reader.readAsDataURL(f);
        };

        const close = () => {
            document.getElementById('modal').classList.add('hidden');
            document.getElementById('itemForm').reset();
            base64Img = null;
            document.getElementById('previewImg').classList.add('hidden');
            document.getElementById('uploadText').classList.remove('hidden');
        };

        document.getElementById('addBtn').onclick = () => { 
            document.getElementById('editId').value = ''; 
            document.getElementById('modalTitle').innerText = 'ADD ITEM'; 
            document.getElementById('saveBtn').innerHTML = '<span class="text-white text-xl font-black">+</span> SAVE';
            document.getElementById('modal').classList.remove('hidden'); 
        };
        document.getElementById('closeModal').onclick = close;
        document.getElementById('modalOverlay').onclick = close;
        document.getElementById('searchInput').oninput = render;

        // 啟動流程
        window.onload = () => {
            initAuth();
            lucide.createIcons();
        };
    </script>
</body>
</html>
