<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pencarian NISN Siswa Kelas IX - 2026</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #1e3a8a;
            --primary-light: #3b82f6;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --background: #f8fafc;
            --text-main: #1e293b;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', sans-serif;
        }

        body {
            background-color: var(--background);
            color: var(--text-main);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .app-container {
            width: 100%;
            max-width: 500px;
            background: #ffffff;
            border-radius: 24px;
            box-shadow: 0 10px 25px rgba(30, 58, 138, 0.08);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            min-height: 550px;
        }

        /* Header Aplikasi */
        .app-header {
            background: linear-gradient(135deg, var(--primary), #0f172a);
            color: #ffffff;
            padding: 24px;
            text-align: center;
        }
        .app-header h1 {
            font-size: 1.1rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            line-height: 1.4;
        }
        .app-header p {
            font-size: 0.8rem;
            opacity: 0.8;
            margin-top: 4px;
        }

        /* Konten Utama */
        .app-content {
            flex: 1;
            padding: 24px;
            position: relative;
        }

        /* Glassmorphism Box */
        .m3-glass {
            background: #f1f5f9;
            border-radius: 16px;
            padding: 20px;
            border: 1px solid #e2e8f0;
        }

        .search-title {
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 12px;
            color: var(--primary);
        }

        /* Input Wrapper */
        .input-wrapper {
            position: relative;
            display: flex;
            align-items: center;
            background: #ffffff;
            border: 2px solid #cbd5e1;
            border-radius: 12px;
            padding: 0 14px;
            transition: all 0.3s ease;
        }
        .input-wrapper:focus-within {
            border-color: var(--primary-light);
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.15);
        }
        .input-wrapper i {
            color: #94a3b8;
            margin-right: 10px;
            font-size: 1.1rem;
        }
        .input-name {
            width: 100%;
            border: none;
            outline: none;
            padding: 14px 0;
            font-size: 1rem;
            font-weight: 500;
            color: var(--text-main);
        }

        /* Tombol Utama */
        .btn-search {
            width: 100%;
            background: var(--primary-light);
            color: #ffffff;
            border: none;
            border-radius: 12px;
            padding: 14px;
            font-size: 0.95rem;
            font-weight: 600;
            margin-top: 14px;
            cursor: pointer;
            transition: background 0.2s ease;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
        }
        .btn-search:hover {
            background: #2563eb;
        }

        /* Error Message */
        .error-message {
            display: none;
            background: #fef2f2;
            border: 1px solid #fca5a5;
            color: var(--danger);
            border-radius: 12px;
            padding: 12px;
            margin-top: 16px;
            font-size: 0.85rem;
            font-weight: 500;
            gap: 8px;
            align-items: center;
        }

        /* Loading Spinner */
        .loading-container {
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 30px 0;
            gap: 12px;
        }
        .spinner {
            width: 36px;
            height: 36px;
            border: 4px solid #e2e8f0;
            border-top-color: var(--primary-light);
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }
        .pulse-text {
            font-size: 0.85rem;
            color: #64748b;
            font-weight: 500;
        }

        /* Kartu Hasil Hasil Akhir */
        .result-envelope {
            display: none;
            margin-top: 20px;
            animation: slideUp 0.4s ease-out;
        }
        .student-card {
            background: #ffffff;
            border: 2px solid #e2e8f0;
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.02);
        }
        .student-name {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--primary);
            text-transform: uppercase;
            margin-bottom: 4px;
        }
        .student-meta {
            font-size: 0.8rem;
            color: #64748b;
            margin-bottom: 16px;
            border-bottom: 1px dashed #e2e8f0;
            padding-bottom: 12px;
        }
        .info-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
            background: #f8fafc;
            padding: 12px 14px;
            border-radius: 8px;
        }
        .info-label {
            font-size: 0.9rem;
            font-weight: 500;
            color: #64748b;
        }
        .info-value {
            font-size: 1.05rem;
            font-weight: 700;
            color: var(--primary);
            letter-spacing: 0.5px;
        }

        /* Animations */
        @keyframes spin { to { transform: rotate(360deg); } }
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="app-container">
    
    <div class="app-header">
        <h1>SMP NEGERI 1 LINGGA</h1>
        <p>Layanan Mandiri Pencarian NISN Siswa 2026</p>
    </div>

    <div class="app-content">

        <div class="m3-glass search-box">
            <div class="search-title">Cari NISN Berdasarkan Nama</div>
            
            <div class="input-wrapper">
                <i class="fa-solid fa-user"></i>
                <input type="text" id="input-search-name" class="input-name" placeholder="Ketik nama lengkap siswa...">
            </div>

            <button class="btn-search" onclick="prosesCariNisn()">
                <i class="fa-solid fa-magnifying-glass"></i> Cari NISN
            </button>
        </div>

        <div id="search-error" class="error-message"></div>

        <div id="search-loading" class="loading-container">
            <div class="spinner"></div>
            <div class="pulse-text">Mencari data di database sekolah...</div>
        </div>

        <div id="result-target" class="result-envelope"></div>

    </div>
</div>

