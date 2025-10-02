[index.html](https://github.com/user-attachments/files/22663440/index.html)

<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> </title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&family=Inter:wght@300;400;500;600&display=swap');
        
        :root {
            --primary: #1a365d;
            --secondary: #d69e2e;
            --accent: #2d3748;
            --light: #f7fafc;
            --dark: #2d3748;
        }
        
        body {
            font-family: 'Cairo', sans-serif;
            transition: all 0.3s ease;
        }
        
        .lang-en, .lang-fr, .lang-ff {
            font-family: 'Inter', sans-serif;
        }
        
        .hero-pattern {
            background: linear-gradient(rgba(26, 54, 93, 0.8), rgba(26, 54, 93, 0.9)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%231a365d"/><path d="M0 0L100 100M100 0L0 100" stroke="%23d69e2e" stroke-width="1"/></svg>');
        }
        
        .rtl {
            direction: rtl;
        }
        
        .ltr {
            direction: ltr;
        }
        
        /* إخفاء المحتوى أثناء تحميل اللغة */
        .translatable {
            opacity: 1;
            transition: opacity 0.3s ease;
        }
        
        .translating {
            opacity: 0.5;
        }
        
        /* تأثيرات للزر النشط */
        .lang-btn.active {
            background-color: #d69e2e !important;
            color: white !important;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800"> <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <!-- شريط التنقل -->
    <nav class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center py-4">
                <!-- الشعار -->
                <div class="flex items-center space-x-2 rtl:space-x-reverse">
                    <div class="w-10 h-10 bg-amber-500 rounded-full flex items-center justify-center">
                        <i class="fas fa-book text-white text-lg"></i>
                    </div>
                    <span class="text-xl font-bold text-blue-900" data-i18n="journal_title">المجلة الفولانية</span> <meta name="description" content="مجلة التاريخ والثقافة الفولانية - منصة متعددة اللغات للتراث الفولاني">
                </div>

                <!-- روابط التنقل -->
                <div class="hidden md:flex space-x-8 rtl:space-x-reverse">
                    <a href="#home" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_home">الرئيسية</a>
                    <a href="#issues" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_issues">الأعداد</a>
                    <a href="#articles" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_articles">المقالات</a>
                    <a href="#research" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_research">الأبحاث</a>
                    <a href="#oral-histories" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_oral_histories">قصص شفهية</a>
                    <a href="#glossary" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_glossary">المعجم</a>
                </div>

                <!-- زر القائمة المختصرة للأجهزة الصغيرة -->
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-blue-900 focus:outline-none">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>

                <!-- اختيار اللغة -->
                <div class="flex items-center space-x-2 rtl:space-x-reverse">
                    <button class="lang-btn px-2 py-1 text-sm bg-amber-500 text-white rounded active" data-lang="ar">عربي</button>
                    <button class="lang-btn px-2 py-1 text-sm bg-gray-100 text-gray-600 rounded lang-en" data-lang="en">EN</button>
                    <button class="lang-btn px-2 py-1 text-sm bg-gray-100 text-gray-600 rounded lang-fr" data-lang="fr">FR</button>
                    <button class="lang-btn px-2 py-1 text-sm bg-gray-100 text-gray-600 rounded lang-ff" data-lang="ff">FF</button>
                </div>
            </div>

            <!-- القائمة المختصرة -->
            <div id="mobile-menu" class="hidden md:hidden py-4 border-t">
                <div class="flex flex-col space-y-4">
                    <a href="#home" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_home">الرئيسية</a>
                    <a href="#issues" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_issues">الأعداد</a>
                    <a href="#articles" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_articles">المقالات</a>
                    <a href="#research" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_research">الأبحاث</a>
                    <a href="#oral-histories" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_oral_histories">قصص شفهية</a>
                    <a href="#glossary" class="text-blue-900 hover:text-amber-500 font-medium" data-i18n="nav_glossary">المعجم</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- قسم البطل (Hero) -->
    <section id="home" class="hero-pattern text-white py-20">
        <div class="container mx-auto px-4 text-center">
            <h1 class="text-4xl md:text-5xl font-bold mb-4" data-i18n="hero_title">مجلة التاريخ والثقافة الفولانية</h1>
            <p class="text-xl mb-8 max-w-3xl mx-auto" data-i18n="hero_description">منصة متعددة اللغات تهدف للحفاظ على التراث الفولاني ونشره من خلال الأبحاث الأكاديمية، القصص الشفهية، والمواد الثقافية.</p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#issues" class="bg-amber-500 hover:bg-amber-600 text-white font-bold py-3 px-6 rounded-lg transition duration-300" data-i18n="hero_button1">
                    استكشف الأعداد الأخيرة
                </a>
                <a href="#submit" class="bg-transparent hover:bg-blue-800 border-2 border-white text-white font-bold py-3 px-6 rounded-lg transition duration-300" data-i18n="hero_button2">
                    أرسل مقالك
                </a>
            </div>
        </div>
    </section>

    <!-- الأقسام الرئيسية -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-blue-900 mb-12" data-i18n="sections_title">أقسام المجلة</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- قسم الأعداد -->
                <div class="bg-blue-50 rounded-lg p-6 shadow-md hover:shadow-lg transition duration-300">
                    <div class="w-14 h-14 bg-blue-900 rounded-full flex items-center justify-center mb-4">
                        <i class="fas fa-book-open text-white text-xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-blue-900 mb-2" data-i18n="section_issues_title">الأعداد</h3>
                    <p class="text-gray-700 mb-4" data-i18n="section_issues_desc">استكشف أعداد المجلة الدورية التي تضم أحدث الأبحاث والمقالات حول الثقافة الفولانية.</p>
                    <a href="#issues" class="text-amber-600 font-medium hover:text-amber-700" data-i18n="section_explore">استكشف الأعداد →</a>
                </div>
                
                <!-- قسم المقالات -->
                <div class="bg-blue-50 rounded-lg p-6 shadow-md hover:shadow-lg transition duration-300">
                    <div class="w-14 h-14 bg-blue-900 rounded-full flex items-center justify-center mb-4">
                        <i class="fas fa-newspaper text-white text-xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-blue-900 mb-2" data-i18n="section_articles_title">المقالات</h3>
                    <p class="text-gray-700 mb-4" data-i18n="section_articles_desc">مقالات متنوعة تغطي جوانب مختلفة من التاريخ الفولاني، الثقافة، اللغة، والفنون.</p>
                    <a href="#articles" class="text-amber-600 font-medium hover:text-amber-700" data-i18n="section_read">اقرأ المقالات →</a>
                </div>
                
                <!-- قسم الأبحاث -->
                <div class="bg-blue-50 rounded-lg p-6 shadow-md hover:shadow-lg transition duration-300">
                    <div class="w-14 h-14 bg-blue-900 rounded-full flex items-center justify-center mb-4">
                        <i class="fas fa-search text-white text-xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-blue-900 mb-2" data-i18n="section_research_title">الأبحاث</h3>
                    <p class="text-gray-700 mb-4" data-i18n="section_research_desc">أبحاث أكاديمية معمقة حول التاريخ الفولاني، علم الإنسان، اللغويات، والمزيد.</p>
                    <a href="#research" class="text-amber-600 font-medium hover:text-amber-700" data-i18n="section_browse">استعرض الأبحاث →</a>
                </div>
                
                <!-- قسم القصص الشفهية -->
                <div class="bg-blue-50 rounded-lg p-6 shadow-md hover:shadow-lg transition duration-300">
                    <div class="w-14 h-14 bg-blue-900 rounded-full flex items-center justify-center mb-4">
                        <i class="fas fa-microphone text-white text-xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-blue-900 mb-2" data-i18n="section_oral_title">قصص شفهية</h3>
                    <p class="text-gray-700 mb-4" data-i18n="section_oral_desc">مجموعة من التسجيلات الصوتية والمرئية للقصص والتقاليد الشفهية الفولانية.</p>
                    <a href="#oral-histories" class="text-amber-600 font-medium hover:text-amber-700" data-i18n="section_listen">استمع إلى القصص →</a>
                </div>
                
                <!-- قسم المعجم -->
                <div class="bg-blue-50 rounded-lg p-6 shadow-md hover:shadow-lg transition duration-300">
                    <div class="w-14 h-14 bg-blue-900 rounded-full flex items-center justify-center mb-4">
                        <i class="fas fa-book text-white text-xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-blue-900 mb-2" data-i18n="section_glossary_title">المعجم</h3>
                    <p class="text-gray-700 mb-4" data-i18n="section_glossary_desc">قاموس متعدد اللغات للمصطلحات الفولانية مع تفسيراتها وأمثلة على استخدامها.</p>
                    <a href="#glossary" class="text-amber-600 font-medium hover:text-amber-700" data-i18n="section_explore_glossary">استكشف المعجم →</a>
                </div>
                
                <!-- قسم الوسائط -->
                <div class="bg-blue-50 rounded-lg p-6 shadow-md hover:shadow-lg transition duration-300">
                    <div class="w-14 h-14 bg-blue-900 rounded-full flex items-center justify-center mb-4">
                        <i class="fas fa-photo-video text-white text-xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-blue-900 mb-2" data-i18n="section_media_title">الوسائط المتعددة</h3>
                    <p class="text-gray-700 mb-4" data-i18n="section_media_desc">معرض للصور، مقاطع الفيديو، والتسجيلات الصوتية التي توثق الثقافة الفولانية.</p>
                    <a href="#media" class="text-amber-600 font-medium hover:text-amber-700" data-i18n="section_browse_media">استعرض الوسائط →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- أحدث المحتويات -->
    <section class="py-16 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-blue-900 mb-12" data-i18n="latest_content">أحدث المحتويات</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- مقال حديث -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition duration-300">
                    <div class="h-48 bg-blue-900 flex items-center justify-center">
                        <i class="fas fa-newspaper text-white text-5xl"></i>
                    </div>
                    <div class="p-6">
                        <span class="text-sm text-amber-600 font-medium" data-i18n="content_article">مقال</span>
                        <h3 class="text-xl font-bold text-blue-900 my-2" data-i18n="content_article_title">الهجرة الفولانية عبر العصور</h3>
                        <p class="text-gray-700 mb-4" data-i18n="content_article_desc">تتبع مسارات هجرة المجتمعات الفولانية عبر غرب أفريقيا وأثرها على التنوع الثقافي.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-sm text-gray-500" data-i18n="content_days_ago">2 يوم مضت</span>
                            <a href="#" class="text-blue-900 hover:text-amber-600 font-medium" data-i18n="content_read_more">اقرأ المزيد →</a>
                        </div>
                    </div>
                </div>
                
                <!-- بحث حديث -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition duration-300">
                    <div class="h-48 bg-blue-800 flex items-center justify-center">
                        <i class="fas fa-search text-white text-5xl"></i>
                    </div>
                    <div class="p-6">
                        <span class="text-sm text-amber-600 font-medium" data-i18n="content_research">بحث</span>
                        <h3 class="text-xl font-bold text-blue-900 my-2" data-i18n="content_research_title">الأنماط الموسيقية في الثقافة الفولانية</h3>
                        <p class="text-gray-700 mb-4" data-i18n="content_research_desc">دراسة تحليلية للأنماط الموسيقية التقليدية وتطورها في المجتمعات الفولانية.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-sm text-gray-500" data-i18n="content_days_ago2">5 يوم مضت</span>
                            <a href="#" class="text-blue-900 hover:text-amber-600 font-medium" data-i18n="content_read_more">اقرأ المزيد →</a>
                        </div>
                    </div>
                </div>
                
                <!-- قصة شفهية حديثة -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition duration-300">
                    <div class="h-48 bg-blue-700 flex items-center justify-center">
                        <i class="fas fa-microphone text-white text-5xl"></i>
                    </div>
                    <div class="p-6">
                        <span class="text-sm text-amber-600 font-medium" data-i18n="content_oral">قصة شفهية</span>
                        <h3 class="text-xl font-bold text-blue-900 my-2" data-i18n="content_oral_title">حكايات الجدّة أمونة</h3>
                        <p class="text-gray-700 mb-4" data-i18n="content_oral_desc">مجموعة من الحكايات التقليدية التي ترويها الجدّة أمونة من منطقة فوتا جالون.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-sm text-gray-500" data-i18n="content_week_ago">أسبوع مضى</span>
                            <a href="#" class="text-blue-900 hover:text-amber-600 font-medium" data-i18n="content_listen">استمع →</a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#articles" class="bg-blue-900 hover:bg-blue-800 text-white font-bold py-3 px-6 rounded-lg transition duration-300" data-i18n="view_all_content">
                    عرض جميع المحتويات
                </a>
            </div>
        </div>
    </section>

    <!-- قسم الاشتراك -->
    <section class="py-16 bg-blue-900 text-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-4" data-i18n="subscribe_title">اشترك في النشرة البريدية</h2>
            <p class="text-xl mb-8 max-w-3xl mx-auto" data-i18n="subscribe_desc">ابق على اطلاع بأحدث الأبحاث، المقالات، والفعاليات المتعلقة بالثقافة الفولانية.</p>
            
            <form class="max-w-xl mx-auto flex flex-col md:flex-row gap-4">
                <input type="email" placeholder="بريدك الإلكتروني" class="flex-grow px-4 py-3 rounded-lg text-gray-800 focus:outline-none focus:ring-2 focus:ring-amber-500" data-i18n-placeholder="email_placeholder">
                <button type="submit" class="bg-amber-500 hover:bg-amber-600 text-white font-bold py-3 px-6 rounded-lg transition duration-300" data-i18n="subscribe_button">
                    اشترك الآن
                </button>
            </form>
            
            <p class="text-sm mt-4 text-blue-200" data-i18n="privacy_notice">نحن نحترم خصوصيتك ولن نشارك بريدك مع أي طرف ثالث.</p>
        </div>
    </section>

    <!-- التذييل -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- معلومات المجلة -->
                <div>
                    <h3 class="text-xl font-bold mb-4" data-i18n="footer_journal_title">المجلة الفولانية</h3>
                    <p class="text-gray-300 mb-4" data-i18n="footer_journal_desc">منصة أكاديمية وثقافية تهدف للحفاظ على التراث الفولاني ونشره.</p>
                    <div class="flex space-x-4 rtl:space-x-reverse">
                        <a href="#" class="text-gray-300 hover:text-amber-500"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-300 hover:text-amber-500"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-300 hover:text-amber-500"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-300 hover:text-amber-500"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <!-- روابط سريعة -->
                <div>
                    <h3 class="text-xl font-bold mb-4" data-i18n="footer_quick_links">روابط سريعة</h3>
                    <ul class="space-y-2">
                        <li><a href="#about" class="text-gray-300 hover:text-amber-500" data-i18n="footer_about">عن المجلة</a></li>
                        <li><a href="#submit" class="text-gray-300 hover:text-amber-500" data-i18n="footer_submit">إرسال مقال</a></li>
                        <li><a href="#events" class="text-gray-300 hover:text-amber-500" data-i18n="footer_events">الفعاليات</a></li>
                        <li><a href="#contact" class="text-gray-300 hover:text-amber-500" data-i18n="footer_contact">اتصل بنا</a></li>
                        <li><a href="#donate" class="text-gray-300 hover:text-amber-500" data-i18n="footer_donate">ادعمنا</a></li>
                    </ul>
                </div>
                
                <!-- الأقسام -->
                <div>
                    <h3 class="text-xl font-bold mb-4" data-i18n="footer_sections">الأقسام</h3>
                    <ul class="space-y-2">
                        <li><a href="#issues" class="text-gray-300 hover:text-amber-500" data-i18n="nav_issues">الأعداد</a></li>
                        <li><a href="#articles" class="text-gray-300 hover:text-amber-500" data-i18n="nav_articles">المقالات</a></li>
                        <li><a href="#research" class="text-gray-300 hover:text-amber-500" data-i18n="nav_research">الأبحاث</a></li>
                        <li><a href="#oral-histories" class="text-gray-300 hover:text-amber-500" data-i18n="nav_oral_histories">قصص شفهية</a></li>
                        <li><a href="#glossary" class="text-gray-300 hover:text-amber-500" data-i18n="nav_glossary">المعجم</a></li>
                    </ul>
                </div>
                
                <!-- معلومات الاتصال -->
                <div>
                    <h3 class="text-xl font-bold mb-4" data-i18n="footer_contact_us">اتصل بنا</h3>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-envelope mt-1 mr-2 text-amber-500 rtl:ml-2 rtl:mr-0"></i>
                            <span class="text-gray-300">info@fulanijournal.org</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-phone mt-1 mr-2 text-amber-500 rtl:ml-2 rtl:mr-0"></i>
                            <span class="text-gray-300">+123 456 7890</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-2 text-amber-500 rtl:ml-2 rtl:mr-0"></i>
                            <span class="text-gray-300" data-i18n="footer_address">الخرطوم، السودان</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p data-i18n="footer_copyright">جميع الحقوق محفوظة © 2023 المجلة الفولانية. المحتوى مرخص تحت رخصة المشاع الإبداعي CC BY-SA.</p>
            </div>
        </div>
    </footer>

    <script>
        // نظام الترجمة متعدد اللغات
        const translations = {
            ar: {
                // التنقل
                "journal_title": "المجلة الفولانية",
                "nav_home": "الرئيسية",
                "nav_issues": "الأعداد",
                "nav_articles": "المقالات",
                "nav_research": "الأبحاث",
                "nav_oral_histories": "قصص شفهية",
                "nav_glossary": "المعجم",
                
                // البطل (Hero)
                "hero_title": "مجلة التاريخ والثقافة الفولانية",
                "hero_description": "منصة متعددة اللغات تهدف للحفاظ على التراث الفولاني ونشره من خلال الأبحاث الأكاديمية، القصص الشفهية، والمواد الثقافية.",
                "hero_button1": "استكشف الأعداد الأخيرة",
                "hero_button2": "أرسل مقالك",
                
                // الأقسام
                "sections_title": "أقسام المجلة",
                "section_issues_title": "الأعداد",
                "section_issues_desc": "استكشف أعداد المجلة الدورية التي تضم أحدث الأبحاث والمقالات حول الثقافة الفولانية.",
                "section_articles_title": "المقالات",
                "section_articles_desc": "مقالات متنوعة تغطي جوانب مختلفة من التاريخ الفولاني، الثقافة، اللغة، والفنون.",
                "section_research_title": "الأبحاث",
                "section_research_desc": "أبحاث أكاديمية معمقة حول التاريخ الفولاني، علم الإنسان، اللغويات، والمزيد.",
                "section_oral_title": "قصص شفهية",
                "section_oral_desc": "مجموعة من التسجيلات الصوتية والمرئية للقصص والتقاليد الشفهية الفولانية.",
                "section_glossary_title": "المعجم",
                "section_glossary_desc": "قاموس متعدد اللغات للمصطلحات الفولانية مع تفسيراتها وأمثلة على استخدامها.",
                "section_media_title": "الوسائط المتعددة",
                "section_media_desc": "معرض للصور، مقاطع الفيديو، والتسجيلات الصوتية التي توثق الثقافة الفولانية.",
                
                "section_explore": "استكشف الأعداد →",
                "section_read": "اقرأ المقالات →",
                "section_browse": "استعرض الأبحاث →",
                "section_listen": "استمع إلى القصص →",
                "section_explore_glossary": "استكشف المعجم →",
                "section_browse_media": "استعرض الوسائط →",
                
                // المحتوى
                "latest_content": "أحدث المحتويات",
                "content_article": "مقال",
                "content_article_title": "الهجرة الفولانية عبر العصور",
                "content_article_desc": "تتبع مسارات هجرة المجتمعات الفولانية عبر غرب أفريقيا وأثرها على التنوع الثقافي.",
                "content_research": "بحث",
                "content_research_title": "الأنماط الموسيقية في الثقافة الفولانية",
                "content_research_desc": "دراسة تحليلية للأنماط الموسيقية التقليدية وتطورها في المجتمعات الفولانية.",
                "content_oral": "قصة شفهية",
                "content_oral_title": "حكايات الجدّة أمونة",
                "content_oral_desc": "مجموعة من الحكايات التقليدية التي ترويها الجدّة أمونة من منطقة فوتا جالون.",
                
                "content_days_ago": "2 يوم مضت",
                "content_days_ago2": "5 يوم مضت",
                "content_week_ago": "أسبوع مضى",
                "content_read_more": "اقرأ المزيد →",
                "content_listen": "استمع →",
                
                "view_all_content": "عرض جميع المحتويات",
                
                // الاشتراك
                "subscribe_title": "اشترك في النشرة البريدية",
                "subscribe_desc": "ابق على اطلاع بأحدث الأبحاث، المقالات، والفعاليات المتعلقة بالثقافة الفولانية.",
                "email_placeholder": "بريدك الإلكتروني",
                "subscribe_button": "اشترك الآن",
                "privacy_notice": "نحن نحترم خصوصيتك ولن نشارك بريدك مع أي طرف ثالث.",
                
                // التذييل
                "footer_journal_title": "المجلة الفولانية",
                "footer_journal_desc": "منصة أكاديمية وثقافية تهدف للحفاظ على التراث الفولاني ونشره.",
                "footer_quick_links": "روابط سريعة",
                "footer_about": "عن المجلة",
                "footer_submit": "إرسال مقال",
                "footer_events": "الفعاليات",
                "footer_contact": "اتصل بنا",
                "footer_donate": "ادعمنا",
                "footer_sections": "الأقسام",
                "footer_contact_us": "اتصل بنا",
                "footer_address": "الخرطوم، السودان",
                "footer_copyright": "جميع الحقوق محفوظة © 2023 المجلة الفولانية. المحتوى مرخص تحت رخصة المشاع الإبداعي CC BY-SA."
            },
            en: {
                // Navigation
                "journal_title": "Fulani Journal",
                "nav_home": "Home",
                "nav_issues": "Issues",
                "nav_articles": "Articles",
                "nav_research": "Research",
                "nav_oral_histories": "Oral Histories",
                "nav_glossary": "Glossary",
                
                // Hero
                "hero_title": "Journal of Fulani History and Culture",
                "hero_description": "A multilingual platform dedicated to preserving and disseminating Fulani heritage through academic research, oral histories, and cultural materials.",
                "hero_button1": "Explore Latest Issues",
                "hero_button2": "Submit Article",
                
                // Sections
                "sections_title": "Journal Sections",
                "section_issues_title": "Issues",
                "section_issues_desc": "Explore our periodic journal issues featuring the latest research and articles on Fulani culture.",
                "section_articles_title": "Articles",
                "section_articles_desc": "Diverse articles covering various aspects of Fulani history, culture, language, and arts.",
                "section_research_title": "Research",
                "section_research_desc": "In-depth academic research on Fulani history, anthropology, linguistics, and more.",
                "section_oral_title": "Oral Histories",
                "section_oral_desc": "A collection of audio and visual recordings of Fulani oral stories and traditions.",
                "section_glossary_title": "Glossary",
                "section_glossary_desc": "A multilingual dictionary of Fulani terms with explanations and usage examples.",
                "section_media_title": "Multimedia",
                "section_media_desc": "Gallery of images, videos, and audio recordings documenting Fulani culture.",
                
                "section_explore": "Explore Issues →",
                "section_read": "Read Articles →",
                "section_browse": "Browse Research →",
                "section_listen": "Listen to Stories →",
                "section_explore_glossary": "Explore Glossary →",
                "section_browse_media": "Browse Media →",
                
                // Content
                "latest_content": "Latest Content",
                "content_article": "Article",
                "content_article_title": "Fulani Migration Through the Ages",
                "content_article_desc": "Tracing the migration paths of Fulani communities across West Africa and their impact on cultural diversity.",
                "content_research": "Research",
                "content_research_title": "Musical Patterns in Fulani Culture",
                "content_research_desc": "An analytical study of traditional musical patterns and their evolution in Fulani societies.",
                "content_oral": "Oral History",
                "content_oral_title": "Grandma Amuna's Tales",
                "content_oral_desc": "A collection of traditional stories narrated by Grandma Amuna from the Fouta Djallon region.",
                
                "content_days_ago": "2 days ago",
                "content_days_ago2": "5 days ago",
                "content_week_ago": "1 week ago",
                "content_read_more": "Read More →",
                "content_listen": "Listen →",
                
                "view_all_content": "View All Content",
                
                // Subscription
                "subscribe_title": "Subscribe to Our Newsletter",
                "subscribe_desc": "Stay updated with the latest research, articles, and events related to Fulani culture.",
                "email_placeholder": "Your Email",
                "subscribe_button": "Subscribe Now",
                "privacy_notice": "We respect your privacy and will not share your email with any third party.",
                
                // Footer
                "footer_journal_title": "Fulani Journal",
                "footer_journal_desc": "An academic and cultural platform dedicated to preserving and promoting Fulani heritage.",
                "footer_quick_links": "Quick Links",
                "footer_about": "About",
                "footer_submit": "Submit",
                "footer_events": "Events",
                "footer_contact": "Contact",
                "footer_donate": "Donate",
                "footer_sections": "Sections",
                "footer_contact_us": "Contact Us",
                "footer_address": "Khartoum, Sudan",
                "footer_copyright": "All rights reserved © 2023 Fulani Journal. Content licensed under CC BY-SA."
            },
            fr: {
                // Navigation
                "journal_title": "Revue Foulani",
                "nav_home": "Accueil",
                "nav_issues": "Numéros",
                "nav_articles": "Articles",
                "nav_research": "Recherches",
                "nav_oral_histories": "Histoires Orales",
                "nav_glossary": "Glossaire",
                
                // Hero
                "hero_title": "Revue d'Histoire et de Culture Foulani",
                "hero_description": "Une plateforme multilingue dédiée à la préservation et à la diffusion du patrimoine foulani à travers la recherche académique, les histoires orales et les documents culturels.",
                "hero_button1": "Explorer les Derniers Numéros",
                "hero_button2": "Soumettre un Article",
                
                // Sections
                "sections_title": "Sections de la Revue",
                "section_issues_title": "Numéros",
                "section_issues_desc": "Explorez nos numéros périodiques présentant les dernières recherches et articles sur la culture foulani.",
                "section_articles_title": "Articles",
                "section_articles_desc": "Articles divers couvrant divers aspects de l'histoire, de la culture, de la langue et des arts foulani.",
                "section_research_title": "Recherches",
                "section_research_desc": "Recherches académiques approfondies sur l'histoire foulani, l'anthropologie, la linguistique et plus encore.",
                "section_oral_title": "Histoires Orales",
                "section_oral_desc": "Une collection d'enregistrements audio et visuels d'histoires et traditions orales foulani.",
                "section_glossary_title": "Glossaire",
                "section_glossary_desc": "Un dictionnaire multilingue des termes foulani avec explications et exemples d'utilisation.",
                "section_media_title": "Multimédia",
                "section_media_desc": "Galerie d'images, vidéos et enregistrements audio documentant la culture foulani.",
                
                "section_explore": "Explorer les Numéros →",
                "section_read": "Lire les Articles →",
                "section_browse": "Parcourir les Recherches →",
                "section_listen": "Écouter les Histoires →",
                "section_explore_glossary": "Explorer le Glossaire →",
                "section_browse_media": "Parcourir les Médias →",
                
                // Content
                "latest_content": "Contenu Récent",
                "content_article": "Article",
                "content_article_title": "La Migration Foulani à Travers les Âges",
                "content_article_desc": "Retracer les chemins de migration des communautés foulani à travers l'Afrique de l'Ouest et leur impact sur la diversité culturelle.",
                "content_research": "Recherche",
                "content_research_title": "Modèles Musicaux dans la Culture Foulani",
                "content_research_desc": "Une étude analytique des modèles musicaux traditionnels et leur évolution dans les sociétés foulani.",
                "content_oral": "Histoire Orale",
                "content_oral_title": "Les Contes de Grand-mère Amuna",
                "content_oral_desc": "Une collection d'histoires traditionnelles racontées par Grand-mère Amuna de la région du Fouta Djallon.",
                
                "content_days_ago": "Il y a 2 jours",
                "content_days_ago2": "Il y a 5 jours",
                "content_week_ago": "Il y a 1 semaine",
                "content_read_more": "Lire la Suite →",
                "content_listen": "Écouter →",
                
                "view_all_content": "Voir Tout le Contenu",
                
                // Subscription
                "subscribe_title": "Abonnez-vous à Notre Newsletter",
                "subscribe_desc": "Restez informé des dernières recherches, articles et événements liés à la culture foulani.",
                "email_placeholder": "Votre Email",
                "subscribe_button": "S'abonner Maintenant",
                "privacy_notice": "Nous respectons votre vie privée et ne partagerons pas votre email avec des tiers.",
                
                // Footer
                "footer_journal_title": "Revue Foulani",
                "footer_journal_desc": "Une plateforme académique et culturelle dédiée à la préservation et à la promotion du patrimoine foulani.",
                "footer_quick_links": "Liens Rapides",
                "footer_about": "À Propos",
                "footer_submit": "Soumettre",
                "footer_events": "Événements",
                "footer_contact": "Contact",
                "footer_donate": "Soutenir",
                "footer_sections": "Sections",
                "footer_contact_us": "Contactez-nous",
                "footer_address": "Khartoum, Soudan",
                "footer_copyright": "Tous droits réservés © 2023 Revue Foulani. Contenu sous licence CC BY-SA."
            },
            ff: {
                // Navigation
                "journal_title": "Jaŋde Fulfulde",
                "nav_home": "Jaɓɓorgo",
                "nav_issues": "Taƴƴe",
                "nav_articles": "Binndi",
                "nav_research": "Ƴeewtere",
                "nav_oral_histories": "Taali Tati",
                "nav_glossary": "Saggitorde",
                
                // Hero
                "hero_title": "Jaŋde Taariika e Adaaji Fulɓe",
                "hero_description": "Nokkuure ɗemɗe ɗuuɗɗe woodi njiylaw Adunaaji Fulɓe e njahrugol taariikaaji, taali tati, e ko adii ɓesngu.",
                "hero_button1": "Ƴeew Taƴƴe Kesɗe",
                "hero_button2": "Nawna Binndi",
                
                // Sections
                "sections_title": "Fedde Jaŋde",
                "section_issues_title": "Taƴƴe",
                "section_issues_desc": "Ƴeew taƴƴe jaŋde amen ɗi njahri ɓesngu e binndi kesɗi e Adunaaji Fulɓe.",
                "section_articles_title": "Binndi",
                "section_articles_desc": "Binndi ceeri ceeri ɗi hawta ko heewi e taariika Fulɓe, adunaaji, ɗemngal, e laabi.",
                "section_research_title": "Ƴeewtere",
                "section_research_desc": "Ƴeewtere anndal mawnungal e taariika Fulɓe, anndal nedɗo, ɗemngal, e ɓeydaagu.",
                "section_oral_title": "Taali Tati",
                "section_oral_desc": "Fedde mawnungal taali tati e aadaaji Fulɓe ɗi ndaaran ko heewi e ndiyam e njiylaw.",
                "section_glossary_title": "Saggitorde",
                "section_glossary_desc": "Saggitorde ɗemɗe ɗuuɗɗe woodi kala kelme Fulfulde e firooji maɓɓe e misaalaaji.",
                "section_media_title": "Ko Adii Njiylaw",
                "section_media_desc": "Nokkuure njiylaw fijirde, wideooji, e ndiyam ɗi njahri Adunaaji Fulɓe.",
                
                "section_explore": "Ƴeew Taƴƴe →",
                "section_read": "Janng Binndi →",
                "section_browse": "Ƴeew Ƴeewtere →",
                "section_listen": "Haŋkito Taali →",
                "section_explore_glossary": "Ƴeew Saggitorde →",
                "section_browse_media": "Ƴeew Njiylaw →",
                
                // Content
                "latest_content": "Ko Kesɗi",
                "content_article": "Binndi",
                "content_article_title": "Jahrugol Fulɓe Laawol Ngoni",
                "content_article_desc": "Dootagol laawol jahrugol renndooji Fulɓe haa worgo Afrik e ko waɗi e ceerol adunaaji.",
                "content_research": "Ƴeewtere",
                "content_research_title": "Fannu Wamɓe e Adunaaji Fulɓe",
                "content_research_desc": "Ƴeewtere firoowo fannu wamɓe aadaaji e ɓeydaagu maɓɓe e renndooji Fulɓe.",
                "content_oral": "Taali Tati",
                "content_oral_title": "Taali Maama Amuna",
                "content_oral_desc": "Fedde taali aadaaji ɗi Maama Amuna wiɗi yimre Fouta Djallon.",
                
                "content_days_ago": "Ñalɗi 2 ɓaawo",
                "content_days_ago2": "Ñalɗi 5 ɓaawo",
                "content_week_ago": "Yontere 1 ɓaawo",
                "content_read_more": "Janng Ɓeydaagu →",
                "content_listen": "Haŋkito →",
                
                "view_all_content": "Yiy Ko Fof",
                
                // Subscription
                "subscribe_title": "Winndito e Jaɓɓorgel Amen",
                "subscribe_desc": "Hokkito ko kesɗi e ɓesngu, binndi, e ko waɗi e Adunaaji Fulɓe.",
                "email_placeholder": "Email Maɓɓa",
                "subscribe_button": "Winndito Jooni",
                "privacy_notice": "Min ndewata suturo maɓɓa, min mbaawata njalbi email maɓɓa wonande goɗɗo.",
                
                // Footer
                "footer_journal_title": "Jaŋde Fulfulde",
                "footer_journal_desc": "Nokkuure anndal e adunaaji woodi njiylaw Adunaaji Fulɓe e njahrugol.",
                "footer_quick_links": "Jokkol Cewɗol",
                "footer_about": "Baɗte",
                "footer_submit": "Nawna",
                "footer_events": "Ko Waɗi",
                "footer_contact": "Jokkol",
                "footer_donate": "Wallu",
                "footer_sections": "Fedde",
                "footer_contact_us": "Jokkol Min",
                "footer_address": "Khartoum, Sudan",
                "footer_copyright": "Haɓɓe fof heɓii © 2023 Jaŋde Fulfulde. Ko adii ina woodi lesdi CC BY-SA."
            }
        };

        // دالة لتحميل اللغة
        function loadLanguage(lang) {
            // تغيير سمة اللغة في عنصر HTML
            document.documentElement.lang = lang;
            
            // تغيير اتجاه النص بناءً على اللغة
            if (lang === 'ar') {
                document.documentElement.dir = 'rtl';
                document.body.classList.add('rtl');
                document.body.classList.remove('ltr');
            } else {
                document.documentElement.dir = 'ltr';
                document.body.classList.add('ltr');
                document.body.classList.remove('rtl');
            }
            
            // إضافة تأثير الترجمة
            document.querySelectorAll('.translatable').forEach(el => {
                el.classList.add('translating');
            });
            
            // ترجمة النصوص
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if (translations[lang] && translations[lang][key]) {
                    el.textContent = translations[lang][key];
                }
            });
            
            // ترجمة النصوص في عناصر الإدخال
            document.querySelectorAll('[data-i18n-placeholder]').forEach(el => {
                const key = el.getAttribute('data-i18n-placeholder');
                if (translations[lang] && translations[lang][key]) {
                    el.placeholder = translations[lang][key];
                }
            });
            
            // إزالة تأثير الترجمة بعد انتهاء الترجمة
            setTimeout(() => {
                document.querySelectorAll('.translatable').forEach(el => {
                    el.classList.remove('translating');
                });
            }, 300);
            
            // تحديث أزرار اللغة النشطة
            document.querySelectorAll('.lang-btn').forEach(btn => {
                if (btn.getAttribute('data-lang') === lang) {
                    btn.classList.add('active');
                    btn.classList.remove('bg-gray-100', 'text-gray-600');
                    btn.classList.add('bg-amber-500', 'text-white');
                } else {
                    btn.classList.remove('active');
                    btn.classList.add('bg-gray-100', 'text-gray-600');
                    btn.classList.remove('bg-amber-500', 'text-white');
                }
            });
            
            // حفظ اللغة المفضلة
            localStorage.setItem('preferred-language', lang);
        }

        // تهيئة اللغة عند تحميل الصفحة
        document.addEventListener('DOMContentLoaded', function() {
            // إضافة صنف translatable لجميع العناصر التي يمكن ترجمتها
            document.querySelectorAll('[data-i18n], [data-i18n-placeholder]').forEach(el => {
                el.classList.add('translatable');
            });
            
            // تحديد اللغة المفضلة من localStorage أو استخدام اللغة الافتراضية
            const preferredLang = localStorage.getItem('preferred-language') || 'ar';
            loadLanguage(preferredLang);
            
            // إضافة مستمعي الأحداث لأزرار تغيير اللغة
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const lang = this.getAttribute('data-lang');
                    loadLanguage(lang);
                });
            });
            
            // تفعيل القائمة المختصرة للأجهزة الصغيرة
            document.getElementById('menu-toggle').addEventListener('click', function() {
                const menu = document.getElementById('mobile-menu');
                menu.classList.toggle('hidden');
            });
        });
    </script>
</body>
</html>
