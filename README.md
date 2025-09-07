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

    /* Mobile-specific improvements */
    @media (max-width: 767px) {
      /* Improved mobile typography */
      .hero-section h1 {
        font-size: 1.8rem;
        line-height: 2.2rem;
      }
      .hero-section p {
        font-size: 1rem;
        line-height: 1.6rem;
        padding: 0 0.5rem;
      }
      
      /* Better button sizing for touch */
      .btn-mobile {
        padding: 0.8rem 1.2rem;
        font-size: 1rem;
        min-height: 48px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
      
      /* Improved spacing for mobile */
      .mobile-section-padding {
        padding-top: 2.5rem;
        padding-bottom: 2.5rem;
      }
      
      /* Better card layout for mobile */
      .mobile-card {
        margin-bottom: 1.5rem;
        padding: 1.2rem;
      }
      
      /* Improved grid for mobile features */
      .mobile-feature-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
      }
      
      /* Better pricing card layout */
      .pricing-card-mobile {
        margin-bottom: 2rem;
        transform: scale(0.95);
      }
      .pricing-card-mobile:last-child {
        margin-bottom: 0;
      }
      
      /* Center align text on mobile */
      .mobile-text-center {
        text-align: center;
      }
      
      /* Adjust video size for mobile */
      .mobile-video {
        width: 100%;
        height: auto;
        max-height: 240px;
      }
      
      /* Footer adjustments */
      .mobile-footer {
        flex-direction: column;
        text-align: center;
        padding: 1.5rem 1rem;
      }
      
      /* Reduce icon sizes on mobile */
      .mobile-icon {
        font-size: 1.8rem;
      }
      
      /* Better form elements for mobile */
      input, select, textarea {
        font-size: 16px !important; /* Prevents zoom on iOS */
      }
      
      /* Prevent horizontal scrolling */
      body, html {
        overflow-x: hidden;
        width: 100%;
      }
      
      /* Touch-friendly links */
      a, button {
        min-height: 44px;
        min-width: 44px;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      /* Features section improvements */
      .mobile-feature-section {
        padding: 2rem 1rem;
      }
      
      .mobile-feature-card {
        padding: 1.2rem;
        margin-bottom: 0.5rem;
        height: auto;
        display: flex;
        flex-direction: column;
      }
      
      .mobile-feature-icon {
        font-size: 1.8rem;
        margin-bottom: 0.8rem;
      }
      
      .mobile-feature-title {
        font-size: 1.1rem;
        margin-bottom: 0.5rem;
        line-height: 1.4;
      }
      
      .mobile-feature-desc {
        font-size: 0.95rem;
        line-height: 1.5;
      }
      
      /* Pricing section improvements */
      .mobile-pricing-section {
        padding: 2rem 1rem;
      }
      
      .mobile-pricing-grid {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
        margin-top: 1.5rem;
      }
      
      .mobile-pricing-card {
        padding: 1.5rem;
        margin-bottom: 0;
        transform: scale(1);
        width: 100%;
      }
      
      .mobile-pricing-card.featured {
        transform: scale(1);
        order: -1; /* Move featured card to top on mobile */
        margin: 0.5rem 0 1.5rem 0;
      }
      
      .mobile-price {
        font-size: 2rem;
        margin: 0.8rem 0;
      }
      
      .mobile-price-desc {
        font-size: 0.95rem;
      }
      
      .mobile-pricing-features {
        margin: 1rem 0;
      }
      
      .mobile-pricing-feature {
        font-size: 0.9rem;
        margin-bottom: 0.6rem;
        line-height: 1.4;
      }
      
      .mobile-pricing-button {
        padding: 0.8rem;
        font-size: 0.95rem;
        margin-top: 1rem;
      }
      
      /* General improvements for mobile */
      .mobile-section-heading {
        font-size: 1.6rem;
        margin-bottom: 0.5rem;
      }
      
      .mobile-section-subheading {
        font-size: 1rem;
        line-height: 1.5;
        margin-bottom: 1.5rem;
        padding: 0 0.5rem;
      }
      
      .mobile-action-buttons {
        flex-direction: column;
        gap: 0.8rem;
        margin-top: 2rem;
      }
      
      .mobile-action-button {
        width: 100%;
        justify-content: center;
        padding: 0.9rem;
        font-size: 1rem;
      }
    }
  </style>
</head>
<body class="overflow-x-hidden">

  <!-- Hero Section -->
  <header class="hero-section py-12 md:py-24 text-center relative">
    <div class="relative z-10 container mx-auto px-4">
      <div class="flex justify-center items-center mb-4 select-none">
        <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/DataGram-title.png" 
          alt="DataGram LeadsMiner Logo" 
          style="background: transparent;" 
          class="max-h-16 md:max-h-32 object-contain">
      </div>

      <h1 class="text-2xl md:text-4xl font-bold mb-4">DataGram LeadsMiner</h1>
      <p class="text-white text-lg md:text-2xl font-semibold max-w-3xl mx-auto leading-relaxed px-4 mb-6 md:mb-8">
        الطريقة الأذكى لجلب عملاء مهتمين بدون تكاليف إعلانات
      </p>
      <div class="flex flex-wrap justify-center gap-3 md:gap-4 mt-6 md:mt-8">
        <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-green px-6 py-3 rounded-lg text-base md:text-lg flex items-center btn-mobile">
          <i class="fas fa-download ml-2"></i> تنزيل الان
        </a>
        <a href="https://wa.me/201027930040" target="_blank" class="btn-white-bordered px-6 py-3 rounded-lg text-base md:text-lg flex items-center btn-mobile">
          <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
        </a>
      </div>
    </div>
  </header>

  <main class="bg-gray-50 text-gray-900">
    <!-- What is LeadsMiner -->
    <section id="about" class="py-10 md:py-20 bg-white mobile-section-padding">
      <div class="max-w-6xl mx-auto px-4 md:flex md:items-center md:gap-12">
        <div class="md:w-2/5 mb-8 md:mb-0 flex justify-center">
          <img
            src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/leadsminer%20logo.png"
            alt="شعار LeadsMiner مع رمز معول تعدين يصنع ثقوب في صخر، ألوان شعار أزرق ورمادي"
            class="leadminer-img modern-card max-w-[150px] md:max-w-[220px]"
          />
        </div>
        <div class="md:w-3/5 mobile-text-center md:text-right">
          <h2 class="text-2xl md:text-3xl font-bold mb-4 md:mb-6 text-primary-dark section-heading">ما هو LeadsMiner ؟</h2>
          <p class="text-base md:text-lg leading-relaxed text-gray-700 mb-6">
            LeadsMiner أداة قوية على نظام الويندوز، تعمل بنفس منطق الاستهداف الموجود في مدير الإعلانات الخاص بمواقع التواصل الاجتماعي مثل (فيسبوك، انستقرام، تيك توك) وتوصلك لعملاء دقيقين ومهتمين — وكل هذا بدون ما تدفع ولا ريال على الإعلانات.
          </p>
          <div class="flex flex-wrap justify-center md:justify-start gap-3 md:gap-4">
            <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-5 py-2.5 md:px-6 md:py-3 rounded-lg flex items-center btn-mobile text-sm md:text-base">
              <i class="fas fa-download ml-2"></i> تنزيل الان
            </a>
            <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-5 py-2.5 md:px-6 md:py-3 rounded-lg flex items-center btn-mobile text-sm md:text-base">
              <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section - Improved for Mobile -->
    <section id="features" class="py-12 md:py-16 bg-gradient-to-b from-white to-gray-50 mobile-feature-section">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-4 text-primary-dark section-heading text-center mobile-section-heading">ميزات LeadsMiner</h2>
        <p class="text-base md:text-lg text-center text-gray-600 max-w-3xl mx-auto mb-8 md:mb-12 mobile-section-subheading">اكتشف القوة الكاملة لأداة استخراج العملاء الرائدة في السوق</p>
        
        <div class="grid mobile-feature-grid md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6">
          <div class="feature-card animate-fade-in modern-card mobile-feature-card">
            <div class="text-secondary-light text-2xl md:text-3xl mb-3 md:mb-4 mobile-feature-icon"><i class="fas fa-users"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark mobile-feature-title">عملاء غير محدودين</h3>
            <p class="text-gray-700 text-sm md:text-base mobile-feature-desc">تقدر تستخرج عدد لا نهائي من العملاء المحتملين لعملك</p>
          </div>
          
          <div class="feature-card animate-fade-in modern-card mobile-feature-card">
            <div class="text-secondary-light text-2xl md:text-3xl mb-3 md:mb-4 mobile-feature-icon"><i class="fas fa-globe"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark mobile-feature-title">استهداف عالمي</h3>
            <p class="text-gray-700 text-sm md:text-base mobile-feature-desc">استهدف أي دولة في العالم مع دقة في التوصيل</p>
          </div>
          
          <div class="feature-card animate-fade-in modern-card mobile-feature-card">
            <div class="text-secondary-light text-2xl md:text-3xl mb-3 md:mb-4 mobile-feature-icon"><i class="fas fa-bullseye"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark mobile-feature-title">استهداف ذكي</h3>
            <p class="text-gray-700 text-sm md:text-base mobile-feature-desc">حدد اهتمامات العملاء، الفئة العمرية، النوع، وحتى مكان السكن</p>
          </div>
          
          <div class="feature-card animate-fade-in modern-card mobile-feature-card">
            <div class="text-secondary-light text-2xl md:text-3xl mb-3 md:mb-4 mobile-feature-icon"><i class="fas fa-shield-alt"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark mobile-feature-title">خصوصية وأمان</h3>
            <p class="text-gray-700 text-sm md:text-base mobile-feature-desc">بياناتك تبقى عندك وما تطلع لحد، بأعلى معايير الأمان</p>
          </div>
          
          <div class="feature-card animate-fade-in modern-card mobile-feature-card">
            <div class="text-secondary-light text-2xl md:text-3xl mb-3 md:mb-4 mobile-feature-icon"><i class="fas fa-money-bill-wave"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark mobile-feature-title">توفير المال</h3>
            <p class="text-gray-700 text-sm md:text-base mobile-feature-desc">وفر آلاف الريالات وتخلى عن الحملات الإعلانية المكلفة</p>
          </div>
          
          <div class="feature-card animate-fade-in modern-card mobile-feature-card">
            <div class="text-secondary-light text-2xl md:text-3xl mb-3 md:mb-4 mobile-feature-icon"><i class="fas fa-headset"></i></div>
            <h3 class="text-xl font-bold mb-2 text-primary-dark mobile-feature-title">دعم فني 24/7</h3>
            <p class="text-gray-700 text-sm md:text-base mobile-feature-desc">فريق دعم فني متاح على مدار الساعة لمساعدتك</p>
          </div>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-3 md:gap-4 mt-10 md:mt-12 mobile-action-buttons">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>

    <!-- How it works -->
    <section class="py-12 md:py-16 bg-primary-light text-white mobile-section-padding">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-8 md:mb-12 section-heading text-center mobile-section-heading">كيف يعمل LeadsMiner؟</h2>
        
          <div class="bg-primary rounded-xl p-4 md:p-8 mb-6 md:mb-8 modern-card">
            <div class="info-scroll space-y-4 mb-6 md:mb-8 flex justify-center">
              <video class="rounded-lg shadow-lg mobile-video" controls>
                <source src="howitworks.mp4" type="video/mp4">
                متصفحك لا يدعم تشغيل الفيديو.
              </video>
            </div>
          </div>


          <div class="text-center mt-8 md:mt-10">
            <h3 class="text-xl md:text-2xl font-extrabold mb-4 md:mb-6">جاهز تشترك ؟</h3>
            <div class="flex flex-wrap justify-center gap-3 md:gap-4">
              <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-6 py-3 rounded-lg text-base md:text-lg flex items-center btn-mobile">
                <i class="fas fa-download ml-2"></i> تنزيل الان
              </a>
              <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg text-base md:text-lg flex items-center btn-mobile">
                <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section - Improved for Mobile -->
    <section id="pricing" class="py-12 md:py-16 bg-gray-50 mobile-pricing-section">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-4 text-primary-dark section-heading text-center mobile-section-heading">باقات LeadsMiner</h2>
        <p class="text-base md:text-lg text-center text-gray-600 max-w-3xl mx-auto mb-8 md:mb-12 mobile-section-subheading">اختر الباقة المناسبة لاحتياجاتك وابدأ في زيادة مبيعاتك اليوم</p>

        <div class="mobile-pricing-grid md:grid md:grid-cols-3 md:gap-8">
          <!-- Beginner -->
          <div class="relative bg-white rounded-xl shadow-lg p-5 md:p-6 text-center text-gray-800 modern-card mobile-pricing-card">
            <div class="ribbon ribbon-blue">مبتدئ</div>
            <div class="my-5 md:my-6">
              <div class="text-3xl md:text-4xl font-bold text-primary-dark mobile-price">370$</div>
              <div class="text-gray-500 mt-2 text-sm md:text-base mobile-price-desc">شهرياً</div>
            </div>
            <ul class="text-right space-y-2 md:space-y-3 my-5 md:my-6 mobile-pricing-features">
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> اشتراك لمدة شهر واحد</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> عدد غير محدود من العملاء</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
            </ul>
            <a href="https://wa.me/201027930040" class="btn-blue w-full py-3 rounded-lg mt-5 md:mt-6 flex items-center justify-center mobile-pricing-button">
              <i class="fas fa-shopping-cart ml-2"></i> اشترك الآن
            </a>
          </div>

          <!-- Pro -->
          <div class="relative bg-white rounded-xl shadow-xl p-6 md:p-8 text-center text-gray-900 border-4 border-accent-light modern-card mobile-pricing-card featured">
            <div class="ribbon ribbon-green">الأكثر شهرة</div>
            <div class="my-5 md:my-6">
              <div class="text-3xl md:text-4xl font-bold text-primary-dark mobile-price">2999$</div>
              <div class="text-gray-500 mt-2 text-sm md:text-base mobile-price-desc">سنوياً <span class="text-green-600">(وفر 20%)</span></div>
            </div>
            <ul class="text-right space-y-2 md:space-y-3 my-5 md:my-6 mobile-pricing-features">
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> اشتراك لمدة عام كامل</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> عدد غير محدود من العملاء</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> تحديثات مجانية</li>
            </ul>
            <a href="https://wa.me/201027930040" class="btn-green w-full py-3 rounded-lg mt-5 md:mt-6 flex items-center justify-center mobile-pricing-button">
              <i class="fas fa-crown ml-2"></i> اشترك الآن
            </a>
          </div>

          <!-- Expert -->
          <div class="relative bg-white rounded-xl shadow-lg p-5 md:p-6 text-center text-gray-800 modern-card mobile-pricing-card">
            <div class="ribbon ribbon-gray">خبير</div>
            <div class="my-5 md:my-6">
              <div class="text-3xl md:text-4xl font-bold text-primary-dark mobile-price">3700$</div>
              <div class="text-gray-500 mt-2 text-sm md:text-base mobile-price-desc">دفعة واحدة</div>
            </div>
            <ul class="text-right space-y-2 md:space-y-3 my-5 md:my-6 mobile-pricing-features">
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> اشتراك مدى الحياة</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> عدد لا نهائي من العملاء</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
              <li class="flex items-center justify-end text-sm md:text-base mobile-pricing-feature"><span class="check-icon">✔</span> تحديثات مجانية دائمة</li>
            </ul>
            <a href="https://wa.me/201027930040" class="btn-blue w-full py-3 rounded-lg mt-5 md:mt-6 flex items-center justify-center mobile-pricing-button">
              <i class="fas fa-gem ml-2"></i> اشترك الآن
            </a>
          </div>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-3 md:gap-4 mt-10 md:mt-12 mobile-action-buttons">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-12 md:py-16 bg-white mobile-section-padding">
      <div class="max-w-4xl mx-auto px-4 text-center">
        <h2 class="text-2xl md:text-3xl font-bold mb-4 text-primary-dark section-heading text-center mobile-section-heading">تواصل معنا</h2>
        <p class="text-base md:text-lg text-gray-600 mb-6 md:mb-8 mobile-section-subheading">هل لديك استفسار أو تحتاج إلى مساعدة؟ فريقنا متاح لخدمتك</p>
        
        <div class="bg-blue-50 rounded-xl p-5 md:p-8 modern-card">
          <div class="flex flex-col md:flex-row justify-center items-center gap-4 md:gap-6 mb-6 md:mb-8">
            <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-5 py-2.5 md:px-6 md:py-3 rounded-lg flex items-center btn-mobile text-sm md:text-base">
              <i class="fab fa-whatsapp text-xl ml-2"></i> واتساب
            </a>
            <a href="mailto:info@datagram.site" class="btn-blue px-5 py-2.5 md:px-6 md:py-3 rounded-lg flex items-center btn-mobile text-sm md:text-base">
              <i class="fas fa-envelope text-xl ml-2"></i> البريد الإلكتروني
            </a>
          </div>
          
          <p class="text-primary-dark font-semibold text-base md:text-lg">
            <i class="fas fa-phone-alt ml-2"></i> +201027930040
          </p>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-3 md:gap-4 mt-10 md:mt-12 mobile-action-buttons">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-12 md:py-16 bg-gray-50 mobile-section-padding">
      <div class="max-w-4xl mx-auto px-4">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-4 text-primary-dark section-heading text-center mobile-section-heading">الأسئلة الشائعة</h2>
        
        <div class="space-y-4 mt-6 md:mt-8">
          <div class="bg-white rounded-xl p-5 md:p-6 shadow modern-card mobile-card">
            <h3 class="text-lg md:text-xl font-bold text-primary-dark mb-2">هل أحتاج إلى خبرة تقنية لاستخدام LeadsMiner؟</h3>
            <p class="text-gray-700 text-sm md:text-base">لا، LeadsMiner صمم ليكون سهل الاستخدام حتى لأولئك الذين ليست لديهم خلفية تقنية. واجهة المستخدم بسيطة وبديهية.</p>
          </div>
          
          <div class="bg-white rounded-xl p-5 md:p-6 shadow modern-card mobile-card">
            <h3 class="text-lg md:text-xl font-bold text-primary-dark mb-2">كم من الوقت يستغرق لبدء رؤية النتائج؟</h3>
            <p class="text-gray-700 text-sm md:text-base">معظم العملاء يبدأون في رؤية النتائج من الساعات الاولي، حيث يمكنك استخراج أول قائمة عملاء محتملين خلال اقل من ساعة واحدة من التثبيت.</p>
          </div>
        </div>
        
        <!-- Action buttons -->
        <div class="flex flex-wrap justify-center gap-3 md:gap-4 mt-10 md:mt-12 mobile-action-buttons">
          <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn-blue px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fas fa-download ml-2"></i> تنزيل الان
          </a>
          <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg text-base md:text-lg flex items-center mobile-action-button">
            <i class="fab fa-whatsapp ml-2"></i> تواصل معنا
          </a>
        </div>
      </div>
    </section>
  </main>

  <footer class="bg-primary-dark py-8 text-white mobile-footer">
    <div class="max-w-6xl mx-auto px-4 flex flex-col md:flex-row justify-between items-center">
      <div class="mb-6 md:mb-0">
        <div class="flex justify-center items-center mb-4 select-none">
          <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/DataGram-title.png" 
            alt="DataGram LeadsMiner Logo" 
            style="background: transparent;" 
            class="max-h-16 md:max-h-24 object-contain">
        </div>
        <p class="text-blue-200 mt-2 text-sm md:text-base">© 2025 جميع الحقوق محفوظة</p>
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