<script>
// DATABASE SISWA KELAS IX 2026 (Diambil dari Berkas PDF Sekolah)
const STUDENT_DATABASE = [
    { name: "adelia dwi nurmansyah", nisn: "0115557747" },
    { name: "Ananda Ibnu Fahrezi", nisn: "0101111863" },
    { name: "Dafitra Ariansyah", nisn: "0112631039" },
    { name: "Delvry Anggara Panjaitan", nisn: "0097680988" },
    { name: "Dyra Altha Funisya", nisn: "0117042213" },
    { name: "Faqiha Tazkiatun Nufus", nisn: "0111647237" },
    { name: "Ghastan Gautama Ginarda", nisn: "0109121124" },
    { name: "JEANTRIKA SAPUTERA", nisn: "0112426972" },
    { name: "Liyana Zahira", nisn: "0114122561" },
    { name: "M.BAYU RIZKITULLAH", nisn: "0128826786" },
    { name: "MARWA DWI RAMADANI", nisn: "0118177962" },
    { name: "MECA ADELYA CAHYANI", nisn: "0113559822" },
    { name: "megawati", nisn: "0118701232" },
    { name: "Meisya Awalun Nurhasanah", nisn: "0115247372" },
    { name: "Muhammad Erwan Zarka", nisn: "0114962861" },
    { name: "Muhammad Fadhil Ardiansyah", nisn: "0118552573" },
    { name: "Muhammad Gibran Assyafari", nisn: "0102053051" },
    { name: "Mulhuda", nisn: "0118730407" },
    { name: "NUR RAFNI YASMADI", nisn: "0113332240" },
    { name: "QIAN FERDINAND", nisn: "0117775355" },
    { name: "RAFADIL ANΑΝΤΑ", nisn: "0114103715" },
    { name: "RAJA FATHUR ABDILLAH", nisn: "0118789434" },
    { name: "RINA RIYANTI", nisn: "0112333526" },
    { name: "RISKA SARI", nisn: "0113067688" },
    { name: "RISKY ARDIAN MISKA SACHPUTRA", nisn: "0114699199" },
    { name: "RISNA ULKA ARYANI", nisn: "0113962310" },
    { name: "RIZKA ALFIA AZ ZAHRA", nisn: "0115867734" },
    { name: "sapinah", nisn: "0117587242" },
    { name: "Sheril Gianda Utami", nisn: "0114766625" },
    { name: "SILA ADELIA", nisn: "0112026378" },
    { name: "SUKMASARI", nisn: "0116317492" },
    { name: "SYARIFAH IZZATI AQILA", nisn: "0111751808" },
    { name: "SYARIFAH NAFIA SAFIZ", nisn: "0113394958" },
    { name: "SYARIFAH NAJWA SAFIZ", nisn: "0116942061" },
    { name: "Syarifah Zilfa Natasya", nisn: "0116938426" },
    { name: "ZALFA MUFIDAH INAYAH", nisn: "0112757766" },
    { name: "Zatia Maysya", nisn: "0115755742" },
    { name: "ZIFARA OKTIA GISKA", nisn: "0105395625" }
];

// FUNGSI EKSEKUSI PENCARIAN (Check & Submit)
function prosesCariNisn() {
    const inputField = document.getElementById('input-search-name');
    const resultTarget = document.getElementById('result-target');
    const errorBox = document.getElementById('search-error');
    const loadingBox = document.getElementById('search-loading');

    // Reset Tampilan Awal
    resultTarget.style.display = 'none';
    errorBox.style.display = 'none';
    errorBox.innerHTML = '';

    // Ambil nilai teks input, hilangkan spasi berlebih, jadikan huruf kecil semua agar fleksibel
    const queryName = inputField.value.trim().toLowerCase();

    // 1. Validasi: Input Kosong
    if (queryName === "") {
        errorBox.style.display = 'flex';
        errorBox.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i> Silakan masukkan nama lengkap siswa terlebih dahulu.';
        return;
    }

    // 2. Validasi Jarak Teks: Menghindari pengguna hanya mengetik 1-2 huruf
    if (queryName.length < 3) {
        errorBox.style.display = 'flex';
        errorBox.innerHTML = '<i class="fa-solid fa-circle-info"></i> Masukkan nama lebih spesifik/lengkap untuk alasan keamanan data.';
        return;
    }

    // 3. Pencocokan Ketat (Mencari kecocokan nama yang sama persis dalam database)
    const resultMatch = STUDENT_DATABASE.filter(student => student.name.toLowerCase() === queryName);

    // 4. Validasi: Jika Data Tidak Ditemukan
    if (resultMatch.length === 0) {
        errorBox.style.display = 'flex';
        errorBox.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i> Maaf, nama siswa tidak ditemukan. Pastikan ejaan dan nama lengkap sudah benar.';
        return;
    }

    // 5. Lolos Validasi: Tampilkan Animasi Loading
    loadingBox.style.display = 'flex';

    setTimeout(() => {
        loadingBox.style.display = 'none';
        
        const student = resultMatch[0];
        
        // Buat komponen kartu hasil
        resultTarget.innerHTML = `
            <div class="student-card">
                <div class="student-name">${student.name}</div>
                <div class="student-meta">Status Verifikasi: Terdaftar Aktif</div>
                
                <div class="info-row">
                    <span class="info-label">Nomor NISN</span>
                    <span class="info-value">${student.nisn}</span>
                </div>
            </div>
        `;
        
        // Tampilkan hasil secara eksklusif ke layar
        resultTarget.style.display = 'block';
    }, 1000);
}
</script>

</body>
</html>
