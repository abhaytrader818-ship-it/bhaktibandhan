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
      --brand:#ff6f00; /* saffron */
      --brand-dark:#b25300;
      --gold:#d4af37;
      --bg:#fff8f0;
      --muted:#6b6b6b;
      --card-shadow:0 10px 30px rgba(16,24,40,0.08);
    }
    *{box-sizing:border-box;}
    body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial; background:var(--bg); color:#222; margin:0;}
    a{color:inherit; text-decoration:none;}
    /* Topbar */
    .topbar{background:linear-gradient(90deg,var(--brand),#ff9a3d); color:white; padding:18px 0; box-shadow:0 6px 30px rgba(0,0,0,0.08);}
    .brand{display:flex;align-items:center;gap:14px}
    .brand-badge{width:68px;height:68px;border-radius:50%;display:flex;align-items:center;justify-content:center;background:radial-gradient(circle,#ffd699,#ff8a00);border:3px solid rgba(212,175,55,0.95);box-shadow:0 10px 30px rgba(255,136,0,0.14)}
    .brand-title{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:var(--gold);margin:0}
    .brand-tag{font-size:13px;color:#fff3d9;margin:0;font-weight:600}

    /* Navbar */
    .navbar-custom{background:#fff;padding:10px 0;box-shadow:0 6px 30px rgba(0,0,0,0.04);}
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
        <img src="https://raw.githubusercontent.com/abhaytrader818-ship-it/bhaktibandhan/main/WhatsApp%20Image%202025-11-23%20at%2020.16.29_9e7ef7ff.jpg" style="width:60px;height:60px;border-radius:50%;">
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
        <svg width="280" height="180" viewBox="0 0 400 260" aria-hidden="true">
          <rect rx="20" width="400" height="260" fill="#fff7ed" />
          <text x="200" y="140" text-anchor="middle" font-size="20" fill="#ff6f00" font-weight="700">Bhakti Bandhan</text>
        </svg>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services" class="section">
  <div class="container">
    <h3 class="mb-3" data-i18n="services_title">Our Services</h3>
    <div class="row services-row g-3">
      <!-- 10 service cards -->
      <!-- Example: repeat for all 10 -->
      <div class="col-md-6 col-lg-4">
        <div class="service-card p-3">
          <div class="service-title" data-i18n="s1">Grih Pravesh Puja</div>
          <div class="service-desc" data-i18n="s1d">Blessings for new homes with full rituals & samagri.</div>
          <div class="mt-2"><button class="btn btn-primary-custom btn-sm" onclick="serviceBook('Grih Pravesh Puja')"><strong data-i18n="book">Book</strong></button></div>
        </div>
      </div>
      <!-- Repeat other 9 cards as in your original code -->
    </div>
  </div>
</section>

<!-- PUROHITS -->
<section id="purohits" class="section">
  <div class="container">
    <div class="d-flex justify-content-between align-items-center mb-3">
      <h3 data-i18n="purohits_title">Verified Purohits (Demo)</h3>
      <div class="muted small">Click a purohit to prefill booking or WhatsApp directly</div>
    </div>
    <div class="row g-4" id="purohitGrid"></div>
  </div>
</section>

<!-- BOOKING -->
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

<!-- DONATE -->
<section id="donate" class="section bg-white">
  <div class="container">
    <h3 class="mb-3" data-i18n="donate_title">Support Bhakti Bandhan</h3>
    <p class="muted mb-3" data-i18n="donate_desc">
      Aap hamare mission ko support kar sakte hain. Har donation se verified purohits aur samagri delivery ka quality maintain hota hai.
    </p>
    
    <div class="row g-3">
      <div class="col-md-6">
        <div class="panchang-card text-center">
          <h5>UPI / Bank Transfer</h5>
          <p>UPI ID: <strong>bhaktibandhan@upi</strong></p>
          <button class="btn btn-gold" onclick="copyUPI()">Copy UPI</button>
        </div>
      </div>
      <div class="col-md-6">
        <div class="panchang-card text-center">
          <h5>Donate via WhatsApp</h5>
          <p>Send your donation confirmation on WhatsApp for receipt</p>
          <button class="btn btn-success" onclick="donateWhatsApp()">WhatsApp Now</button>
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
        <div id="festList" class="mt-3"></div>
      </div>
      <div class="col-lg-6">
        <h4 data-i18n="map_title">Map — Demo Lucknow Location</h4>
        <div class="mt-3 panchang-card">
          <p class="muted">Showing a sample temple / service hub in Lucknow (Demo).</p>
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

<!-- SUPPORT -->
<section id="support" class="section">
  <div class="container">
    <div class="row g-4">
      <div class="col-md-8">
        <h4 data-i18n="support_title">Help & Support</h4>
        <p class="muted">For bookings or urgent help contact our support. Demo phone: <strong>+91 78977 86771</strong></p>
        <div class="d-flex gap-2">
          <a class="btn btn-dark" href="https://wa.me/917897786771" target="_blank">WhatsApp Support</a>
          <a class="btn btn-outline-secondary" href="mailto:support@bhaktibandhan.com">Email</a>
        </div>
      </div>
    </div>
  </div>
</section>

<footer>
  &copy; 2025 Bhakti Bandhan — All rights reserved.
</footer>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

<script>
  const pujas = ["Grih Pravesh Puja","Satyanarayan Katha","Havan / Yagya","Wedding Puja","Festival Pooja","Special Occasion Puja","Navratri Puja","Shanti Puja","Anniversary Puja","Custom Puja"];
  const pujaSelect = document.getElementById('puja');
  pujas.forEach(p => { let opt = document.createElement('option'); opt.value = p; opt.innerText = p; pujaSelect.appendChild(opt); });

  const purohits = [
    {name:"Pandit Anil",rating:4.9,city:"Lucknow",phone:"+917897786771"},
    {name:"Pandit Rajesh",rating:4.7,city:"Kanpur",phone:"+919810000011"},
    {name:"Pandit Suresh",rating:4.8,city:"Varanasi",phone:"+918900000022"}
  ];
  const purohitGrid = document.getElementById('purohitGrid');
  purohits.forEach(p=>{
    let div = document.createElement('div');
    div.className='col-md-4';
    div.innerHTML=`<div class="purohit-card p-3 text-center" onclick="prefillBooking('${p.name}', '${p.phone}')">
      <img src="https://via.placeholder.com/110" class="purohit-avatar mb-2" alt="${p.name}">
      <div class="fw-bold">${p.name}</div>
      <div class="muted small">${p.city}</div>
      <div class="rating-badge mt-1">${p.rating} ⭐</div>
    </div>`;
    purohitGrid.appendChild(div);
  });

  function prefillBooking(name, phone){
    document.getElementById('name').value=name;
    document.getElementById('phone').value=phone;
    alert('Booking form prefilled for '+name);
  }

  function handleBooking(e){
    e.preventDefault();
    const n=document.getElementById('name').value;
    const ph=document.getElementById('phone').value;
    const pj=document.getElementById('puja').value;
    const dt=document.getElementById('datetime').value;
    const kt=document.getElementById('kit').value;
    const msg=`Hi, I want to book ${pj} on ${dt}. Name: ${n} Phone: ${ph} Kit: ${kt}`;
    document.getElementById('sampleMsg').innerText=msg;
    const waLink='https://wa.me/917897786771?text='+encodeURIComponent(msg);
    window.open(waLink,'_blank');
  }

  function openWhatsAppQuick(){
    const msg=document.getElementById('sampleMsg').innerText;
    window.open('https://wa.me/917897786771?text='+encodeURIComponent(msg),'_blank');
  }

  function sendLiveLocation(){
    alert("Live location feature demo only. Open WhatsApp and share manually.");
  }

  function copyUPI(){
    const upi = 'bhaktibandhan@upi';
    navigator.clipboard.writeText(upi).then(()=>{alert('UPI ID copied: '+upi);});
  }

  function donateWhatsApp(){
    const msg=`Hello Bhakti Bandhan Team, I would like to donate to support your mission. Please provide instructions.`;
    const waNumber='919810000011';
    window.open(`https://wa.me/${waNumber}?text=${encodeURIComponent(msg)}`,'_blank');
  }

  // Festival demo list
  const festivals = ["Diwali - 12 Nov 2025","Holi - 28 Mar 2026","Raksha Bandhan - 17 Aug 2025","Navratri - 15 Oct 2025"];
  const festList = document.getElementById('festList');
  festivals.forEach(f=>{
    const div=document.createElement('div');
    div.className='festival-item';
    div.innerText=f;
    festList.appendChild(div);
  });
</script>

</body>
</html>
