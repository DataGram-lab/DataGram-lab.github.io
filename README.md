<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>DataGram LeadsMiner - أداة استخراج العملاء</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    body {
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0f3f80 0%, #1e60b0 100%);
      color: white;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      scroll-behavior: smooth;
    }
    .btn-blue {
      background: #0ea5e9;
      color: white;
      transition: all 0.3s ease;
      border: 2px solid #0ea5e9;
    }
    .btn-blue:hover {
      background: #0284c7;
      border-color: #0284c7;
      transform: translateY(-2px);
    }
    .btn-green {
      background: #4ade80;
      color: #064e3b;
      transition: all 0.3s ease;
      border: 2px solid #4ade80;
      font-weight: 600;
      box-shadow: 0 4px 8px rgba(74, 222, 128, 0.4);
    }
    .btn-green:hover {
      background: #22c55e;
      border-color: #22c55e;
      box-shadow: 0 6px 12px rgba(34, 197, 94, 0.6);
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
      background-color: #4ade80;
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
      background-color: #3b82f6;
      color: white;
      right: 0.5rem;
    }
    .ribbon-green {
      background-color: #22c55e;
      color: white;
      left: 0.5rem;
    }
    .ribbon-gray {
      background-color: #6b7280;
      color: white;
      left: 0.5rem;
    }
    /* Custom checkbox icons */
    .check-icon {
      color: #4ade80;
      font-weight: 800;
      font-size: 1.3rem;
      margin-left: 0.5rem;
    }
    /* Logo stylization */
    .logo-letter {
      font-weight: 900;
      color: #2e77d0;
    }
    .logo-letter.d-blue {
      color: #0ea5e9;
    }
    /* Image container styling */
    .leadminer-img {
      max-width: 130px;
      margin: 0 auto 1rem auto;
      display: block;
    }
    /* Feature cards */
    .feature-card {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      padding: 1.5rem;
      transition: all 0.3s ease;
      height: 100%;
    }
    .feature-card:hover {
      transform: translateY(-5px);
      background: rgba(255, 255, 255, 0.15);
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
      background: rgba(15, 63, 128, 0.85);
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
        max-width: 180px;
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
  </style>
</head>
<body class="overflow-x-hidden">

  <!-- Hero Section -->
  <header class="hero-section py-16 md:py-24 text-center relative">
    <div class="relative z-10">
      <h1 class="text-4xl md:text-5xl font-extrabold mb-4 flex justify-center items-center gap-1 select-none">
        <span class="logo-letter d-blue">D</span>ataGram
        <span class="bg-blue-500 text-white text-sm px-2 py-1 rounded-full ml-2">LeadsMiner</span>
      </h1>
      <p class="text-white text-xl md:text-2xl font-semibold max-w-3xl mx-auto leading-relaxed px-4 mb-8">
        الطريقة الأذكى لجلب عملاء مهتمين بدون إعلانات
      </p>
      <div class="flex flex-wrap justify-center gap-4 mt-8">
        <button class="btn-green px-8 py-3 rounded-lg text-lg" onclick="scrollToSection('pricing')">
          ابدأ الآن <i class="fas fa-arrow-left mr-2"></i>
        </button>
        <button class="btn-white-bordered px-8 py-3 rounded-lg text-lg" onclick="scrollToSection('features')">
          اكتشف الميزات <i class="fas fa-star mr-2"></i>
        </button>
      </div>
    </div>
  </header>

  <main class="bg-gray-100 text-gray-900">
    <!-- What is LeadsMiner -->
    <section id="about" class="py-12 md:py-16 bg-white">
      <div class="max-w-6xl mx-auto px-4 md:flex md:items-center md:gap-12">
        <div class="md:w-2/5 mb-8 md:mb-0 flex justify-center">
          <img
            src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/5aaaee32-4b3f-4612-b0c0-dfca2106d9f7.png"
            alt="شعار LeadsMiner مع رمز معول تعدين يصنع ثقوب في صخر، ألوان شعار أزرق ورمادي"
            class="leadminer-img rounded-lg shadow-lg"
            onerror="this.onerror=null;this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/00edd5a0-2b8f-4117-a5f7-20105e840832.png';"
          />
        </div>
        <div class="md:w-3/5">
          <h2 class="text-3xl font-bold mb-6 text-blue-900 border-r-4 border-blue-500 pr-4">ما هو LeadsMiner ؟</h2>
          <p class="text-lg leading-relaxed text-gray-700 mb-6">
            LeadsMiner أداة قوية على نظام الويندوز، تعمل بنفس منطق الاستهداف الموجود في مدير الإعلانات الخاص بمواقع التواصل الاجتماعي مثل (فيسبوك، انستقرام، تيك توك) وتوصلك لعملاء دقيقين ومهتمين — وكل هذا بدون ما تدفع ولا ريال على الإعلانات.
          </p>
          <div class="flex flex-wrap gap-4">
            <button class="btn-blue px-6 py-3 rounded-lg">
              <i class="fas fa-download ml-2"></i> تنزيل الان
            </button>
            <button class="btn-green px-6 py-3 rounded-lg" onclick="scrollToSection('contact')">
              <i class="fas fa-comments ml-2"></i> تواصل معنا
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-16 bg-gradient-to-b from-white to-gray-100">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-4 text-blue-900">ميزات LeadsMiner</h2>
        <p class="text-lg text-center text-gray-600 max-w-3xl mx-auto mb-12">اكتشف القوة الكاملة لأداة استخراج العملاء الرائدة في السوق</p>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="feature-card animate-fade-in">
            <div class="text-blue-500 text-3xl mb-4"><i class="fas fa-users"></i></div>
            <h3 class="text-xl font-bold mb-2 text-blue-900">عملاء غير محدودين</h3>
            <p class="text-gray-700">تقدر تستخرج عدد لا نهائي من العملاء المحتملين لعملك</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-blue-500 text-3xl mb-4"><i class="fas fa-globe"></i></div>
            <h3 class="text-xl font-bold mb-2 text-blue-900">استهداف عالمي</h3>
            <p class="text-gray-700">استهدف أي دولة في العالم مع دقة في التوصيل</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-blue-500 text-3xl mb-4"><i class="fas fa-bullseye"></i></div>
            <h3 class="text-xl font-bold mb-2 text-blue-900">استهداف ذكي</h3>
            <p class="text-gray-700">حدد اهتمامات العملاء، الفئة العمرية، النوع، وحتى مكان السكن</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-blue-500 text-3xl mb-4"><i class="fas fa-shield-alt"></i></div>
            <h3 class="text-xl font-bold mb-2 text-blue-900">خصوصية وأمان</h3>
            <p class="text-gray-700">بياناتك تبقى عندك وما تطلع لحد، بأعلى معايير الأمان</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-blue-500 text-3xl mb-4"><i class="fas fa-money-bill-wave"></i></div>
            <h3 class="text-xl font-bold mb-2 text-blue-900">توفير المال</h3>
            <p class="text-gray-700">وفر آلاف الريالات وتخلى عن الحملات الإعلانية المكلفة</p>
          </div>
          
          <div class="feature-card animate-fade-in">
            <div class="text-blue-500 text-3xl mb-4"><i class="fas fa-headset"></i></div>
            <h3 class="text-xl font-bold mb-2 text-blue-900">دعم فني 24/7</h3>
            <p class="text-gray-700">فريق دعم فني متاح على مدار الساعة لمساعدتك</p>
          </div>
        </div>
      </div>
    </section>

    <!-- How it works -->
    <section class="py-16 bg-blue-900 text-white">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">كيف يعمل LeadsMiner؟</h2>
        
        <div class="bg-blue-800 rounded-xl p-6 md:p-8 mb-8">
          <div class="info-scroll space-y-4 mb-8">
            <ul class="list-none text-lg">
              <li class="flex items-center gap-2 mb-4 p-3 bg-blue-700 rounded-lg"><span class="check-icon">✔</span> عملاء غير محدودة : تقدر تستخرج عدد لا نهائي من العملاء</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-blue-700 rounded-lg"><span class="check-icon">✔</span> استهداف مفتوح لكل دول العالم : تختار الدولة اللي تبغا وتوصل لها</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-blue-700 rounded-lg"><span class="check-icon">✔</span> استهداف ذكي : تحدد اهتمامات العميل، الفئة العمرية، النوع، وحتى مكان السكن</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-blue-700 rounded-lg"><span class="check-icon">✔</span> استهداف دقيق - زي نظام إعلانات فيسبوك و انستجرام يوصل لك جمهورك المثالي</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-blue-700 rounded-lg"><span class="check-icon">✔</span> بدون إعلانات - ووفر آلاف الريالات وتخلى عن الحملات المدفوعة</li>
              <li class="flex items-center gap-2 mb-4 p-3 bg-blue-700 rounded-lg"><span class="check-icon">✔</span> خصوصية وأمان - بياناتك تبقى عندك وما تطلع لحد</li>
            </ul>
          </div>

          <div class="text-center mt-10">
            <h3 class="text-2xl font-extrabold mb-6">جاهز تشتريك ؟</h3>
            <div class="flex flex-wrap justify-center gap-4">
              <button class="btn-blue px-8 py-3 rounded-lg text-lg">
                <i class="fas fa-download ml-2"></i> تنزيل الان
              </button>
              <button class="btn-green px-8 py-3 rounded-lg text-lg" onclick="scrollToSection('pricing')">
                <i class="fas fa-tags ml-2"></i> عرض الباقات
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="py-16 bg-gray-100">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-4 text-blue-900">باقات LeadsMiner</h2>
        <p class="text-lg text-center text-gray-600 max-w-3xl mx-auto mb-12">اختر الباقة المناسبة لاحتياجاتك وابدأ في زيادة مبيعاتك اليوم</p>

        <div class="pricing-grid grid grid-cols-1 gap-8 md:grid-cols-3">
          <!-- Beginner -->
          <div class="relative bg-white rounded-xl shadow-lg p-6 text-center text-gray-800 transform hover:scale-105 transition-transform duration-300">
            <div class="ribbon ribbon-blue">مبتدئ</div>
            <div class="my-6">
              <div class="text-4xl font-bold text-blue-900">370$</div>
              <div class="text-gray-500 mt-2">شهرياً</div>
            </div>
            <ul class="text-right space-y-3 my-6">
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> اشتراك لمدة شهر واحد</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> عدد غير محدود من العملاء</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
            </ul>
            <button class="btn-blue w-full py-3 rounded-lg mt-6">
              <i class="fas fa-shopping-cart ml-2"></i> اشترك الآن
            </button>
          </div>

          <!-- Pro -->
          <div class="relative bg-white rounded-xl shadow-xl p-8 text-center text-gray-900 transform scale-105 border-4 border-green-400 z-10">
            <div class="ribbon ribbon-green">الأكثر شهرة</div>
            <div class="my-6">
              <div class="text-4xl font-bold text-blue-900">2999$</div>
              <div class="text-gray-500 mt-2">سنوياً <span class="text-green-600">(وفر 20%)</span></div>
            </div>
            <ul class="text-right space-y-3 my-6">
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> اشتراك لمدة عام كامل</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> عدد غير محدود من العملاء</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> تحديثات مجانية</li>
            </ul>
            <button class="btn-green w-full py-3 rounded-lg mt-6">
              <i class="fas fa-crown ml-2"></i> اشترك الآن
            </button>
          </div>

          <!-- Expert -->
          <div class="relative bg-white rounded-xl shadow-lg p-6 text-center text-gray-800 transform hover:scale-105 transition-transform duration-300">
            <div class="ribbon ribbon-gray">خبير</div>
            <div class="my-6">
              <div class="text-4xl font-bold text-blue-900">3700$</div>
              <div class="text-gray-500 mt-2">دفعة واحدة</div>
            </div>
            <ul class="text-right space-y-3 my-6">
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> اشتراك مدى الحياة</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> عدد لا نهائي من العملاء</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> استهداف دولي مفتوح</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> دعم فني 24 ساعة</li>
              <li class="flex items-center justify-end"><span class="check-icon">✔</span> تحديثات مجانية دائمة</li>
            </ul>
            <button class="btn-blue w-full py-3 rounded-lg mt-6">
              <i class="fas fa-gem ml-2"></i> اشترك الآن
            </button>
          </div>
        </div>

        <p class="text-center text-gray-600 mt-8">جميع الباقات تشمل ضمان استرداد الأموال خلال 14 يوم</p>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-white">
      <div class="max-w-4xl mx-auto px-4 text-center">
        <h2 class="text-3xl font-bold mb-4 text-blue-900">تواصل معنا</h2>
        <p class="text-lg text-gray-600 mb-8">هل لديك استفسار أو تحتاج إلى مساعدة؟ فريقنا متاح لخدمتك</p>
        
        <div class="bg-blue-50 rounded-xl p-8">
          <div class="flex flex-col md:flex-row justify-center items-center gap-6 mb-8">
            <a href="https://wa.me/201027930040" target="_blank" class="btn-green px-6 py-3 rounded-lg flex items-center">
              <i class="fab fa-whatsapp text-2xl ml-2"></i> واتساب
            </a>
            <a href="mailto:info@datagram.com" class="btn-blue px-6 py-3 rounded-lg flex items-center">
              <i class="fas fa-envelope text-2xl ml-2"></i> البريد الإلكتروني
            </a>
          </div>
          
          <p class="text-blue-900 font-semibold">
            <i class="fas fa-phone-alt ml-2"></i> +20 10 279 300 40
          </p>
          <p class="text-gray-600 mt-2">متاحين من الساعة 9 صباحاً حتى 5 مساءً (بتوقيت السعودية)</p>
        </div>
      </div>
    </section>
  </main>

  <!-- FAQ Section -->
  <section class="py-16 bg-gray-100">
    <div class="max-w-4xl mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-4 text-blue-900">الأسئلة الشائعة</h2>
      
      <div class="space-y-4 mt-8">
        <div class="bg-white rounded-xl p-6 shadow">
          <h3 class="text-xl font-bold text-blue-900 mb-2">هل أحتاج إلى خبرة تقنية لاستخدام LeadsMiner؟</h3>
          <p class="text-gray-700">لا، LeadsMiner صمم ليكون سهل الاستخدام حتى لأولئك الذين ليست لديهم خلفية تقنية. واجهة المستخدم بسيطة وبديهية.</p>
        </div>
        
        <div class="bg-white rounded-xl p-6 shadow">
          <h3 class="text-xl font-bold text-blue-900 mb-2">كم من الوقت يستغرق لبدء رؤية النتائج؟</h3>
          <p class="text-gray-700">معظم العملاء يبدأون في رؤية النتائج من اليوم الأول، حيث يمكنك استخراج أول قائمة عملاء محتملين خلال ساعات من التثبيت.</p>
        </div>
        
        <div class="bg-white rounded-xl p-6 shadow">
          <h3 class="text-xl font-bold text-blue-900 mb-2">هل هناك ضمان لاسترداد الأموال؟</h3>
          <p class="text-gray-700">نعم، نقدم ضمان استرداد الأموال خلال 14 يوم إذا لم تكن راضياً عن الخدمة لأي سبب من الأسباب.</p>
        </div>
      </div>
    </div>
  </section>

  <footer class="bg-blue-900 py-8 text-white">
    <div class="max-w-6xl mx-auto px-4 flex flex-col md:flex-row justify-between items-center">
      <div class="mb-6 md:mb-0">
        <h1 class="text-2xl font-extrabold flex items-center gap-1">
          <span class="logo-letter d-blue">D</span>ataGram
          <span class="text-sm bg-blue-700 px-2 py-1 rounded-full mr-2">LeadsMiner</span>
        </h1>
        <p class="text-blue-200 mt-2">© 2023 جميع الحقوق محفوظة</p>
      </div>
      
      <div class="flex flex-col items-center md:items-end">
        <a href="https://wa.me/201027930040" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 text-green-400 font-semibold hover:text-green-300 transition-colors mb-2">
          <i class="fab fa-whatsapp text-xl"></i>
          <span>+20 10 279 300 40</span>
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
