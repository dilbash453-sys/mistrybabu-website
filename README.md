# mistrybabu-website<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MistryBabu.com - पूरे बिहार के मिस्त्री और लेबर ऑनलाइन</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Hind:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Hind', sans-serif; }
  </style>
</head>
<body class="bg-gray-100 min-h-screen text-gray-800 pb-16">

  <header class="bg-gradient-to-r from-orange-600 to-amber-600 text-white shadow-md sticky top-0 z-50">
    <div class="max-w-md mx-auto px-4 py-3 flex items-center justify-between">
      <div class="flex items-center space-x-2">
        <div class="bg-white text-orange-600 font-black px-2.5 py-1 rounded shadow text-lg">MB</div>
        <div>
          <h1 class="text-xl font-bold leading-none tracking-tight">MistryBabu<span class="text-yellow-300">.com</span></h1>
          <p class="text-[11px] text-orange-100 font-medium">पूरे बिहार के मिस्त्री & लेबर अब ऑनलाइन</p>
        </div>
      </div>
      <span class="bg-orange-800/60 text-xs px-2.5 py-1 rounded-full border border-orange-400/40">38 जिले</span>
    </div>
  </header>

  <nav class="max-w-md mx-auto bg-white border-b border-gray-200 sticky top-[57px] z-40 flex shadow-sm">
    <button onclick="switchTab('find-mason')" id="tab-find" class="flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-orange-600 text-orange-600 transition">
      👷 मिस्त्री खोजें
    </button>
    <button onclick="switchTab('post-job')" id="tab-post" class="flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-transparent text-gray-500 hover:text-orange-600 transition">
      🏠 काम पोस्ट करें
    </button>
    <button onclick="switchTab('register-mason')" id="tab-reg" class="flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-transparent text-gray-500 hover:text-orange-600 transition">
      📝 मिस्त्री/लेबर जुड़ें
    </button>
  </nav>

  <main class="max-w-md mx-auto p-4 space-y-4">

    <section id="view-find-mason" class="space-y-4">
      
      <div class="bg-white p-4 rounded-xl shadow-sm border border-gray-200 space-y-3">
        <div class="grid grid-cols-2 gap-2">
          <div>
            <label class="block text-[11px] font-bold text-gray-600 mb-1">अपना ज़िला चुनें</label>
            <select id="filter-district" onchange="renderMasons()" class="w-full text-xs font-semibold p-2 bg-gray-50 border border-gray-300 rounded-lg focus:outline-none focus:border-orange-500">
              <option value="सभी">पूरा बिहार (सभी ज़िले)</option>
              <option value="पटना">पटना</option>
              <option value="बक्सर">बक्सर</option>
              <option value="भोजपुर (आरा)">भोजपुर (आरा)</option>
              <option value="रोहतास (सासाराम)">रोहतास (सासाराम)</option>
              <option value="कैमूर (भभुआ)">कैमूर (भभुआ)</option>
              <option value="गया">गया</option>
              <option value="मुजफ्फरपुर">मुजफ्फरपुर</option>
              <option value="भागलपुर">भागलपुर</option>
              <option value="दरभंगा">दरभंगा</option>
              <option value="पूर्णिया">पूर्णिया</option>
              <option value="सारण (छपरा)">सारण (छपरा)</option>
              <option value="सिवान">सिवान</option>
              <option value="गोपालगंज">गोपालगंज</option>
              <option value="वैशाली (हाजीपुर)">वैशाली (हाजीपुर)</option>
              <option value="समस्तीपुर">समस्तीपुर</option>
              <option value="बेगूसराय">बेगूसराय</option>
              <option value="नालंदा (बिहारशरीफ)">नालंदा (बिहारशरीफ)</option>
              <option value="औरंगाबाद">औरंगाबाद</option>
              <option value="नवादा">नवादा</option>
              <option value="जहानाबाद">जहानाबाद</option>
              <option value="अरवल">अरवल</option>
              <option value="पूर्वी चंपारण (मोतिहारी)">पूर्वी चंपारण (मोतिहारी)</option>
              <option value="पश्चिम चंपारण (बेतिया)">पश्चिम चंपारण (बेतिया)</option>
              <option value="सीतामढ़ी">सीतामढ़ी</option>
              <option value="शिवहर">शिवहर</option>
              <option value="मधुबनी">मधुबनी</option>
              <option value="सहरसा">सहरसा</option>
              <option value="मधेपुरा">मधेपुरा</option>
              <option value="सुपौल">सुपौल</option>
              <option value="कटिहार">कटिहार</option>
              <option value="अररिया">अररिया</option>
              <option value="किशनगंज">किशनगंज</option>
              <option value="मुंगेर">मुंगेर</option>
              <option value="जमुई">जमुई</option>
              <option value="खगड़िया">खगड़िया</option>
              <option value="बांका">बांका</option>
              <option value="लखीसराय">लखीसराय</option>
              <option value="शेखपुरा">शेखपुरा</option>
            </select>
          </div>
          <div>
            <label class="block text-[11px] font-bold text-gray-600 mb-1">कारीगर का काम</label>
            <select id="filter-skill" onchange="renderMasons()" class="w-full text-xs font-semibold p-2 bg-gray-50 border border-gray-300 rounded-lg focus:outline-none focus:border-orange-500">
              <option value="सभी">सभी कारीगर & लेबर</option>
              <option value="राजमिस्त्री (चिनाई/जोड़ाई)">राजमिस्त्री (चिनाई)</option>
              <option value="सेंट्रिंग / शटरिंग मिस्त्री">सेंट्रिंग / शटरिंग</option>
              <option value="सरिया / लोहार मिस्त्री">सरिया मिस्त्री</option>
              <option value="लेबर / हेल्पर (मजदूर)">लेबर / हेल्पर</option>
              <option value="प्लास्टर मिस्त्री">प्लास्टर मिस्त्री</option>
              <option value="टाइल्स & मार्बल मिस्त्री">टाइल्स & मार्बल</option>
              <option value="पेंटर & पुट्टी कारीगर">पेंटर कारीगर</option>
              <option value="पीओपी & फॉल सीलिंग मिस्त्री">पीओपी / फॉल सीलिंग</option>
              <option value="कारपेंटर (बढ़ई)">कारपेंटर (बढ़ई)</option>
              <option value="प्लंबर (नल मिस्त्री)">प्लंबर (नल फिटिंग)</option>
              <option value="इलेक्ट्रीशियन (बिजली मिस्त्री)">इलेक्ट्रीशियन</option>
              <option value="वेल्डर & ग्रिल मिस्त्री">वेल्डर / ग्रिल</option>
            </select>
          </div>
        </div>
      </div>

      <div id="mason-list-container" class="space-y-3"></div>
    </section>

    <section id="view-post-job" class="hidden">
      <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
        <h2 class="text-base font-bold text-gray-800 border-b pb-2 mb-4 flex items-center gap-2">
          <span>🏠</span> बिहार में कहीं भी काम पोस्ट करें
        </h2>
        <form onsubmit="handleJobSubmit(event)" class="space-y-3">
          <div>
            <label class="block text-xs font-bold text-gray-700">काम का विवरण *</label>
            <input type="text" id="job-title" required placeholder="जैसे: 4 कमरों का प्लास्टर, छत ढलाई लेबर" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-500 focus:outline-none">
          </div>
          <div class="grid grid-cols-2 gap-2">
            <div>
              <label class="block text-xs font-bold text-gray-700">ज़िला *</label>
              <select id="job-district" class="w-full p-2.5 mt-1 text-xs border border-gray-300 rounded-lg bg-white">
                <option value="पटना">पटना</option>
                <option value="बक्सर">बक्सर</option>
                <option value="भोजपुर (आरा)">भोजपुर (आरा)</option>
                <option value="रोहतास">रोहतास</option>
                <option value="गया">गया</option>
                <option value="मुजफ्फरपुर">मुजफ्फरपुर</option>
                <option value="भागलपुर">भागलपुर</option>
                <option value="अन्य जिला">अन्य जिला</option>
              </select>
            </div>
            <div>
              <label class="block text-xs font-bold text-gray-700">अनुमानित दिहाड़ी या ठेका *</label>
              <input type="text" id="job-budget" required placeholder="उदा. ₹750/दिन या ठेका" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg">
            </div>
          </div>
          <div>
            <label class="block text-xs font-bold text-gray-700">आपका मोबाइल नंबर *</label>
            <input type="tel" id="job-phone" maxlength="10" required placeholder="मिस्त्री आपको सीधा फोन करेंगे" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg">
          </div>
          <button type="submit" class="w-full bg-orange-600 hover:bg-orange-700 text-white font-bold py-3 rounded-lg text-sm transition shadow-md">
            काम पोस्ट करें
          </button>
        </form>
      </div>

      <div class="mt-6">
        <h3 class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-2">हालिया पोस्ट किए गए काम</h3>
        <div id="job-posts-container" class="space-y-2"></div>
      </div>
    </section>

    <section id="view-register-mason" class="hidden">
      <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
        <h2 class="text-base font-bold text-gray-800 border-b pb-2 mb-4 flex items-center gap-2">
          <span>👷</span> पूरे बिहार के मिस्त्री/हेल्पर यहाँ जुड़ें
        </h2>
        <form onsubmit="handleMasonRegister(event)" class="space-y-3">
          <div>
            <label class="block text-xs font-bold text-gray-700">मिस्त्री या हेल्पर का पूरा नाम *</label>
            <input type="text" id="reg-name" required placeholder="अपना नाम लिखें" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-500 focus:outline-none">
          </div>
          
          <div class="grid grid-cols-2 gap-2">
            <div>
              <label class="block text-xs font-bold text-gray-700">आपका हुनर / काम *</label>
              <select id="reg-skill" class="w-full p-2.5 mt-1 text-xs border border-gray-300 rounded-lg bg-white">
                <option value="राजमिस्त्री (चिनाई/जोड़ाई)">राजमिस्त्री (चिनाई)</option>
                <option value="सेंट्रिंग / शटरिंग मिस्त्री">सेंट्रिंग / शटरिंग मिस्त्री</option>
                <option value="सरिया / लोहार मिस्त्री">सरिया मिस्त्री</option>
                <option value="लेबर / हेल्पर (मजदूर)">लेबर / हेल्पर (मजदूर)</option>
                <option value="प्लास्टर मिस्त्री">प्लास्टर मिस्त्री</option>
                <option value="टाइल्स & मार्बल मिस्त्री">टाइल्स & मार्बल मिस्त्री</option>
                <option value="पेंटर & पुट्टी कारीगर">पेंटर & पुट्टी कारीगर</option>
                <option value="पीओपी & फॉल सीलिंग मिस्त्री">पीओपी & फॉल सीलिंग</option>
                <option value="कारपेंटर (बढ़ई)">कारपेंटर (बढ़ई)</option>
                <option value="प्लंबर (नल मिस्त्री)">प्लंबर (नल मिस्त्री)</option>
                <option value="इलेक्ट्रीशियन (बिजली मिस्त्री)">इलेक्ट्रीशियन</option>
                <option value="वेल्डर & ग्रिल मिस्त्री">वेल्डर & ग्रिल मिस्त्री</option>
              </select>
            </div>
            <div>
              <label class="block text-xs font-bold text-gray-700">आपका ज़िला *</label>
              <select id="reg-district" class="w-full p-2.5 mt-1 text-xs border border-gray-300 rounded-lg bg-white">
                <option value="पटना">पटना</option>
                <option value="बक्सर">बक्सर</option>
                <option value="भोजपुर (आरा)">भोजपुर (आरा)</option>
                <option value="रोहतास (सासाराम)">रोहतास (सासाराम)</option>
                <option value="गया">गया</option>
                <option value="मुजफ्फरपुर">मुजफ्फरपुर</option>
                <option value="भागलपुर">भागलपुर</option>
                <option value="दरभंगा">दरभंगा</option>
                <option value="पूर्णिया">पूर्णिया</option>
                <option value="सारण (छपरा)">सारण (छपरा)</option>
                <option value="सिवान">सिवान</option>
                <option value="गोपालगंज">गोपालगंज</option>
                <option value="वैशाली">वैशाली</option>
                <option value="समस्तीपुर">समस्तीपुर</option>
                <option value="बेगूसराय">बेगूसराय</option>
                <option value="नालंदा">नालंदा</option>
                <option value="अन्य जिला">अन्य जिला</option>
              </select>
            </div>
          </div>

          <div class="grid grid-cols-2 gap-2">
            <div>
              <label class="block text-xs font-bold text-gray-700">अनुभव (कितने साल) *</label>
              <input type="text" id="reg-exp" required placeholder="जैसे: 6 साल" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg">
            </div>
            <div>
              <label class="block text-xs font-bold text-gray-700">प्रति दिन रेट (₹) *</label>
              <input type="text" id="reg-rate" required placeholder="उदा. ₹750/दिन या ₹450" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg">
            </div>
          </div>

          <div>
            <label class="block text-xs font-bold text-gray-700">मोबाइल नंबर (कॉल और WhatsApp) *</label>
            <input type="tel" id="reg-phone" maxlength="10" required placeholder="10 अंकों का मोबाइल नंबर" class="w-full p-2.5 mt-1 text-sm border border-gray-300 rounded-lg">
          </div>

          <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-3 rounded-lg text-sm transition shadow-md">
            बिहार भर में काम पाने के लिए जुड़ें
          </button>
        </form>
      </div>
    </section>

  </main>

  <script>
    // डेमो डेटा
    let masons = [
      { id: 1, name: "विकास कुमार शर्मा", district: "पटना", skill: "टाइल्स & मार्बल मिस्त्री", exp: "6 साल", rate: "₹800/दिन", phone: "9876543210" },
      { id: 2, name: "रामसुंदर यादव", district: "बक्सर", skill: "राजमिस्त्री (चिनाई/जोड़ाई)", exp: "10 साल", rate: "₹700/दिन", phone: "9876543211" },
      { id: 3, name: "मुन्ना बढ़ई", district: "भोजपुर (आरा)", skill: "कारपेंटर (बढ़ई)", exp: "7 साल", rate: "₹800/दिन", phone: "9876543212" },
      { id: 4, name: "सोनू कुमार", district: "गया", skill: "लेबर / हेल्पर (मजदूर)", exp: "3 साल", rate: "₹450/दिन", phone: "9876543213" },
      { id: 5, name: "अनिल पासवान", district: "मुजफ्फरपुर", skill: "पेंटर & पुट्टी कारीगर", exp: "5 साल", rate: "₹650/दिन", phone: "9876543214" }
    ];

    let jobs = [
      { id: 1, title: "घर निर्माण के लिए 5 लेबर और 2 राजमिस्त्री चाहिए", district: "पटना", budget: "₹750/दिन", phone: "9123456789" },
      { id: 2, title: "दुकान में टाइल्स और फॉल सीलिंग लगवानी है", district: "बक्सर", budget: "ठेका", phone: "9123456788" }
    ];

    function switchTab(tab) {
      document.getElementById('view-find-mason').classList.add('hidden');
      document.getElementById('view-post-job').classList.add('hidden');
      document.getElementById('view-register-mason').classList.add('hidden');

      document.getElementById('tab-find').className = "flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-transparent text-gray-500";
      document.getElementById('tab-post').className = "flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-transparent text-gray-500";
      document.getElementById('tab-reg').className = "flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-transparent text-gray-500";

      if(tab === 'find-mason') {
        document.getElementById('view-find-mason').classList.remove('hidden');
        document.getElementById('tab-find').className = "flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-orange-600 text-orange-600";
      } else if(tab === 'post-job') {
        document.getElementById('view-post-job').classList.remove('hidden');
        document.getElementById('tab-post').className = "flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-orange-600 text-orange-600";
        renderJobs();
      } else if(tab === 'register-mason') {
        document.getElementById('view-register-mason').classList.remove('hidden');
        document.getElementById('tab-reg').className = "flex-1 py-3 text-xs sm:text-sm font-bold text-center border-b-2 border-orange-600 text-orange-600";
      }
    }

    function renderMasons() {
      const district = document.getElementById('filter-district').value;
      const skill = document.getElementById('filter-skill').value;
      const container = document.getElementById('mason-list-container');

      const filtered = masons.filter(m => {
        const matchDistrict = (district === 'सभी' || m.district === district);
        const matchSkill = (skill === 'सभी' || m.skill === skill);
        return matchDistrict && matchSkill;
      });

      if(filtered.length === 0) {
        container.innerHTML = `<div class="bg-white p-6 rounded-xl text-center text-gray-500 text-sm">इस ज़िले में अभी कारीगर रजिस्टर नहीं हुए हैं। आप सीधे काम पोस्ट कर सकते हैं।</div>`;
        return;
      }

      container.innerHTML = filtered.map(m => `
        <div class="bg-white p-4 rounded-xl border border-gray-200 shadow-sm flex flex-col justify-between space-y-3">
          <div class="flex justify-between items-start">
            <div>
              <h3 class="font-bold text-gray-900 text-base leading-tight">${m.name}</h3>
              <p class="text-xs text-orange-600 font-semibold mt-0.5">📍 ज़िला: ${m.district}</p>
            </div>
            <span class="bg-orange-50 text-orange-700 border border-orange-200 text-xs px-2 py-1 rounded font-bold">
              ${m.rate}
            </span>
          </div>

          <div class="bg-gray-50 p-2.5 rounded-lg text-xs grid grid-cols-2 gap-2 text-gray-600">
            <div>🛠 <b>काम:</b> ${m.skill}</div>
            <div>⭐ <b>अनुभव:</b> ${m.exp}</div>
          </div>

          <div class="grid grid-cols-2 gap-2 pt-1">
            <a href="tel:${m.phone}" class="bg-green-600 hover:bg-green-700 text-white text-center py-2.5 rounded-lg text-xs font-bold flex items-center justify-center gap-1.5 shadow-sm">
              <span>📞</span> कॉल करें
            </a>
            <a href="https://wa.me/91${m.phone}?text=नमस्ते ${m.name} जी, मुझे MistryBabu.com से आपका नंबर मिला। मुझे काम के लिए बात करनी है।" target="_blank" class="bg-emerald-500 hover:bg-emerald-600 text-white text-center py-2.5 rounded-lg text-xs font-bold flex items-center justify-center gap-1.5 shadow-sm">
              <span>💬</span> WhatsApp
            </a>
          </div>
        </div>
      `).join('');
    }

    function renderJobs() {
      const container = document.getElementById('job-posts-container');
      container.innerHTML = jobs.map(j => `
        <div class="bg-gray-50 p-3 rounded-lg border border-gray-200 flex justify-between items-center text-xs">
          <div>
            <p class="font-bold text-gray-800">${j.title}</p>
            <p class="text-gray-500 mt-0.5">📍 ज़िला: ${j.district} | 💰 ${j.budget}</p>
          </div>
          <a href="tel:${j.phone}" class="bg-orange-600 text-white px-3 py-1.5 rounded font-bold">कॉल करें</a>
        </div>
      `).join('');
    }

    function handleJobSubmit(e) {
      e.preventDefault();
      const newJob = {
        id: Date.now(),
        title: document.getElementById('job-title').value,
        district: document.getElementById('job-district').value,
        budget: document.getElementById('job-budget').value,
        phone: document.getElementById('job-phone').value
      };
      jobs.unshift(newJob);
      alert('काम सफलतापूर्वक पोस्ट हो गया है!');
      e.target.reset();
      renderJobs();
    }

    function handleMasonRegister(e) {
      e.preventDefault();
      const newMason = {
        id: Date.now(),
        name: document.getElementById('reg-name').value,
        district: document.getElementById('reg-district').value,
        skill: document.getElementById('reg-skill').value,
        exp: document.getElementById('reg-exp').value,
        rate: document.getElementById('reg-rate').value,
        phone: document.getElementById('reg-phone').value
      };
      masons.unshift(newMason);
      alert('बधाई हो! आपकी प्रोफाइल पूरे बिहार में MistryBabu.com पर जुड़ गई है।');
      e.target.reset();
      switchTab('find-mason');
      renderMasons();
    }

    renderMasons();
  </script>
</body>
</html>
