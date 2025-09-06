<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>DataGram LeadsMiner</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: {
              light: '#4f8fcc',
              DEFAULT: '#0f3f80',
              dark: '#0a2a55'
            },
            secondary: {
              light: '#5ec8f9',
              DEFAULT: '#0ea5e9',
              dark: '#0284c7'
            },
            accent: {
              light: '#7ae7a2',
              DEFAULT: '#4ade80',
              dark: '#22c55e'
            }
          }
        }
      }
    }
  </script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800&display=swap');
    
    body {
      font-family: 'Tajawal', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #4f8fcc 0%, #0f3f80 100%);
      color: white;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      scroll-behavior: smooth;
    }
    .btn-blue {
      background: #5ec8f9;
      color: white;
      transition: all 0.3s ease;
      border: 2px solid #5ec8f9;
    }
    .btn-blue:hover {
      background: #0ea5e9;
      border-color: #0ea5e9;
      transform: translateY(-2px);
      box-shadow: 0 6px 12px rgba(94, 200, 249, 0.4);
    }
    .btn-green {
      background: #7ae7a2;
      color: #064e3b;
      transition: all 0.3s ease;
      border: 2px solid #7ae7a2;
      font-weight: 600;
      box-shadow: 0 4px 8px rgba(122, 231, 162, 0.4);
    }
    .btn-green:hover {
      background: #4ade80;
      border-color: #4ade80;
      box-shadow: 0 6px 12px rgba(74, 222, 128, 0.6);
      color: #064e3b;
      transform: translateY(-2px);
    }
    .btn-white-bordered {
      background: transparent;
      border: 2px solid white;
      color: white;
      font-weight: 600;
      transition: all 0.3s ease;
    }
    .btn-white-bordered:hover {
      background: white;
      color: #0f3f80;
      transform: translateY(-2px);
    }
    /* Scrollbar for info section */
    .info-scroll {
      max-height: 260px;
      overflow-y: auto;
      scroll-behavior: smooth;
      padding-right: 1rem;
    }
    .info-scroll::-webkit-scrollbar {
      width: 6px;
    }
    .info-scroll::-webkit-scrollbar-thumb {
      background-color: #7ae7a2;
      border-radius: 10px;
    }
    /* Ribbon style for pricing */
    .ribbon {
      position: absolute;
      top: -10px;
      font-weight: 700;
      padding: 0.25rem 0.75rem;
      border-radius: 9999px;
      font-size: 0.875rem;
      white-space: nowrap;
    }
    .ribbon-blue {
      background-color: #5ec8f9;
      color: white;
      right: 0.5rem;
    }
    .ribbon-green {
      background-color: #7ae7a2;
      color: #064e3b;
      left: 0.5rem;
    }
    .ribbon-gray {
      background-color: #a0aec0;
      color: white;
      left: 0.5rem;
    }
    /* Custom checkbox icons */
    .check-icon {
      color: #7ae7a2;
      font-weight: 800;
      font-size: 1.3rem;
      margin-left: 0.5rem;
    }
    /* Logo stylization */
    .logo-letter {
      font-weight: 900;
      color: #5ec8f9;
    }
    .logo-letter.d-blue {
      color: #7ae7a2;
    }
    /* Image container styling */
    .leadminer-img {
      max-width: 180px;
      margin: 0 auto 1rem auto;
      display: block;
      border-radius: 12px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
    }
    /* Feature cards */
    .feature-card {
      background: rgba(255, 255, 255, 0.15);
      border-radius: 16px;
      padding: 1.5rem;
      transition: all 0.3s ease;
      height: 100%;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }
    .feature-card:hover {
      transform: translateY(-5px);
      background: rgba(255, 255, 255, 0.2);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
    }
    /* Hero section */
    .hero-section {
      background: url('https://images.unsplash.com/photo-1516387938699-a93567ec168e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80') no-repeat center center;
      background-size: cover;
      position: relative;
    }
    .hero-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(135deg, rgba(79, 143, 204, 0.9) 0%, rgba(10, 42, 85, 0.85) 100%);
    }
    /* Responsive adjustments */
    @media (min-width: 768px) {
      .pricing-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }
      .section-padding {
        padding-left: 4rem;
        padding-right: 4rem;
      }
      .leadminer-img {
        max-width: 220px;
      }
    }
    /* Animation */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fade-in {
      animation: fadeIn 1s ease-out forwards;
    }
    /* Stagger animation for features */
    .feature-card:nth-child(1) { animation-delay: 0.1s; }
    .feature-card:nth-child(2) { animation-delay: 0.2s; }
    .feature-card:nth-child(3) { animation-delay: 0.3s; }
    .feature-card:nth-child(4) { animation-delay: 0.4s; }
    .feature-card:nth-child(5) { animation-delay: 0.5s; }
    .feature-card:nth-child(6) { animation-delay: 0.6s; }
    
    /* Modern card styling */
    .modern-card {
      border-radius: 16px;
      overflow: hidden;
      transition: all 0.3s ease;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
    }
    .modern-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
    }
    
    /* Section headings */
    .section-heading {
      position: relative;
      padding-bottom: 1rem;
      margin-bottom: 2rem;
    }
    .section-heading::after {
      content: '';
      position: absolute;
      bottom: 0;
      right: 0;
      width: 80px;
      height: 4px;
      background: linear-gradient(to left, #5ec8f9, #7ae7a2);
      border-radius: 2px;
    }
    .section-heading.text-center::after {
      right: 50%;
      transform: translateX(50%);
    }
  </style>
</head>
<body class="overflow-x-hidden">

  <!-- Hero Section -->
  <header class="hero-section py-16 md:py-24 text-center relative">
    <div class="relative z-10 container mx-auto px-4">
      <div class="flex justify-center items-center mb-4 select-none">
      <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/DataGram-title.png" 
       alt="DataGram LeadsMiner Logo" 
       class="max-h-20 md:max-h-32 object-contain">
    </div>

      <p class="text-white text-xl md:text-2xl font-semibold max-w-3xl mx-auto leading-relaxed px-4 mb-8">
        الطريقة الأذكى لجلب عملاء مهتمين بدون تكاليف إعلانات
      </p>
      <div class="flex flex-wrap justify-center gap-4 mt-8">
        <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-green px-8 py-3 rounded-lg text-lg flex items-center">
          <i class="fas fa-download ml-2"></i> تنزيل الان
        </a>
        <a href="https://wa.me/201027930040" target="_blank" class="btn-white-bordered px-8 py-3 rounded-lg text-lg flex items-center">
          <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
        </a>
      </div>
    </div>
  </header>

  <main class="bg-gray-50 text-gray-900">
    <!-- What is LeadsMiner -->
    <section id="about" class="py-12 md:py-20 bg-white">
      <div class="max-w-6xl mx-auto px-4 md:flex md:items-center md:gap-12">
        <div class="md:w-2/5 mb-8 md:mb-0 flex justify-center">
          <img
            src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/leadsminer%20logo.png"
            alt="شعار LeadsMiner مع رمز معول تعدين يصنع ثقوب في صخر، ألوان شعار أزرق ورمادي"
            class="leadminer-img modern-card"
          />
        </div>
        <div class="md:w-3/5">
          <h2 class="text-3xl font-bold mb-6 text-primary-dark section-heading">ما هو LeadsMiner ؟</h2>
          <p class="text-lg leading-relaxed text-gray-700 mb-6">
            LeadsMiner أداة قوية على نظام الويندوز، تعمل بنفس منطق الاستهداف الموجود في مدير الإعلانات الخاص بمواقع التواصل الاجتماعي مثل (فيسبوك، انستقرام، تيك توك) وتوصلك لعملاء دقيقين ومهتمين — وكل هذا بدون ما تدفع ولا ريال على الإعلانات.
          </p>
          <div class="flex flex-wrap gap-4">
            <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-6 py-3 rounded-lg flex items-center">
              <i class="fas fa-download ml-2"></i> تنزيل الان
            </a>
            <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg flex items-center">
              <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-16 bg-gradient-to-b from-white to-gray-50">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-4 text-primary-dark section-heading text-center">ميزات LeadsMiner</h2>
        <p class="text-lg text-center text-gray-600 max-w-3xl mx-auto mb-12">اكتشف القوة الكاملة لأداة استخراج العملاء الرائدة في السوق</p>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="feature-card animate-fade-in">
            <div class="text-secondary-light text-3xl mb-4"><i class="fas fa-users"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark">عملاء غير محدودين</h3>
            <p class="text-gray-700">تقدر تستخرج عدد لا نهائي من العملاء المحتملين لعملك</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-secondary-light text-3xl mb-4"><i class="fas fa-globe"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark">استهداف عالمي</h3>
            <p class="text-gray-700">استهدف أي دولة في العالم مع دقة في التوصيل</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-secondary-light text-3xl mb-4"><i class="fas fa-bullseye"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark">استهداف ذكي</h3>
            <p class="text-gray-700">حدد اهتمامات العملاء، الفئة العمرية، النوع، وحتى مكان السكن</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-secondary-light text-3xl mb-4"><i class="fas fa-shield-alt"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark">خصوصية وأمان</h3>
            <p class="text-gray-700">بياناتك تبقى عندك وما تطلع لحد، بأعلى معايير الأمان</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-secondary-light text-3xl mb-4"><i class="fas fa-money-bill-wave"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark">توفير المال</h3>
            <p class="text-gray-700">وفر آلاف الريالات وتخلى عن الحملات الإعلانية المكلفة</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-secondary-light text-3xl mb-4"><i class="fas fa-headset"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark">دعم فني 24/7</h3>
            <p class="text-gray-700">فريق دعم فني متاح على مدار الساعة لمساعدتك</p>
          </div>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-4 mt-12">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>

    <!-- How it works -->
    <section class="py-16 bg-primary-light text-white">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 section-heading text-center">كيف يعمل LeadsMiner؟</h2>
        
        <div class="bg-primary rounded-xl p-6 md:p-8 mb-8 modern-card">
          <div class="info-scroll space-y-4 mb-8">
            <ul class="list-none text-lg">
              <li class="flex items-center gap-2 mb-4 p-3 bg-primary-dark rounded-lg"><span class="check-icon">✔</span> عملاء غير محدودة : تقدر تستخرج عدد لا نهائي من العملاء</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-primary-dark rounded-lg"><span class="check-icon">✔</span> استهداف مفتوح لكل دول العالم : تختار الدولة اللي تبغا وتوصل لها</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-primary-dark rounded-lg"><span class="check-icon">✔</span> استهداف ذكي : تحدد اهتمامات و سلوكيات العميل، الفئة العمرية، النوع، وحتى مكان السكن</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-primary-dark rounded-lg"><span class="check-icon">✔</span> استهداف دقيق - زي نظام إعلانات فيسبوك و انستجرام يوصل لك جمهورك المثالي</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-primary-dark rounded-lg"><span class="check-icon">✔</span> بدون إعلانات - ووفر آلاف الريالات وتخلى عن الحملات المدفوعة</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-primary-dark rounded-lg"><span class="check-icon">✔</span> خصوصية وأمان - بياناتك تبقى عندك وما تطلع لحد</li>
            </ul>
          </div>

          <div class="text-center mt-10">
            <h3 class="text-2xl font-extrabold mb-6">جاهز تشترك ؟</h3>
            <div class="flex flex-wrap justify-center gap-4">
              <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-8 py-3 rounded-lg text-lg flex items-center">
                <i class="fas fa-download ml-2"></i> تنزيل الان
              </a>
              <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-8 py-3 rounded-lg text-lg flex items-center">
                <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="py-16 bg-gray-50">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-4 text-primary-dark section-heading text-center">باقات LeadsMiner</h2>
        <p class="text-lg text-center text-gray-600 max-w-3xl mx-auto mb-12">اختر الباقة المناسبة لاحتياجاتك وابدأ في زيادة مبيعاتك اليوم</p>

        <div class="pricing-grid grid grid-cols-1 gap-8 md:grid-cols-3">
          <!-- Beginner -->
          <div class="relative bg-white rounded-xl shadow-lg p-6 text-center text-gray-800 transform hover:scale-105 transition-transform duration-300 modern-card">
            <div class="ribbon ribbon-blue">مبتدئ</div>
            <div class="my-6">
              <div class="text-4xl font-bold text-primary-dark">370$</div>
              <div class="text-gray-500 mt-2">شهرياً</div>
            </div>
            <ul class="text-right space-y-3 my-6">
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> اشتراك لمدة شهر واحد</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> عدد غير محدود من العملاء</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
            </ul>
            <a href="https://wa.me/201027930040" class="btn-blue w-full py-3 rounded-lg mt-6 flex items-center justify-center">
              <i class="fas fa-shopping-cart ml-2"></i> اشترك الآن
            </a>
          </div>

          <!-- Pro -->
          <div class="relative bg-white rounded-xl shadow-xl p-8 text-center text-gray-900 transform scale-105 border-4 border-accent-light z-10 modern-card">
            <div class="ribbon ribbon-green">الأكثر شهرة</div>
            <div class="my-6">
              <div class="text-4xl font-bold text-primary-dark">2999$</div>
              <div class="text-gray-500 mt-2">سنوياً <span class="text-green-600">(وفر 20%)</span></div>
            </div>
            <ul class="text-right space-y-3 my-6">
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> اشتراك لمدة عام كامل</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> عدد غير محدود من العملاء</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> تحديثات مجانية</li>
            </ul>
            <a href="https://wa.me/201027930040" class="btn-green w-full py-3 rounded-lg mt-6 flex items-center justify-center">
              <i class="fas fa-crown ml-2"></i> اشترك الآن
            </a>
          </div>

          <!-- Expert -->
          <div class="relative bg-white rounded-xl shadow-lg p-6 text-center text-gray-800 transform hover:scale-105 transition-transform duration-300 modern-card">
            <div class="ribbon ribbon-gray">خبير</div>
            <div class="my-6">
              <div class="text-4xl font-bold text-primary-dark">3700$</div>
              <div class="text-gray-500 mt-2">دفعة واحدة</div>
            </div>
            <ul class="text-right space-y-3 my-6">
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> اشتراك مدى الحياة</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> عدد لا نهائي من العملاء</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> تحديثات مجانية دائمة</li>
            </ul>
            <a href="https://wa.me/201027930040" class="btn-blue w-full py-3 rounded-lg mt-6 flex items-center justify-center">
              <i class="fas fa-gem ml-2"></i> اشترك الآن
            </a>
          </div>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-4 mt-12">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-white">
      <div class="max-w-4xl mx-auto px-4 text-center">
        <h2 class="text-3xl font-bold mb-4 text-primary-dark section-heading text-center">تواصل معنا</h2>
        <p class="text-lg text-gray-600 mb-8">هل لديك استفسار أو تحتاج إلى مساعدة؟ فريقنا متاح لخدمتك</p>
        
        <div class="bg-blue-50 rounded-xl p-8 modern-card">
          <div class="flex flex-col md:flex-row justify-center items-center gap-6 mb-8">
            <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg flex items-center">
              <i class="fab fa-whatsapp text-2xl ml-2"></i> واتساب
            </a>
            <a href="mailto:info@datagram.site" class="btn-blue px-6 py-3 rounded-lg flex items-center">
              <i class="fas fa-envelope text-2xl ml-2"></i> البريد الإلكتروني
            </a>
          </div>
          
          <p class="text-primary-dark font-semibold">
            <i class="fas fa-phone-alt ml-2"></i> +201027930040
          </p>
  
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-4 mt-12">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-16 bg-gray-50">
      <div class="max-w-4xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-4 text-primary-dark section-heading text-center">الأسئلة الشائعة</h2>
        
        <div class="space-y-4 mt-8">
          <div class="bg-white rounded-xl p-6 shadow modern-card">
            <h3 class="text-xl font-bold text-primary-dark mb-2">هل أحتاج إلى خبرة تقنية لاستخدام LeadsMiner؟</h3>
            <p class="text-gray-700">لا، LeadsMiner صمم ليكون سهل الاستخدام حتى لأولئك الذين ليست لديهم خلفية تقنية. واجهة المستخدم بسيطة وبديهية.</p>
          </div>
          
          <div class="bg-white rounded-xl p-6 shadow modern-card">
            <h3 class="text-xl font-bold text-primary-dark mb-2">كم من الوقت يستغرق لبدء رؤية النتائج؟</h3>
            <p class="text-gray-700">معظم العملاء يبدأون في رؤية النتائج من الساعات الاولي، حيث يمكنك استخراج أول قائمة عملاء محتملين خلال اقل من ساعة واحدة من التثبيت.</p>
          </div>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-4 mt-12">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-8 py-3 rounded-lg text-lg flex items-center">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>
  </main>

  <footer class="bg-primary-dark py-8 text-white">
    <div class="max-w-6xl mx-auto px-4 flex flex-col md:flex-row justify-between items-center">
      <div class="mb-6 md:mb-0">
        <div class="flex justify-center items-center mb-4 select-none">
        <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/DataGram-title.png" 
         alt="DataGram LeadsMiner Logo" 
         class="max-h-20 md:max-h-32 object-contain">
</div>

        <p class="text-blue-200 mt-2">© 2025 جميع الحقوق محفوظة</p>
      </div>
      
      <div class="flex flex-col items-center md:items-end">
        <a href="https://wa.me/201027930040" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 text-accent-light font-semibold hover:text-accent-dark transition-colors mb-2">
          <i class="fab fa-whatsapp text-xl"></i>
          <span>+201027930040</span>
        </a>
        <div class="flex gap-4 mt-4">
          <a href="#" class="text-blue-200 hover:text-white transition-colors"><i class="fab fa-facebook-f text-xl"></i></a>
          <a href="#" class="text-blue-200 hover:text-white transition-colors"><i class="fab fa-twitter text-xl"></i></a>
          <a href="#" class="text-blue-200 hover:text-white transition-colors"><i class="fab fa-instagram text-xl"></i></a>
        </div>
      </div>
    </div>
  </footer>

  <script>
    function scrollToSection(id) {
      const section = document.getElementById(id);
      if (section) {
        section.scrollIntoView({ behavior: "smooth" });
      }
    }
    
    // Add animation on scroll
    document.addEventListener('DOMContentLoaded', function() {
      const animatedElements = document.querySelectorAll('.animate-fade-in');
      
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.visibility = 'visible';
            entry.target.classList.add('animate-fade-in');
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.1 });
      
      animatedElements.forEach(el => {
        el.style.visibility = 'hidden';
        observer.observe(el);
      });
    });
  </script>
</body>
</html>
