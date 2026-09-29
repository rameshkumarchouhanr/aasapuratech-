# work-spot-
.github/workflows/codeql-analysis.yml<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>मेरी वेबसाइट</title>
    <style>https://aasapuratech.blg.com
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 2rem;
        }
        main {
            padding: 2rem;
        }
        footer {
            background-color: #343a40;
            color: white;
            padding: 1rem;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

    <header>
        <h1>नमस्ते, आपकी वेबसाइट में स्वागत है!</h1>
        <p>यह एक सरल और आकर्षक HTML टेम्पलेट है।</p>
    </header>

    <main>
        <h2>मुख्य सामग्री (Main Content)</h2>
        <p>आप यहाँ अपनी वेबसाइट के अनुसार जानकारी जोड़ सकते हैं।</p>
    </main>

    <footer>
        <p>&copy; 2026 सर्वाधिकार सुरक्षित।</p>
    </footer>

</body>
</html>
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>आशापुरा टेक - Aasapura Tech</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }
        header {
            background-color: #004080;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            background-color: #0066cc;
            color: white;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .container {
            display: flex;
            min-height: 400px;
            margin: 20px;
        }
        sidebar {
            width: 25%;
            background: white;
            padding: 15px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            overflow-y: max-height;
            max-height: 500px;
        }
        .content {
            width: 75%;
            background: white;
            padding: 20px;
            margin-left: 20px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
        }
        .page-link {
            display: block;
            padding: 5px 0;
            color: #0066cc;
            cursor: pointer;
            text-decoration: none;
        }
        .page-link:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <header>
        <h1>आशापुरा टेक (Aasapura Tech)</h1>
        <p>संस्थापक: रमेश कुमार चौहान | मोबाइल: 9057194614</p>
    </header>

    <nav>
        <a href="#" onclick="showHome()">होम</a>
        <a href="#" onclick="showPagesList()">सभी 100 पेजेस सूची</a>
        <a href="#" onclick="showContact()">संपर्क करें</a>
    </nav>

    <div class="container">
        <sidebar id="sidebar-menu">
            <h3>पेज सूची (1 से 100)</h3>
            <div id="links-container" style="max-height: 400px; overflow-y: scroll;">
                <!-- JavaScript द्वारा 100 लिंक्स यहाँ जनरेट होंगे -->
            </div>
        </sidebar>

        <div class="content" id="main-content">
            <h2>स्वागत है!</h2>
            <p>यह आशापुरा टेक की आधिकारिक गिटअप वेबसाइट है। बाईं ओर दी गई सूची से किसी भी पेज (1 से 100) पर क्लिक करके उसका विवरण यहाँ देख सकते हैं।</p>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 Aasapura Tech. All Rights Reserved.</p>
    </footer>

    <script>
        // 100 पेजेस का डेटा डायनेमिक रूप से तैयार करना
        const totalPages = 100;
        
        function generateSidebarLinks() {
            let container = document.getElementById('links-container');
            let htmlContent = '';
            for (let i = 1; i <= totalPages; i++) {
                htmlContent += `<a class="page-link" onclick="loadPage(${i})">पेज नंबर ${i}: विषय विवरण</a>`;
            }
            container.innerHTML = htmlContent;
        }

        function loadPage(pageNumber) {
            let contentDiv = document.getElementById('main-content');
            contentDiv.innerHTML = `
                <h2>आशापुरा टेक - पेज क्र. ${pageNumber}</h2>
                <p>यह पेज नंबर <strong>${pageNumber}</strong> का मुख्य कंटेंट है। यहाँ आप अपनी अंग्रेजी ग्रामर, शिक्षा या टेक से जुड़ी सामग्री जोड़ सकते हैं।</p>
                <p><em>यह वेबसाइट रमेश कुमार चौहान द्वारा गिटअप पर होस्ट की गई है।</em></p>
            `;
        }

        function showHome() {
            document.getElementById('main-content').innerHTML = `
                <h2>स्वागत है!</h2>
                <p>यह आशापुरा टेक की आधिकारिक गिटअप वेबसाइट है। बाईं ओर दी गई सूची से किसी भी पेज (1 से 100) पर क्लिक करें।</p>
            `;
        }

        function showContact() {
            document.getElementById('main-content').innerHTML = `
                <h2>संपर्क करें</h2>
                <p><strong>संस्थापक:</strong> रमेश कुमार चौहान</p>
                <p><strong>मोबाइल नंबर:</strong> 9057194614</p>
                <p><strong>प्लेटफॉर्म:</strong> आशापुरा टेक / गिटअप</p>
            `;
        }

        // पेज लोड होने पर लिंक्स जनरेट करें
        window.onload = function() {
            generateSidebarLinks();
        };
    </script>

</body>
</html>

<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>आशापुरा टेक - Aashapura Tech</title>
    <!-- Tailwind CSS for modern styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .smooth-scroll { scroll-behavior: smooth; }
    </style>
</head>
<body class="smooth-scroll bg-gray-50 text-gray-900 transition-colors duration-300" id="body">

    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md transition-colors duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center h-16">
            <div class="flex items-center space-x-2">
                <span class="text-2xl font-bold text-indigo-600">🚀 आशापुरा टेक</span>
            </div>
            <nav class="hidden md:flex space-x-6 font-medium">
                <a href="#home" class="hover:text-indigo-600 transition">होम</a>
                <a href="#services" class="hover:text-indigo-600 transition">सेवाएं</a>
                <a href="#about" class="hover:text-indigo-600 transition">हमारे बारे में</a>
                <a href="#contact" class="hover:text-indigo-600 transition">संपर्क करें</a>
            </nav>
            <div class="flex items-center space-x-4">
                <button onclick="toggleDarkMode()" class="p-2 rounded-full bg-gray-200 dark:bg-gray-700 text-sm font-semibold" id="theme-btn">🌙</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="py-20 bg-gradient-to-r from-indigo-600 to-blue-500 text-white text-center">
        <div class="max-w-4xl mx-auto px-4">
            <h1 class="text-4xl sm:text-6xl font-extrabold mb-6">आशापुरा टेक में आपका स्वागत है</h1>
            <p class="text-lg sm:text-xl mb-8 text-indigo-100">हम आपके बिजनेस और डिजिटल सफर को आसान बनाने के लिए बेहतरीन मोबाइल ऐप्स, सॉफ्टवेयर और डिजिटल समाधान प्रदान करते हैं।</p>
            <a href="#contact" class="bg-white text-indigo-600 font-bold px-8 py-3 rounded-full shadow-lg hover:bg-indigo-50 transition">जुड़ें हमारे साथ</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-12">
            <h2 class="text-3xl font-bold">हमारी सेवाएं (Our Services)</h2>
            <p class="text-gray-600 mt-2">हम इन क्षेत्रों में बेहतरीन तकनीकी सेवाएं देते हैं</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-white p-6 rounded-xl shadow-md border hover:shadow-xl transition">
                <div class="text-4xl mb-4">📱</div>
                <h3 class="text-xl font-semibold mb-2">मोबाइल ऐप डेवलपमेंट</h3>
                <p class="text-gray-600">एंड्रॉइड और आईओएस के लिए कस्टमाइज्ड और फास्ट मोबाइल एप्लीकेशन तैयार करना।</p>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-md border hover:shadow-xl transition">
                <div class="text-4xl mb-4">💻</div>
                <h3 class="text-xl font-semibold mb-2">वेबसाइट डिजाइनिंग</h3>
                <p class="text-gray-600">आकर्षक, रिस्पॉन्सिव और यूजर-फ्रेंडली वेबसाइट्स का निर्माण जो आपके बिजनेस को आगे बढ़ाएं।</p>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-md border hover:shadow-xl transition">
                <div class="text-4xl mb-4">📚</div>
                <h3 class="text-xl font-semibold mb-2">डिजिटल शिक्षा सामग्री</h3>
                <p class="text-gray-600">छात्रों और शिक्षकों के लिए अंग्रेजी व्याकरण और शिक्षा से जुड़ी डिजिटल सामग्री व टूल्स।</p>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="bg-gray-100 py-16 transition-colors duration-300" id="about-section">
        <div class="max-w-4xl mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-4">हमारे बारे में</h2>
            <p class="text-gray-700 leading-relaxed text-lg">
                आशापुरा टेक तकनीकी नवाचार (Innovation) और गुणवत्तापूर्ण डिजिटल सेवाओं के लिए समर्पित है। हमारा उद्देश्य आम लोगों और छोटे उद्योगों (MSME) तक आधुनिक डिजिटल तकनीक को बेहद आसान और प्रभावी तरीके से पहुंचाना है।
            </p>
        </div>
    </section>

    <!-- Contact Form Section -->
    <section id="contact" class="py-16 max-w-3xl mx-auto px-4">
        <div class="bg-white p-8 rounded-2xl shadow-lg border">
            <h2 class="text-2xl font-bold mb-6 text-center">हमसे संपर्क करें</h2>
            <form id="contactForm" onsubmit="handleFormSubmit(event)" class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-gray-700">आपका नाम</label>
                    <input type="text" id="name" required class="mt-1 block w-full px-4 py-2 border rounded-lg focus:ring-indigo-500 focus:border-indigo-500">
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">ईमेल आईडी</label>
                    <input type="email" id="email" required class="mt-1 block w-full px-4 py-2 border rounded-lg focus:ring-indigo-500 focus:border-indigo-500">
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">संदेश (Message)</label>
                    <textarea id="message" rows="4" required class="mt-1 block w-full px-4 py-2 border rounded-lg focus:ring-indigo-500 focus:border-indigo-500"></textarea>
                </div>
                <button type="submit" class="w-full bg-indigo-600 text-white font-bold py-3 rounded-lg hover:bg-indigo-700 transition">संदेश भेजें</button>
            </form>
            <p id="successMessage" class="hidden text-green-600 font-semibold text-center mt-4">धन्यवाद! आपका संदेश सफलतापूर्वक प्राप्त हो गया है।</p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-6 text-center">
        <p>&copy; 2026 आशापुरा टेक (Aashapura Tech). सर्वाधिकार सुरक्षित।</p>
    </footer>

    <!-- JavaScript Section -->
    <script>
        // Form Submission Logic
        function handleFormSubmit(event) {
            event.preventDefault(); // पेज रीफ्रेश होने से रोकता है
            
            const name = document.getElementById('name').value;
            const successMsg = document.getElementById('successMessage');
            
            // सक्सेस मैसेज दिखाना
            successMsg.textContent = `धन्यवाद ${name}! आपका संदेश हमें मिल गया है, हम जल्द ही संपर्क करेंगे।`;
            successMsg.classList.remove('hidden');
            
            // फॉर्म रीसेट करना
            document.getElementById('contactForm').reset();
            
            // 5 सेकंड बाद मैसेज छुपाना
            setTimeout(() => {
                successMsg.classList.add('hidden');
            }, 5000);
        }

        // Dark/Light Mode Toggle Logic
        function toggleDarkMode() {
            const body = document.getElementById('body');
            const navbar = document.getElementById('navbar');
            const themeBtn = document.getElementById('theme-btn');
            const aboutSec = document.getElementById('about-section');

            body.classList.toggle('bg-gray-900');
            body.classList.toggle('text-white');
            navbar.classList.toggle('bg-gray-800');
            navbar.classList.toggle('text-white');
            
            if (body.classList.contains('bg-gray-900')) {
                themeBtn.textContent = '☀️';
                aboutSec.classList.remove('bg-gray-100');
                aboutSec.classList.add('bg-gray-800');
            } else {
                themeBtn.textContent = '🌙';
                aboutSec.classList.remove('bg-gray-800');
                aboutSec.classList.add('bg-gray-100');
            }
        }
    </script>
</body>
</html>
