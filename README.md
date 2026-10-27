<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دي فرصتك في الشواغر ماتضيعها</title>
    <style>
        :root {
            --primary: #1e3a8a; /* كحلي أنيق */
            --secondary: #059669; /* أخضر أمل */
            --accent: #f59e0b; /* ذهبي للتميز */
            --bg: #f8fafc;
            --card: #ffffff;
            --text: #1e293b;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg);
            color: var(--text);
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
            padding: 15px;
        }

        .app-container {
            width: 100%;
            max-width: 500px;
            background: var(--card);
            border-radius: 24px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.08);
            overflow: hidden;
            padding: 24px 20px;
            margin-top: 10px;
            border-top: 6px solid var(--secondary);
        }

        /* رأس الصفحة */
        header {
            text-align: center;
            margin-bottom: 25px;
        }

        header h1 {
            font-size: 1.8rem;
            font-weight: 900;
            color: var(--primary);
            line-height: 1.3;
            margin-bottom: 8px;
        }

        header p {
            font-size: 0.95rem;
            color: #64748b;
        }

        /* أزرار المسارات الرئيسية */
        .btn-track {
            width: 100%;
            padding: 18px;
            margin-bottom: 15px;
            border: none;
            border-radius: 16px;
            font-size: 1.25rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }

        .btn-scientific {
            background: linear-gradient(135deg, #1e3a8a, #2563eb);
            color: white;
        }

        .btn-literary {
            background: linear-gradient(135deg, #059669, #10b981);
            color: white;
        }

        .btn-track:active {
            transform: scale(0.98);
        }

        /* كروت الأقسام العلمية الثلاثة */
        .cards-grid {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-bottom: 20px;
        }

        .sub-card {
            background: #f1f5f9;
            padding: 16px;
            border-radius: 14px;
            border-right: 5px solid var(--primary);
            cursor: pointer;
            transition: 0.2s;
            font-size: 1.1rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .sub-card:hover, .sub-card.selected {
            background: #e2e8f0;
            border-right-color: var(--accent);
            transform: translateX(-4px);
        }

        /* الحقول والقوائم */
        .form-group {
            margin-top: 20px;
            background: #f8fafc;
            padding: 18px;
            border-radius: 16px;
            border: 1px solid #e2e8f0;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            font-size: 0.95rem;
            color: #334155;
        }

        select, input[type="number"] {
            width: 100%;
            padding: 14px;
            border-radius: 10px;
            border: 2px solid #cbd5e1;
            font-size: 1.05rem;
            outline: none;
            margin-bottom: 15px;
            background: white;
            transition: 0.2s;
        }

        select:focus, input[type="number"]:focus {
            border-color: var(--secondary);
        }

        .btn-submit {
            width: 100%;
            background: var(--accent);
            color: #78350f;
            border: none;
            padding: 14px;
            font-size: 1.15rem;
            font-weight: 800;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(245, 158, 11, 0.3);
        }

        /* بطاقة النتيجة */
        .result-box {
            margin-top: 20px;
            padding: 20px;
            border-radius: 16px;
            background: #ecfdf5;
            border: 2px solid #a7f3d0;
            text-align: center;
            animation: fadeIn 0.3s ease-in-out;
        }

        .result-box h3 {
            color: #065f46;
            margin-bottom: 8px;
            font-size: 1.25rem;
        }

        .result-box p {
            font-size: 1rem;
            color: #047857;
            margin-bottom: 6px;
        }

        .uni-tag {
            display: inline-block;
            background: #047857;
            color: white;
            padding: 6px 14px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 1.05rem;
            margin-top: 8px;
        }

        /* رسائل الأدبي والتنبيهات */
        .banner-hope {
            background: linear-gradient(135deg, #fef3c7, #fde68a);
            color: #92400e;
            padding: 14px;
            border-radius: 12px;
            text-align: center;
            font-weight: 800;
            font-size: 1.1rem;
            margin-bottom: 15px;
            border: 1px dashed #d97706;
        }

        .notice-box {
            background: #eff6ff;
            color: #1e40af;
            padding: 12px;
            border-radius: 10px;
            font-size: 0.88rem;
            margin-bottom: 15px;
            line-height: 1.5;
            border-right: 4px solid #3b82f6;
        }

        /* زر الرجوع */
        .btn-back {
            background: none;
            border: none;
            color: #64748b;
            font-size: 0.95rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
            margin-bottom: 15px;
            font-weight: 600;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hidden { display: none !important; }
    </style>
</head>
<body>

    <div class="app-container">
        
        <!-- رأس الموقع -->
        <header>
            <h1>دي فرصتك في الشواغر ماتضيعها 🎓</h1>
            <p>دليلك الذكي لتوقعات القبول في الجامعات السودانية الخاصة والأهلية</p>
        </header>

        <!-- الشاشة 1: الصفحة الرئيسية (اختيار المساق) -->
        <div id="homeScreen">
            <button class="btn-track btn-scientific" onclick="openScientific()">
                🔬 مساق علمي
            </button>
            <button class="btn-track btn-literary" onclick="openLiterary()">
                📚 مساق أدبي
            </button>
        </div>

        <!-- الشاشة 2: فروع المساق العلمي -->
        <div id="scientificScreen" class="hidden">
            <button class="btn-back" onclick="goHome()">➔ الرجوع للرئيسية</button>
            
            <h2 style="font-size: 1.2rem; margin-bottom: 12px; color: var(--primary);">اختر تخصصك العلمي:</h2>
            <div class="cards-grid">
                <div class="sub-card" onclick="selectSciBranch('biology')">
                    <span>🩺 علمي أحياء (المجالات الطبية)</span>
                    <span>👈</span>
                </div>
                <div class="sub-card" onclick="selectSciBranch('engineering')">
                    <span>⚙️ علمي هندسية (كليات الهندسة)</span>
                    <span>👈</span>
                </div>
                <div class="sub-card" onclick="selectSciBranch('computer')">
                    <span>💻 علمي حاسوب (التقنية والبرمجيات)</span>
                    <span>👈</span>
                </div>
            </div>

            <!-- إدخال التخصص والنسبة للعلمي -->
            <div id="sciForm" class="form-group hidden">
                <label id="sciSelectLabel" for="sciMajorSelect">اختر التخصص المطلوب:</label>
                <select id="sciMajorSelect"></select>

                <label for="sciPercentage">اكتب نسبتك المئوية (%):</label>
                <input type="number" id="sciPercentage" placeholder="مثلاً: 78" min="50" max="100">

                <button class="btn-submit" onclick="predictScientific()">توقع جامعتي الآن 🎯</button>
            </div>
        </div>

        <!-- الشاشة 3: المساق الأدبي -->
        <div id="literaryScreen" class="hidden">
            <button class="btn-back" onclick="goHome()">➔ الرجوع للرئيسية</button>

            <!-- عبارة الأمل المطلوبة -->
            <div class="banner-hope">
                ✨ أنتم المستقبل وأنتم أمل السودان ✨
            </div>

            <!-- الملاحظة المهمة المطلوبة -->
            <div class="notice-box">
                💡 <strong>ملاحظة مهمة:</strong> يُسمح لطلاب المساق الأدبي التقديم لدراسة <strong>كلية علوم الحاسوب (قسم تقانة المعلومات IT)</strong> في الجامعات الخاصة والأهلية السودانية!
            </div>

            <div class="form-group">
                <label for="litMajorSelect">اختر التخصص الأدبي المطلوب:</label>
                <select id="litMajorSelect"></select>

                <label for="litPercentage">اكتب نسبتك المئوية (%):</label>
                <input type="number" id="litPercentage" placeholder="مثلاً: 68" min="50" max="100">

                <button class="btn-submit" onclick="predictLiterary()">توقع جامعتي الآن 🎯</button>
            </div>
        </div>

        <!-- صندوق ظهور النتيجة والتوقع -->
        <div id="resultBox" class="result-box hidden">
            <h3 id="resTitle"></h3>
            <p id="resMsg"></p>
            <div id="resUni" class="uni-tag"></div>
        </div>

    </div>

    <script>
        // قواعد البيانات للجامعات والتخصصات في السودان
        const data = {
            biology: {
                majors: [
                    { name: "الطب البشري", min: 80, unis: ["جامعة العلوم الطبية والتكنولوجيا (مامون حميدة)", "جامعة ابن سينا", "جامعة الرازي", "جامعة العلوم والتقانة", "كلية النهضة", "جامعة النيل"] },
                    { name: "طب وجراحة الأسنان", min: 80, unis: ["جامعة العلوم الطبية والتكنولوجيا", "جامعة ابن سينا", "جامعة الرازي", "جامعة البيان"] },
                    { name: "الصيدلة", min: 70, unis: ["جامعة العلوم والتقانة", "جامعة المغتربين", "جامعة اليرموك", "كلية النهضة", "جامعة السودان العالمية"] },
                    { name: "المختبرات الطبية", min: 65, unis: ["جامعة ابن سينا", "جامعة الرازي", "جامعة النيل", "جامعة البيان", "جامعة المشرق"] },
                    { name: "التمريض العالي والتخدير", min: 60, unis: ["كلية النهضة", "جامعة اليرموك", "جامعة العلوم والتقانة", "جامعة الرازي"] },
                    { name: "الأشعة والتصوير الطبي", min: 60, unis: ["جامعة العلوم الطبية والتكنولوجيا", "جامعة ابن سينا", "جامعة المغتربين"] },
                    { name: "العلاج الطبيعي والتأهيل", min: 60, unis: ["جامعة ابن سينا", "جامعة الرازي", "كلية اليرموك"] }
                ]
            },
            engineering: {
                majors: [
                    { name: "هندسة العمارة والتخطيط", min: 68, unis: ["جامعة العلوم والتقانة", "جامعة المستقبل", "جامعة المغتربين"] },
                    { name: "الهندسة الطبية الحيوية", min: 65, unis: ["جامعة العلوم والتقانة", "جامعة المشرق", "جامعة السودان العالمية"] },
                    { name: "الهندسة المدنية", min: 60, unis: ["جامعة المستقبل", "جامعة النيل", "جامعة اليرموك"] },
                    { name: "الهندسة الكهربائية والإلكترونية", min: 60, unis: ["جامعة العلوم والتقانة", "جامعة المستقبل", "جامعة المشرق"] },
                    { name: "هندسة الميكاترونكس والذكاء الاصطناعي", min: 65, unis: ["جامعة المستقبل", "جامعة العلوم والتقانة"] }
                ]
            },
            computer: {
                majors: [
                    { name: "هندسة البرمجيات", min: 65, unis: ["جامعة المستقبل (كمبيوترمان سابقاً)", "جامعة العلوم والتقانة", "جامعة المشرق"] },
                    { name: "الأمن السيبراني والتحري الجنائي الرقمي", min: 65, unis: ["جامعة النيل", "جامعة المستقبل", "جامعة البيان"] },
                    { name: "علوم الحاسوب", min: 60, unis: ["جامعة العلوم والتقانة", "جامعة المستقبل", "جامعة المغتربين"] },
                    { name: "تقانة المعلومات (IT)", min: 55, unis: ["جامعة المشرق", "جامعة النيل", "جامعة السودان العالمية", "كلية النهضة"] }
                ]
            },
            literary: {
                majors: [
                    { name: "تقانة المعلومات IT (متاح للأدبي)", min: 55, unis: ["جامعة المشرق", "جامعة المستقبل", "جامعة النيل", "جامعة السودان العالمية"] },
                    { name: "إدارة الأعمال والتسويق الرقمي", min: 55, unis: ["جامعة الأحفاد للبنات", "جامعة المغتربين", "جامعة المشرق", "جامعة النيل"] },
                    { name: "المحاسبة والعلوم المالية والمصرفية", min: 55, unis: ["جامعة المستقبل", "جامعة البيان", "جامعة العلوم والتقانة"] },
                    { name: "الشريعة والقانون", min: 58, unis: ["جامعة الأحفاد", "جامعة اليرموك", "كلية النهضة", "جامعة المغتربين"] },
                    { name: "اللغة الإنجليزية والترجمة", min: 55, unis: ["جامعة الأحفاد للبنات", "جامعة النيل", "جامعة المشرق"] },
                    { name: "الإعلام والعلاقات العامة", min: 55, unis: ["جامعة البيان", "جامعة المغتربين", "جامعة اليرموك"] },
                    { name: "العلوم السياسية والدبلوماسية", min: 55, unis: ["جامعة الأحفاد للبنات", "جامعة النيل"] }
                ]
            }
        };

        let currentSciBranch = '';

        function goHome() {
            document.getElementById('homeScreen').classList.remove('hidden');
            document.getElementById('scientificScreen').classList.add('hidden');
            document.getElementById('literaryScreen').classList.add('hidden');
            document.getElementById('resultBox').classList.add('hidden');
        }

        function openScientific() {
            document.getElementById('homeScreen').classList.add('hidden');
            document.getElementById('scientificScreen').classList.remove('hidden');
            document.getElementById('sciForm').classList.add('hidden');
            document.getElementById('resultBox').classList.add('hidden');
        }

        function selectSciBranch(branchKey) {
            currentSciBranch = branchKey;
            const form = document.getElementById('sciForm');
            const select = document.getElementById('sciMajorSelect');
            select.innerHTML = '';

            data[branchKey].majors.forEach((m, idx) => {
                const opt = document.createElement('option');
                opt.value = idx;
                opt.textContent = m.name;
                select.appendChild(opt);
            });

            form.classList.remove('hidden');
            document.getElementById('resultBox').classList.add('hidden');
        }

        function openLiterary() {
            document.getElementById('homeScreen').classList.add('hidden');
            document.getElementById('literaryScreen').classList.remove('hidden');
            document.getElementById('resultBox').classList.add('hidden');

            const select = document.getElementById('litMajorSelect');
            select.innerHTML = '';
            data.literary.majors.forEach((m, idx) => {
                const opt = document.createElement('option');
                opt.value = idx;
                opt.textContent = m.name;
                select.appendChild(opt);
            });
        }

        function getRandomUni(unisList) {
            return unisList[Math.floor(Math.random() * unisList.length)];
        }

        function predictScientific() {
            const score = parseFloat(document.getElementById('sciPercentage').value);
            const majorIdx = document.getElementById('sciMajorSelect').value;
            const major = data[currentSciBranch].majors[majorIdx];
            const resultBox = document.getElementById('resultBox');

            if (!score || score < 40 || score > 100) {
                alert("الرجاء كتابة نسبة صحيحة بين 50% و 100%");
                return;
            }

            resultBox.classList.remove('hidden');

            if (score >= major.min) {
                const chosenUni = getRandomUni(major.unis);
                document.getElementById('resTitle').innerText = "🎉 دي جامعتك المتوقعة في الشواغر!";
                document.getElementById('resMsg').innerText = `نسبتك (${score}%) كافية ومنافسة جداً في تخصص (${major.name}) على النفقة الخاصة.`;
                document.getElementById('resUni').innerText = "🏛️ " + chosenUni;
            } else {
                document.getElementById('resTitle').innerText = "⚠️ فرصة بديلة في الشواغر";
                document.getElementById('resMsg').innerText = `نسبتك (${score}%) أقل من الحد الأدنى المقترح لهذا التخصص (${major.min}%)، ولكن يمكنك المنافسة في دبلومات هذا المجال أو تخصصات قريبة في:`;
                document.getElementById('resUni').innerText = "🏛️ " + getRandomUni(major.unis);
            }
        }

        function predictLiterary() {
            const score = parseFloat(document.getElementById('litPercentage').value);
            const majorIdx = document.getElementById('litMajorSelect').value;
            const major = data.literary.majors[majorIdx];
            const resultBox = document.getElementById('resultBox');

            if (!score || score < 40 || score > 100) {
                alert("الرجاء كتابة نسبة صحيحة بين 50% و 100%");
                return;
            }

            resultBox.classList.remove('hidden');
            const chosenUni = getRandomUni(major.unis);

            // الرسالة المشجعة المطلوبة للأدبي
            document.getElementById('resTitle').innerText = "مبروك سيتم قبولك في هذا المجال أكيد! 🌟";
            document.getElementById('resMsg').innerText = `بناءً على شواغر الجامعات الأهلية والخاصة ونسبتك (${score}%)، مقعدك في تخصص (${major.name}) مضمون بإذن الله في:`;
            document.getElementById('resUni').innerText = "🏛️ " + chosenUni;
        }
    </script>
</body>
</html>
