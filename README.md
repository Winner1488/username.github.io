<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title id="page-title">CryptoReborn</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Poppins:wght@500;700&display=swap" rel="stylesheet">
  <style>
    *{box-sizing:border-box;margin:0;padding:0}
    body{font-family:'Montserrat',sans-serif;background:#0b0b0b;color:#eee;line-height:1.6;}
    header{background:#111;padding:20px 40px;position:sticky;top:0;display:flex;justify-content:space-between;align-items:center;z-index:100;}
    #site-name{color:#f2b93d;font-family:'Poppins',sans-serif;font-weight:700;font-size:2.4rem}
    .lang-switcher{position:relative;background:rgba(242,185,61,0.1);padding:6px 12px;border-radius:20px;}
    .lang-switcher::after{content:'▾';color:#eee;position:absolute;right:12px;top:50%;transform:translateY(-50%);}
    #language-select{appearance:none;background:transparent;border:none;color:#eee;font-size:1rem;padding-right:20px;cursor:pointer}
    .hero{position:relative;display:flex;flex-direction:column;justify-content:center;align-items:center;height:100vh;text-align:center;background:linear-gradient(135deg,#1a1a1a,#0b0b0b);overflow:hidden;}
    .hero::before{content:'';position:absolute;top:0;left:0;width:100%;height:100%;background:radial-gradient(circle at 30% 40%,rgba(242,185,61,0.2),transparent 60%),radial-gradient(circle at 70% 60%,rgba(15,255,255,0.2),transparent 60%);z-index:1}
    .coin{position:absolute;bottom:-40px;width:40px;height:40px;background:rgba(242,185,61,0.3);border-radius:50%;animation:floatCoin 7s ease-in-out infinite;}
    @keyframes floatCoin{0%,100%{transform:translateY(0) scale(.8);opacity:0}10%,90%{opacity:1}50%{transform:translateY(-400px) scale(1);opacity:.7}}
    .hero-content{position:relative;z-index:2;max-width:600px;padding:0 20px}
    .hero h2{font-family:'Poppins',sans-serif;font-size:3rem;color:#f2b93d;margin-bottom:.5rem;text-shadow:0 2px 10px rgba(0,0,0,0.5);}
    .hero p{font-size:1.2rem;color:#ccc;margin-bottom:1rem;}
    section{padding:60px 24px;max-width:1100px;margin:auto}
    .block {
      background: rgba(255,255,255,0.04);
      border-radius: 20px;
      padding: 40px;
      margin-bottom: 48px;
      opacity: 1;
      transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease;
    }
    .block:hover {
      transform: translateY(-6px);
      background: rgba(242,185,61,0.1);
      box-shadow: 0 12px 30px rgba(242,185,61,0.5);
    }
    .block h2{font-family:'Poppins',sans-serif;color:#f2b93d;font-size:2.4rem;margin-bottom:16px}
    .block p, .block li{font-size:1rem;color:#ddd;margin-top:12px;line-height:1.6}
    ul{padding-left:1.3em;margin:15px 0;}
    li{margin-bottom:8px;}
    .services-list{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:20px;margin-top:20px;}
    .service-item{background:rgba(242,185,61,0.1);padding:20px;border-radius:12px;color:#ddd;display:flex;flex-direction:column;align-items:center;transition:transform 0.3s ease,background 0.3s ease;text-align:center;min-height:150px;}
    .service-item:hover{background:#f2b93d;color:#111;transform:translateY(-4px);}
    .service-icon{font-size:2rem;margin-bottom:12px;transition:transform 0.3s ease,color 0.3s ease;}
    .service-item:hover .service-icon{transform:scale(1.2);color:#111;}
    .contact-button{padding:12px 30px;background:#f2b93d;border:none;border-radius:30px;color:#111;font-weight:700;cursor:pointer;margin-top:15px;transition:all 0.3s ease;}
    .contact-button:hover{background:#e0a732;transform:translateY(-3px);box-shadow:0 5px 15px rgba(242,185,61,0.4);}
    #contact-info{display:none;background:rgba(242,185,61,0.1);padding:20px;border-radius:12px;margin-top:20px;}

    /* Адаптивность */
    @media (max-width: 768px) {
      header{padding:15px 20px;}
      #site-name{font-size:1.8rem;}
      .hero h2{font-size:2.2rem;}
      .hero p{font-size:1rem;}
      .block{padding:25px;}
      .block h2{font-size:1.8rem;}
    }
  </style>
</head>
<body>
  <header>
    <h1 id="site-name" data-i18n="siteName">CryptoReborn</h1>
    <div class="lang-switcher">
      <select id="language-select">
        <option value="uk">🇺🇦 Українська</option>
        <option value="ru">🇷🇺 Русский</option>
        <option value="en">🇬🇧 English</option>
      </select>
    </div>
  </header>

  <div class="hero">
    <div class="coin"></div><div class="coin"></div><div class="coin"></div>
    <div class="coin"></div><div class="coin"></div><div class="coin"></div>
    <div class="hero-content">
      <h2 data-i18n="heroTitle">Відновіть доступ до своїх криптоактивів</h2>
      <p data-i18n="heroSubtitle">CryptoReborn поверне ваш гаманець до життя — швидко, безпечно й конфіденційно.</p>
    </div>
  </div>

  <section class="block">
    <h2 data-i18n="aboutTitle">Про нас</h2>
    <p data-i18n="aboutText">Ми — експерти з криптографії та безпеки, що допомагають відновлювати втрачені ключі й seed-фрази. Понад 1000 клієнтів вже довірили нам свої активи.</p>
  </section>

  <section class="block">
    <h2 data-i18n="servicesTitle">Що ми пропонуємо</h2>
    <div class="services-list">
      <div class="service-item">
        <span class="service-icon">🔑</span>
        <span data-i18n="service1">Відновлення втрачених приватних ключів і паролів</span>
      </div>
      <div class="service-item">
        <span class="service-icon">🗝️</span>
        <span data-i18n="service2">Підбір та відновлення seed-фраз</span>
      </div>
      <div class="service-item">
        <span class="service-icon">🛠️</span>
        <span data-i18n="service3">Аналіз і відновлення пошкоджених криптогаманців</span>
      </div>
      <div class="service-item">
        <span class="service-icon">🔒</span>
        <span data-i18n="service4">Консультації з безпеці криптоактивів</span>
      </div>
      <div class="service-item">
        <span class="service-icon">🤝</span>
        <span data-i18n="service5">Індивідуальні рішення під складні випадки</span>
      </div>
      <div class="service-item">
        <span class="service-icon">💼</span>
        <span data-i18n="service6">Професійна допомога з відновленням доступу будь-яких криптовалют</span>
      </div>
    </div>
  </section>

  <section class="block">
    <h2 data-i18n="securityTitle">Безпека</h2>
    <p data-i18n="securityText">Ніяких приватних ключів. Повна анонімність. Власні алгоритми шифрування та захищене середовище.</p>
  </section>

  <section class="block">
    <h2 data-i18n="faqTitle">Поширені запитання</h2>
    <ul>
      <li><strong data-i18n="faq1_q">Чи безпечно надавати вам дані?</strong> <span data-i18n="faq1_a">Так, усе конфіденційно і захищено.</span></li>
      <li><strong data-i18n="faq2_q">Що робити, якщо пам’ятаю тільки частину фрази?</strong> <span data-i18n="faq2_a">Ми можемо допомогти підібрати відсутні частини.</span></li>
      <li><strong data-i18n="faq3_q">Скільки триває процес?</strong> <span data-i18n="faq3_a">Від кількох годин до 2–3 днів.</span></li>
    </ul>
  </section>

  <section class="block">
    <h2 data-i18n="casesTitle">Приклади успішних кейсів</h2>
    <p><strong data-i18n="case1_title">Кейс №1:</strong> <span data-i18n="case1_text">Клієнт зберіг лише 10 слів із 12. Наш алгоритм відновив гаманець за 16 годин.</span></p>
    <p><strong data-i18n="case2_title">Кейс №2:</strong> <span data-i18n="case2_text">Втрачено файл із паролем. Ми перевірили понад 5000 варіантів і знайшли підходящий.</span></p>
  </section>

  <section class="block">
    <h2 data-i18n="toolsTitle">Наші інструменти</h2>
    <ul>
      <li data-i18n="tools1">Підтримка понад 500 криптовалют</li>
      <li data-i18n="tools2">Відновлення seed-фраз і wallet.dat файлів</li>
      <li data-i18n="tools3">Генерація паролів з маскою</li>
      <li data-i18n="tools4">Оптимізована багатопоточна обробка</li>
      <li data-i18n="tools5">Повна автономність та конфіденційність</li>
    </ul>
  </section>

  <section class="block">
    <h2 data-i18n="contactTitle">Зв’язатися з нами</h2>
    <p data-i18n="contactText">Натисніть кнопку, щоб дізнатись нашу email-адресу.</p>
    <button class="contact-button" id="reveal-email" data-i18n="contactButton">Написати нам</button>
    <p id="contact-info" data-i18n="contactInfo">Пишіть нам: secure.wallet.hellp@gmail.com<br>Ми відповімо протягом 48 годин.</p>
  </section>

  <script>
    const translations = {
      uk: {
        siteName: "CryptoReborn",
        pageTitle: "CryptoReborn – Відновлення криптовалют",
        heroTitle: "Відновіть доступ до своїх криптоактивів",
        heroSubtitle: "CryptoReborn поверне ваш гаманець до життя — швидко, безпечно й конфіденційно.",
        aboutTitle: "Про нас",
        aboutText: "Ми — експерти з криптографії та безпеки, що допомагають відновлювати втрачені ключі й seed-фрази. Понад 1000 клієнтів вже довірили нам свої активи.",
        servicesTitle: "Що ми пропонуємо",
        service1: "Відновлення втрачених приватних ключів і паролів",
        service2: "Підбір та відновлення seed-фраз",
        service3: "Аналіз і відновлення пошкоджених криптогаманців",
        service4: "Консультації з безпеці криптоактивів",
        service5: "Індивідуальні рішення під складні випадки",
        service6: "Професійна допомога з відновленням доступу будь-яких криптовалют",
        securityTitle: "Безпека",
        securityText: "Ніяких приватних ключів. Повна анонімність. Власні алгоритми шифрування та захищене середовище.",
        faqTitle: "Поширені запитання",
        faq1_q: "Чи безпечно надавати вам дані?",
        faq1_a: "Так, усе конфіденційно і захищено.",
        faq2_q: "Що робити, якщо пам’ятаю тільки частину фрази?",
        faq2_a: "Ми можемо допомогти підібрати відсутні частини.",
        faq3_q: "Скільки триває процес?",
        faq3_a: "Від кількох годин до 2–3 днів.",
        casesTitle: "Приклади успішних кейсів",
        case1_title: "Кейс №1:",
        case1_text: "Клієнт зберіг лише 10 слів із 12. Наш алгоритм відновив гаманець за 16 годин.",
        case2_title: "Кейс №2:",
        case2_text: "Втрачено файл із паролем. Ми перевірили понад 5000 варіантів і знайшли підходящий.",
        toolsTitle: "Наші інструменти",
        tools1: "Підтримка понад 500 криптовалют",
        tools2: "Відновлення seed-фраз і wallet.dat файлів",
        tools3: "Генерація паролів з маскою",
        tools4: "Оптимізована багатопоточна обробка",
        tools5: "Повна автономність та конфіденційність",
        contactTitle: "Зв’язатися з нами",
        contactText: "Натисніть кнопку, щоб дізнатись нашу email-адресу.",
        contactButton: "Написати нам",
        contactInfo: "Пишіть нам: secure.wallet.hellp@gmail.com<br>Ми відповімо протягом 48 годин."
      },
      ru: {
        siteName: "CryptoReborn",
        pageTitle: "CryptoReborn – Восстановление криптовалют",
        heroTitle: "Восстановите доступ к своим криптоактивам",
        heroSubtitle: "CryptoReborn вернет ваш кошелек к жизни — быстро, безопасно и конфиденциально.",
        aboutTitle: "О нас",
        aboutText: "Мы — эксперты по криптографии и безопасности, помогаем восстанавливать утраченные ключи и seed-фразы. Более 1000 клиентов уже доверили нам свои активы.",
        servicesTitle: "Что мы предлагаем",
        service1: "Восстановление утраченных приватных ключей и паролей",
        service2: "Подбор и восстановление seed-фраз",
        service3: "Анализ и ремонт поврежденных криптокошельков",
        service4: "Консультации по безопасности криптоактивов",
        service5: "Индивидуальные решения для сложных случаев",
        service6: "Профессиональная помощь в восстановлении доступа к любым криптовалютам",
        securityTitle: "Безопасность",
        securityText: "Никаких приватных ключей. Полная анонимность. Собственные алгоритмы шифрования и защищенное окружение.",
        faqTitle: "Часто задаваемые вопросы",
        faq1_q: "Безопасно ли предоставлять вам данные?",
        faq1_a: "Да, все конфиденциально и защищено.",
        faq2_q: "Что делать если помню только часть фразы?",
        faq2_a: "Мы можем помочь подобрать недостающие части.",
        faq3_q: "Сколько длится процесс?",
        faq3_a: "От нескольких часов до 2–3 дней.",
        casesTitle: "Примеры успешных кейсов",
        case1_title: "Кейс №1:",
        case1_text: "Клиент сохранил только 10 слов из 12. Наш алгоритм восстановил кошелек за 16 часов.",
        case2_title: "Кейс №2:",
        case2_text: "Файл с паролем был утерян. Мы проверили более 5000 вариантов и нашли подходящий.",
        toolsTitle: "Наши инструменты",
        tools1: "Поддержка более 500 криптовалют",
        tools2: "Восстановление seed-фраз и wallet.dat файлов",
        tools3: "Генерация паролей с маской",
        tools4: "Оптимизированная многопоточность",
        tools5: "Полная автономность и конфиденциальность",
        contactTitle: "Связаться с нами",
        contactText: "Нажмите кнопку, чтобы узнать наш email.",
        contactButton: "Написать нам",
        contactInfo: "Пишите нам: secure.wallet.hellp@gmail.com<br>Мы ответим в течение 48 часов."
      },
      en: {
        siteName: "CryptoReborn",
        pageTitle: "CryptoReborn – Cryptocurrency Recovery",
        heroTitle: "Restore Access to Your Crypto Assets",
        heroSubtitle: "CryptoReborn will bring your wallet back to life — fast, secure, and confidential.",
        aboutTitle: "About Us",
        aboutText: "We are cryptography and security experts helping recover lost keys and seed phrases. Over 1,000 clients have trusted us with their assets.",
        servicesTitle: "What We Offer",
        service1: "Recovery of lost private keys and passwords",
        service2: "Seed phrase recovery and restoration",
        service3: "Analysis and repair of corrupted crypto wallets",
        service4: "Crypto asset security consultations",
        service5: "Custom solutions for complex cases",
        service6: "Professional support for all cryptocurrency recoveries",
        securityTitle: "Security",
        securityText: "No private keys. Complete anonymity. Proprietary encryption algorithms and a secure environment.",
        faqTitle: "Frequently Asked Questions",
        faq1_q: "Is it safe to provide you with my data?",
        faq1_a: "Yes, everything is confidential and protected.",
        faq2_q: "What if I only remember part of my seed phrase?",
        faq2_a: "We can help reconstruct the missing parts.",
        faq3_q: "How long does the process take?",
        faq3_a: "From a few hours up to 2–3 days.",
        casesTitle: "Success Stories",
        case1_title: "Case #1:",
        case1_text: "Client retained only 10 of 12 words. Our algorithm recovered the wallet in 16 hours.",
        case2_title: "Case #2:",
        case2_text: "Password file was lost. We ran over 5000 variations and found the correct combination.",
        toolsTitle: "Our Tools",
        tools1: "Support for 500+ cryptocurrencies",
        tools2: "Seed phrase & wallet.dat recovery",
        tools3: "Custom password mask generation",
        tools4: "Optimized multithreaded performance",
        tools5: "Fully offline and private",
        contactTitle: "Contact Us",
        contactText: "Click the button to reveal our email address.",
        contactButton: "Write to Us",
        contactInfo: "Email us at: secure.wallet.hellp@gmail.com<br>We will respond within 48 hours."
      }
    };

    function applyTranslations(lang) {
      const dict = translations[lang] || translations.uk;
      
      // Обновляем язык документа
      document.documentElement.lang = lang;
      
      // Обновляем заголовок страницы
      document.title = dict.pageTitle;
      
      // Обновляем все элементы с data-i18n
      document.querySelectorAll('[data-i18n]').forEach(el => {
        const key = el.getAttribute('data-i18n');
        if (dict[key]) {
          // Для элементов с HTML используем innerHTML
          if (key === 'contactInfo' || key === 'securityText' || key === 'aboutText') {
            el.innerHTML = dict[key];
          } else {
            el.textContent = dict[key];
          }
        }
      });
      
      // Обновляем выбранный язык в селекторе
      const langSelect = document.getElementById('language-select');
      langSelect.value = lang;
    }

    document.addEventListener('DOMContentLoaded', () => {
      // Определяем язык пользователя
      let userLang = navigator.language.slice(0,2);
      if (!translations[userLang]) userLang = 'uk';
      applyTranslations(userLang);
      
      // Обработчик изменения языка
      document.getElementById('language-select').addEventListener('change', (e) => {
        applyTranslations(e.target.value);
      });
      
      // Кнопка раскрытия email
      const revealBtn = document.getElementById('reveal-email');
      const contactInfo = document.getElementById('contact-info');
      
      if (revealBtn && contactInfo) {
        contactInfo.style.display = 'none';
        revealBtn.addEventListener('click', () => {
          revealBtn.style.display = 'none';
          contactInfo.style.display = 'block';
        });
      }
      
      // Анимация монет
      const coins = document.querySelectorAll('.coin');
      coins.forEach((coin, index) => {
        coin.style.left = `${10 + index * 15}%`;
        coin.style.animationDelay = `${index * 0.5}s`;
      });
    });
  </script>
</body>
</html># username.github.io
