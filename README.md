<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Bhakti Bandhan — Connecting Faith Digitally</title>

  <!-- Bootstrap CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

  <style>
    :root{
      --brand:#ff6f00;      /* saffron */
      --brand-dark:#b25300;
      --gold:#d4af37;
      --bg:#fff8f0;
      --muted:#6b6b6b;
      --card-shadow: 0 10px 30px rgba(16,24,40,0.08);
    }
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial; background:var(--bg); color:#222; margin:0;}
    a{color:inherit}
    /* Header */
    .topbar{background:linear-gradient(90deg,var(--brand),#ff9a3d); color:white;padding:18px 0;box-shadow:0 6px 30px rgba(0,0,0,0.08);}
    .brand{display:flex;align-items:center;gap:14px}
    .brand-badge{width:68px;height:68px;border-radius:50%;display:flex;align-items:center;justify-content:center;background:radial-gradient(circle,#ffd699,#ff8a00);border:3px solid rgba(212,175,55,0.95);box-shadow:0 10px 30px rgba(255,136,0,0.14)}
    .brand-title{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:var(--gold);margin:0}
    .brand-tag{font-size:13px;color:#fff3d9;margin:0;font-weight:600}

    /* Navbar */
    .navbar-custom{background:#fff;padding:10px 0;box-shadow:0 6px 30px rgba(0,0,0,0.04)}
    .nav-link { color: #444 !important; font-weight:600; }
    .btn-primary-custom{background:var(--brand);border-color:var(--brand);color:white}
    .btn-gold{background:var(--gold);color:#3a2b00;border:none}

    /* Hero */
    .hero{padding:36px 0;text-align:left}
    .hero h1{font-size:36px;margin:0 0 8px;color:var(--brand-dark);font-family:'Playfair Display',serif}
    .hero p{color:var(--muted);margin:0 0 14px}

    /* Services row */
    .services-row .service-card{
      background:linear-gradient(180deg,#fff,#fff6ed);
      border-radius:12px;padding:18px;box-shadow:var(--card-shadow);border-left:6px solid rgba(212,175,55,0.12);
    }
    .service-title{font-weight:800;color:var(--gold);font-size:18px}
    .service-desc{color:var(--muted);font-size:14px}

    /* Purohit card */
    .purohit-card{border-radius:12px;overflow:hidden;box-shadow:var(--card-shadow);border:1px solid rgba(0,0,0,0.03)}
    .purohit-avatar{width:110px;height:110px;border-radius:12px;object-fit:cover;border:4px solid #fff;box-shadow:0 8px 20px rgba(0,0,0,0.08)}
    .rating-badge{background:linear-gradient(90deg,#fff7ea,#fff0db);padding:6px 10px;border-radius:20px;font-weight:700;color:#3a3a3a}

    /* Panchang/festivals */
    .panchang-card{background:#fff3e0;border-radius:12px;padding:14px;border-left:6px solid var(--brand-dark);box-shadow:var(--card-shadow)}
    .festival-item{background:linear-gradient(90deg,#fff8f0,#fff4e6);padding:10px;border-radius:8px;margin-bottom:8px}

    /* small */
    .muted{color:var(--muted)}
    pre.sample{background:#fff7ed;padding:12px;border-radius:8px;white-space:pre-wrap}
    footer{background:#1e1e1e;color:#ddd;padding:18px 0;text-align:center;margin-top:30px}

    /* responsive tweaks */
    @media(max-width:768px){
      .brand-title{font-size:18px}
      .hero h1{font-size:28px}
      .purohit-avatar{width:84px;height:84px}
    }
  </style>
</head>
<body>

<!-- TOP BAR -->
<div class="topbar">
  <div class="container d-flex justify-content-between align-items-center">
    <div class="brand">
      <div class="brand-badge" aria-hidden="true">
        <!-- simple trishul SVG -->
        <svg width="36" height="36" viewBox="0 0 200 200"><defs><linearGradient id="g1" x1="0" x2="1"><stop offset="0" stop-color="#ffd699"/><stop offset="1" stop-color="#ff6f00"/></linearGradient></defs><circle cx="100" cy="100" r="98" fill="url(#g1)"/><g fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="7"><path d="M100 40 C86 60,70 88,70 110 C70 128,86 140,100 140 C114 140,130 128,130 110 C130 88,114 60,100 40 Z"/><rect x="93" y="140" width="14" height="40" rx="5" fill="#fff"/><circle cx="100" cy="86" r="7" fill="#111" stroke="#fff" stroke-width="4"/></g></svg>
      </div>
      <div>
        <p class="brand-title mb-0">Bhakti Bandhan</p>
        <p class="brand-tag mb-0">Connecting Faith Digitally</p>
      </div>
    </div>

    <div class="d-flex align-items-center gap-2">
      <div class="me-2">
        <button class="btn btn-light btn-sm" id="lang-en">English</button>
        <button class="btn btn-warning btn-sm" id="lang-hi">हिंदी</button>
      </div>
      <div>
        <a href="#booking" class="btn btn-primary-custom btn-sm">Book Now</a>
      </div>
    </div>
  </div>
</div>

<!-- NAV -->
<nav class="navbar navbar-expand-lg navbar-custom">
  <div class="container">
    <a class="navbar-brand fw-bold text-dark" href="#">Bhakti Bandhan</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navMenu">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navMenu">
      <ul class="navbar-nav ms-auto align-items-lg-center">
        <li class="nav-item"><a class="nav-link" href="#services" data-i18n="nav_services">Services</a></li>
        <li class="nav-item"><a class="nav-link" href="#purohits" data-i18n="nav_purohits">Purohits</a></li>
        <li class="nav-item"><a class="nav-link" href="#panchang" data-i18n="nav_panchang">Panchang</a></li>
        <li class="nav-item"><a class="nav-link" href="#festivals" data-i18n="nav_festivals">Festivals</a></li>
        <li class="nav-item"><a class="nav-link" href="#donate" data-i18n="nav_donate">Donate</a></li>
        <li class="nav-item"><a class="nav-link" href="#support" data-i18n="nav_support">Help</a></li>
      </ul>
    </div>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-lg-7">
        <h1 id="hero_title">Book a Purohit in 3 clicks — Puja at home made simple</h1>
        <p id="hero_sub" class="muted">Havans, Satyanarayan Katha, Grih Pravesh, festival pujas — verified purohits, clear pricing, samagri delivery.</p>
        <div class="d-flex gap-2 hero-actions">
          <a class="btn btn-gold btn-lg" href="#booking" data-i18n="hero_book">Book a Puja</a>
          <a class="btn btn-outline-dark btn-lg" href="#purohits" data-i18n="hero_explore">Explore Purohits</a>
        </div>
      </div>
      <div class="col-lg-5 text-center">
        <!-- visual -->
        <svg width="280" height="180" viewBox="0 0 400 260" aria-hidden="true">
          <rect rx="20" width="400" height="260" fill="#fff7ed" />
          <text x="200" y="140" text-anchor="middle" font-size="20" fill="#ff6f00" font-weight="700">Bhakti Bandhan</text>
        </svg>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES (row-wise, 10 services) -->
<section id="services" class="section">
  <div class="container">
    <h3 class="mb-3" data-i18n="services_title">Our Services</h3>
    <div class="row services-row g-3">
      <!-- 10 service cards -->
      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s1">Grih Pravesh Puja</div>
          <div class="service-desc" data-i18n="s1d">Blessings for new homes with full rituals & samagri.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Grih Pravesh Puja')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s2">Satyanarayan Katha</div>
          <div class="service-desc" data-i18n="s2d">Katha and puja for prosperity & harmony.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Satyanarayan Katha')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s3">Rudrabhishek</div>
          <div class="service-desc" data-i18n="s3d">Special Rudra abhishek for blessings & health.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Rudrabhishek')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s4">Mahamrityunjay Jaap</div>
          <div class="service-desc" data-i18n="s4d">Powerful mantra jaap for healing & protection.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Mahamrityunjay Jaap')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s5">Navgrah Shanti Puja</div>
          <div class="service-desc" data-i18n="s5d">Remedial puja to appease Navagrahas.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Navgrah Shanti Puja')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s6">Lakshmi & Ganesh Puja</div>
          <div class="service-desc" data-i18n="s6d">Festive puja for wealth & auspicious beginnings.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Lakshmi & Ganesh Puja')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s7">Havan (All types)</div>
          <div class="service-desc" data-i18n="s7d">Vastu havan, homam, yagya — customized for purpose.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Havan')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s8">Marriage Puja</div>
          <div class="service-desc" data-i18n="s8d">Vedic marriage ceremonies & muhurat guidance.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Marriage Puja')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s9">Kundali & Vastu</div>
          <div class="service-desc" data-i18n="s9d">Astrology & Vastu consultation for life decisions.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Kundali & Vastu Consultation')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s10">Pitru Shanti Puja</div>
          <div class="service-desc" data-i18n="s10d">Pujas for ancestors & peace in family lineage.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Pitru Shanti Puja')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- PUROHITS (10 demo with dummy WhatsApp & ratings) -->
<section id="purohits" class="section">
  <div class="container">
    <div class="d-flex justify-content-between align-items-center mb-3">
      <h3 data-i18n="purohits_title">Verified Purohits (Demo)</h3>
      <div class="muted small">Click a purohit to prefill booking or WhatsApp directly</div>
    </div>

    <div class="row g-4" id="purohitGrid">
      <!-- JS will inject cards -->
    </div>
  </div>
</section>

<!-- BOOKING & HELP -->
<section id="booking" class="section bg-white">
  <div class="container">
    <div class="row g-4">
      <div class="col-lg-6">
        <h4 data-i18n="booking_title">Quick Booking (WhatsApp)</h4>
        <form id="bookingForm" onsubmit="handleBooking(event)" class="mt-3">
          <div class="mb-2">
            <label class="form-label" data-i18n="label_name">Your Name</label>
            <input id="name" class="form-control" required>
          </div>
          <div class="mb-2">
            <label class="form-label" data-i18n="label_phone">Phone</label>
            <input id="phone" class="form-control" placeholder="7897786771" required>
          </div>
          <div class="mb-2">
            <label class="form-label" data-i18n="label_puja">Select Puja</label>
            <select id="puja" class="form-select"></select>
          </div>
          <div class="mb-2">
            <label class="form-label" data-i18n="label_datetime">Date & Time</label>
            <input id="datetime" type="datetime-local" class="form-control" required>
          </div>
          <div class="mb-2">
            <label class="form-label" data-i18n="label_kit">Puja Samagri Kit</label>
            <select id="kit" class="form-select">
              <option value="none">No, I will arrange</option>
              <option value="basic">Basic Kit (₹399)</option>
              <option value="standard">Standard Kit (₹699)</option>
              <option value="premium">Premium Kit (₹1299)</option>
            </select>
          </div>
          <button class="btn btn-gold" type="submit" data-i18n="send_whatsapp">Send to WhatsApp</button>
        </form>
      </div>

      <div class="col-lg-6">
        <h5 data-i18n="sample_msg">Sample message</h5>
        <pre class="sample" id="sampleMsg">Hi, I want to book Havan on 2025-11-24 09:00.
Name: Anil Kumar
Phone: +91 7897786771
Kit: Standard Kit
Please confirm availability and fees.</pre>

        <div class="mt-3 d-flex gap-2">
          <button class="btn btn-outline-secondary" onclick="openWhatsAppQuick()" data-i18n="open_wa">Open WhatsApp</button>
          <button class="btn btn-outline-info" onclick="sendLiveLocation()" data-i18n="share_loc">Share Live Location</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PANCHANG + FESTIVALS -->
<section id="panchang" class="section">
  <div class="container">
    <div class="row g-4">
      <div class="col-lg-6">
        <h4 data-i18n="panchang_title">Hindu Panchang (Key Festivals 2025–26)</h4>
        <div id="festList" class="mt-3">
          <!-- festival cards injected by JS -->
        </div>
      </div>
      <div class="col-lg-6">
        <h4 data-i18n="map_title">Map — Dummy Lucknow Location</h4>
        <div class="mt-3 panchang-card">
          <p class="muted">Showing a sample temple / service hub in Lucknow (Demo).</p>
          <!-- Google Maps embed (Lucknow coords) -->
          <div style="width:100%;height:300px;border-radius:8px;overflow:hidden">
            <iframe width="100%" height="100%" loading="lazy" style="border:0" referrerpolicy="no-referrer-when-downgrade"
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3557.988248231767!2d80.93004161501202!3d26.846693583155058!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x399bfd9ff3c6a2ab%3A0x1b0f6f2f3c0e13f5!2sAminabad%2C%20Lucknow%2C%20Uttar%20Pradesh%2C%20India!5e0!3m2!1sen!2sin!4v1700000000000!5m2!1sen!2sin">
            </iframe>
          </div>
          <div class="mt-2 d-flex gap-2">
            <a target="_blank" rel="noopener" class="btn btn-outline-primary" href="https://www.google.com/maps/dir/?api=1&destination=26.846694,80.946166" data-i18n="get_directions">Get Directions</a>
            <button class="btn btn-outline-secondary" onclick="openWhatsAppQuick()" data-i18n="need_help">Need Help?</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DONATE -->
<section id="donate" class="section bg-white">
  <div class="container text-center">
    <h4 data-i18n="donate_title">Support & Donate Us</h4>
    <p class="muted" data-i18n="donate_desc">Your donation helps us grow and support verified purohits across India.</p>
    <div class="d-flex justify-content-center gap-3">
      <a class="btn btn-success" href="#" onclick="alert('UPI link placeholder — replace with your UPI/Payment link')">Donate via UPI</a>
      <a class="btn btn-outline-dark" href="#" onclick="alert('Payment gateway placeholder — integrate as needed')">Donate (Card)</a>
    </div>
  </div>
</section>

<!-- SUPPORT & FOOTER -->
<section id="support" class="section">
  <div class="container">
    <div class="row g-4">
      <div class="col-md-8">
        <h4 data-i18n="support_title">Help & Support</h4>
        <p class="muted">For bookings or urgent help contact our support. Demo phone: <strong>+91 78977 86771</strong></p>
        <div class="d-flex gap-2">
          <a class="btn btn-dark" href="https://wa.me/917897786771" target="_blank">WhatsApp Support</a>
          <a class="btn btn-outline-secondary" href="mailto:hello@bhaktibandhan.example">Email Support</a>
        </div>
      </div>
      <div class="col-md-4 text-end">
        <p class="muted">Made with ❤ by</p>
        <h5>HIMANSHU KUMAR</h5>
      </div>
    </div>
  </div>
</section>

<footer>
  © 2025 Bhakti Bandhan • Connecting Faith Digitally
</footer>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

<script>
/* -------------------------
   Data: services (for dropdown)
   ------------------------- */
const servicesList = [
  'Grih Pravesh Puja',
  'Satyanarayan Katha',
  'Rudrabhishek',
  'Mahamrityunjay Jaap',
  'Navgrah Shanti Puja',
  'Lakshmi & Ganesh Puja',
  'Havan (All types)',
  'Marriage Puja',
  'Kundali & Vastu Consultation',
  'Pitru Shanti Puja'
];

/* populate puja select */
const pujaSelect = document.getElementById('puja');
servicesList.forEach(s => {
  const opt = document.createElement('option');
  opt.value = s; opt.textContent = s; pujaSelect.appendChild(opt);
});

/* -------------------------
   Demo purohits data
   ------------------------- */
const demoPurohits = [
  {id:1,name:'Acharya Raghav Sharma', lang:['Hindi','Sanskrit'], exp:18, rating:4.9, whatsapp:'919810000001', reviews:['Very professional and punctual.','Clear chanting and guidance.']},
  {id:2,name:'Pandit Mohan Trivedi', lang:['Hindi'], exp:14, rating:4.8, whatsapp:'919810000002', reviews:['Good explanation of mantras.']},
  {id:3,name:'Acharya Dinesh Joshi', lang:['Sanskrit','Hindi'], exp:16, rating:4.85, whatsapp:'919810000003', reviews:['Calm voice, excellent puja.']},
  {id:4,name:'Pandit Suresh Mishra', lang:['Hindi'], exp:10, rating:4.6, whatsapp:'919810000004', reviews:['Helpful and humble.']},
  {id:5,name:'Acharya Harish Tiwari', lang:['Hindi','Sanskrit'], exp:22, rating:4.95, whatsapp:'919810000005', reviews:['Masterful and precise.']},
  {id:6,name:'Pandit Rajeev Shastri', lang:['Hindi'], exp:12, rating:4.7, whatsapp:'919810000006', reviews:['Good service, clear communication.']},
  {id:7,name:'Acharya Vivek Pathak', lang:['Hindi','Sanskrit'], exp:15, rating:4.8, whatsapp:'919810000007', reviews:['Very learned and gentle.']},
  {id:8,name:'Pandit Shyam Prasad', lang:['Hindi'], exp:9, rating:4.5, whatsapp:'919810000008', reviews:['Friendly and punctual.']},
  {id:9,name:'Acharya Kunal Bhardwaj', lang:['Hindi','Sanskrit'], exp:13, rating:4.75, whatsapp:'919810000009', reviews:['Excellent chants and knowledge.']},
  {id:10,name:'Pandit Ramesh Purohit', lang:['Hindi'], exp:11, rating:4.6, whatsapp:'919810000010', reviews:['Good guidance and devotion.']}
];

/* render purohits */
function renderPurohits(){
  const grid = document.getElementById('purohitGrid');
  grid.innerHTML = '';
  demoPurohits.forEach(p => {
    const col = document.createElement('div'); col.className = 'col-md-6 col-lg-4';
    col.innerHTML = `
      <div class="purohit-card p-3">
        <div class="d-flex gap-3">
          <img class="purohit-avatar" src="${avatarFor(p.name)}" alt="${p.name}">
          <div style="flex:1">
            <h5 style="margin:0">${p.name}</h5>
            <div class="muted small">${p.lang.join(', ')} • ${p.exp}+ yrs</div>
            <div style="margin-top:8px"><strong>Services:</strong> Havan, Satyanarayan Katha, Grih Pravesh</div>
            <div class="d-flex justify-content-between align-items-center mt-3">
              <div class="rating-badge">⭐ ${p.rating}</div>
              <div>
                <button class="btn btn-sm btn-outline-primary" onclick="prefillBooking('${p.name}','Havan','${p.whatsapp}')">Prefill Booking</button>
                <button class="btn btn-sm btn-success" onclick="openPurohitWhatsApp('${p.whatsapp}','${p.name}')">WhatsApp</button>
                <button class="btn btn-sm btn-outline-secondary" onclick="showReviews(${p.id})">Reviews</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    `;
    grid.appendChild(col);
  });
}
renderPurohits();

/* simple avatar generator (svg dataURL) */
function avatarFor(name){
  const initials = name.split(' ').slice(0,2).map(s=>s[0]).join('').toUpperCase();
  const colors = ['#FFD699','#FFC18D','#FFB66B','#FF9E3B','#FFC34D','#FFAA33'];
  const bg = colors[(name.charCodeAt(0)+name.length) % colors.length];
  const svg = <svg xmlns='http://www.w3.org/2000/svg' width='220' height='220'><rect rx='18' width='100%' height='100%' fill='${bg}'/><text x='50%' y='52%' dominant-baseline='middle' text-anchor='middle' font-size='64' font-family='Segoe UI, Roboto, Arial' fill='#5a3710' font-weight='700'>${initials}</text></svg>;
  return 'data:image/svg+xml;utf8,' + encodeURIComponent(svg);
}

/* reviews modal simple */
function showReviews(id){
  const p = demoPurohits.find(x=>x.id===id);
  const content = p.reviews.map(r=><li>${r}</li>).join('');
  alert(Reviews for ${p.name}:\n\n + p.reviews.join('\n\n'));
}

/* open whatsapp for purohit */
function openPurohitWhatsApp(num,name){
  const msg = Hello ${name}, I would like to book a puja. Please confirm availability.;
  window.open(https://wa.me/${num}?text=+encodeURIComponent(msg),'_blank');
}

/* prefill booking */
function prefillBooking(name,puja,whatsapp){
  document.getElementById('puja').value = puja;
  document.getElementById('name').value = '';
  document.getElementById('phone').value = '';
  document.getElementById('datetime').value = '';
  document.getElementById('sampleMsg').innerText = Hi, I want to book *${puja}* with *${name}*.\nName: *Your Name*\nPhone: *+91 7897786771*\nKit: *Standard Kit*\nPlease confirm availability and fees.;
  location.hash = '#booking';
}

/* serviceBook quick from service card */
function serviceBook(svc){
  document.getElementById('puja').value = svc;
  location.hash = '#booking';
}

/* Booking handler */
const platformNumber = '917897786771'; // platform/support
function handleBooking(e){
  e.preventDefault();
  const name = document.getElementById('name').value.trim();
  const phone = document.getElementById('phone').value.trim();
  const puja = document.getElementById('puja').value;
  const datetime = document.getElementById('datetime').value.replace('T',' ');
  const kit = document.getElementById('kit').value;
  if(!name || !phone || !datetime){
    alert('Please fill name, phone and date/time.');
    return;
  }
  const message = Hi, I want to book *${puja}* on *${datetime}*.\nName: *${name}*\nPhone: *${phone}*\nKit: *${kit}*\nPlease confirm availability and fees.;
  window.open(https://wa.me/${platformNumber}?text= + encodeURIComponent(message),'_blank');
}

/* quick open support whatsapp */
function openWhatsAppQuick(){
  const msg = 'Hello Bhakti Bandhan, I need help with a booking.';
  window.open(https://wa.me/${platformNumber}?text= + encodeURIComponent(msg),'_blank');
}

/* live location */
function sendLiveLocation(){
  if(!navigator.geolocation){ alert('Geolocation not supported.'); return; }
  navigator.geolocation.getCurrentPosition(pos=>{
    const lat = pos.coords.latitude.toFixed(6);
    const lon = pos.coords.longitude.toFixed(6);
    const url = https://www.google.com/maps/search/?api=1&query=${lat},${lon};
    window.open(url,'_blank');
  }, err=>{
    alert('Allow location or try again.');
  });
}

/* festivals list (2025-26) */
const festivals = [
  {name:'Makar Sankranti / Pongal', date:'14 Jan 2025'},
  {name:'Vasant Panchami', date:'02 Feb 2025'},
  {name:'Maha Shivaratri', date:'26 Feb 2025'},
  {name:'Holi (Holika Dahan)', date:'13 Mar 2025'},
  {name:'Holi (Rang)', date:'14 Mar 2025'},
  {name:'Rama Navami', date:'06 Apr 2025'},
  {name:'Hanuman Jayanti', date:'12 Apr 2025'},
  {name:'Akshaya Tritiya', date:'30 Apr 2025'},
  {name:'Raksha Bandhan', date:'02 Aug 2025'},
  {name:'Janmashtami', date:'27 Aug 2025'},
  {name:'Ganesh Chaturthi', date:'04 Sep 2025'},
  {name:'Navratri Begins', date:'01 Oct 2025'},
  {name:'Dussehra', date:'10 Oct 2025'},
  {name:'Dhanteras', date:'18 Oct 2025'},
  {name:'Diwali', date:'20 Oct 2025'},
  {name:'Bhai Dooj', date:'23 Oct 2025'},
  {name:'Holi 2026', date:'04 Mar 2026'}
];

function renderFestivals(){
  const container = document.getElementById('festList');
  container.innerHTML = '';
  festivals.forEach(f=>{
    const div = document.createElement('div'); div.className='festival-item p-2 mb-2';
    div.innerHTML = <strong>${f.name}</strong><div class="muted small">${f.date}</div>;
    container.appendChild(div);
  });
}
renderFestivals();

/* -------------------------
   Multi-language support (simple)
   ------------------------- */
const i18n = {
  english:{
    nav_services:'Services',
    nav_purohits:'Purohits',
    nav_panchang:'Panchang',
    nav_festivals:'Festivals',
    nav_donate:'Donate',
    nav_support:'Help',
    hero_book:'Book a Puja',
    hero_explore:'Explore Purohits',
    services_title:'Our Services',
    booking_title:'Quick Booking (WhatsApp)',
    label_name:'Your Name',
    label_phone:'Phone',
    label_puja:'Select Puja',
    label_datetime:'Date & Time',
    label_kit:'Puja Samagri Kit',
    send_whatsapp:'Send to WhatsApp',
    sample_msg:'Sample message',
    open_wa:'Open WhatsApp',
    share_loc:'Share Live Location',
    panchang_title:'Hindu Panchang (Key Festivals 2025–26)',
    map_title:'Map — Demo Lucknow Location',
    get_directions:'Get Directions',
    need_help:'Need Help?',
    donate_title:'Support & Donate Us',
    donate_desc:'Your donation helps us grow and support verified purohits across India.',
    support_title:'Help & Support',
    services_list: servicesList
  },
  hindi:{
    nav_services:'सेवाएँ',
    nav_purohits:'पुजारी',
    nav_panchang:'पंचांग',
    nav_festivals:'त्योहार',
    nav_donate:'दान करें',
    nav_support:'सहायता',
    hero_book:'पूजा बुक करें',
    hero_explore:'पुजारियों को देखें',
    services_title:'हमारी सेवाएँ',
    booking_title:'त्वरित बुकिंग (WhatsApp)',
    label_name:'आपका नाम',
    label_phone:'फोन',
    label_puja:'पुजा चुनें',
    label_datetime:'तारीख और समय',
    label_kit:'पुजा सामग्री किट',
    send_whatsapp:'WhatsApp भेजें',
    sample_msg:'नमूना संदेश',
    open_wa:'WhatsApp खोलें',
    share_loc:'लाइव लोकेशन भेजें',
    panchang_title:'हिंदू पंचांग (2025–26 के मुख्य त्योहार)',
    map_title:'नक्शा — लखनऊ स्थान (डेमो)',
    get_directions:'दिशा प्राप्त करें',
    need_help:'मदद चाहिए?',
    donate_title:'समर्थन और दान',
    donate_desc:'आपका दान हमें और परिवारों तक पहुँचने में मदद करता है।',
    support_title:'हेल्प और सपोर्ट',
    services_list: ['गृह प्रवेश पूजा','सत्यनारायण कथा','रुद्राभिषेक','महामृत्युंजय जाप','नवग्रह शांति पूजा','लक्ष्मी व गणेश पूजा','हवन (सभी प्रकार)','विवाह पूजा','कुंडली व वास्तु','पितृ शांति पूजा']
  }
};

function translateTo(lang){
  const map = i18n[lang] || i18n.english;
  document.querySelectorAll('[data-i18n]').forEach(el=>{
    const key = el.getAttribute('data-i18n');
    if(map[key]) el.textContent = map[key];
  });
  // update static headings
  document.getElementById('hero_title').textContent = lang==='hindi' ? '3 क्लिक में पुजारी बुक करें — घर पर पूजा सरल' : 'Book a Purohit in 3 clicks — Puja at home made simple';
  document.getElementById('hero_sub').textContent = lang==='hindi'
    ? 'हवन, सत्यनारायण कथा, गृह प्रवेश — सत्यापित पुजारी, स्पष्ट कीमतें, सामग्री डिलीवरी।'
    : 'Havans, Satyanarayan Katha, Grih Pravesh, festival pujas — verified purohits, clear pricing, samagri delivery.';
  // update services text content using provided arrays where needed
  // update service card titles/descriptions for Hindi
  if(lang==='hindi'){
    const s = i18n.hindi.services_list;
    const descs = ['नए घर के लिए पूर्ण अनुष्ठान और सामग्री','समृद्धि के लिए कथा और पूजा','रुद्राभिषेक विधि','आरोग्य व सुरक्षा के लिए जाप','नवग्रह शांति अनुष्ठान','समृद्धि और शुभ आरम्भ','विभिन्न प्रकार के हवन','वैदिक विवाह विधियां','कुंडली व वास्तु सलाह','पितरों की शांति के लिए पूजा'];
    document.querySelectorAll('.service-title').forEach((el,i)=>el.textContent = s[i]);
    document.querySelectorAll('.service-desc').forEach((el,i)=>el.textContent = descs[i]);
  } else {
    // English default is already in HTML — keep it
    // but ensure service titles come from servicesList in english if needed
  }
}

// language buttons
document.getElementById('lang-en').addEventListener('click',()=>translateTo('english'));
document.getElementById('lang-hi').addEventListener('click',()=>translateTo('hindi'));

/* initialize English default */
translateTo('english');

</script>
</body>
</html>
