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
    
    /* Improved mobile-specific styles */
    @media (max-width: 767px) {
      /* Features section improvements */
      .mobile-feature-section {
        padding: 2rem 1rem;
      }
      
      .mobile-feature-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
        margin-top: 1.5rem;
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
    
    /* Existing styles */
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
    
    .check-icon {
      color: #7ae7a2;
      font-weight: 800;
      font-size: 1.3rem;
      margin-left: 0.5rem;
    }
    
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
    
    /* Animation */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fade-in {
      animation: fadeIn 1s ease-out forwards;
    }
  </style>
</head>
<body class="overflow-x-hidden">

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

  <script>
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
