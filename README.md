<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PrimeGrade Solutions | Excellence, Integrity, Precision</title>
    <style>
        :root {
            --primary: #0f172a; /* Corporate Navy */
            --secondary: #334155; /* Slate Grey */
            --gold: #fbbf24;    /* Bright Gold */
            --light: #f8fafc;   /* Off-White Background */
        }
        body { font-family: 'Segoe UI', sans-serif; margin: 0; padding: 0; background-color: var(--light); color: #333; line-height: 1.6; }
        a { text-decoration: none; color: inherit; }
        
        /* HEADER */
        .header { 
            background: linear-gradient(135deg, var(--primary), #1e293b); 
            color: white; 
            padding: 40px 20px 40px 20px; 
            text-align: center; 
            border-bottom: 5px solid var(--gold);
        }
        .logo-img { 
            width: 90px; height: 90px; 
            background-color: white; 
            border-radius: 50%; 
            padding: 5px; 
            object-fit: contain; 
            border: 3px solid var(--gold); 
            margin-bottom: 10px;
            box-shadow: 0 0 20px rgba(251, 191, 36, 0.5);
        }
        .brand { font-size: 30px; font-weight: 800; letter-spacing: 1px; margin: 5px 0; }
        .sub-headline { color: #cbd5e1; font-size: 15px; margin-top: 5px; margin-bottom: 20px; font-weight: 400; }
        
        /* NEW: HEADER BUTTON */
        .header-btn {
            background-color: var(--gold);
            color: var(--primary);
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: bold;
            font-size: 16px;
            display: inline-block;
            box-shadow: 0 4px 15px rgba(251, 191, 36, 0.4);
            transition: transform 0.2s;
        }
        .header-btn:active { transform: scale(0.95); }

        /* CONTAINER */
        .container { max-width: 800px; margin: -25px auto 40px auto; padding: 20px; }

        /* CARDS */
        .card {
            background: white;
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 10px 30px -5px rgba(0, 0, 0, 0.1);
            margin-bottom: 25px;
        }

        h2 { color: var(--primary); border-left: 6px solid var(--gold); padding-left: 15px; margin-top: 0; }
        h3 { color: var(--secondary); margin-top: 0; font-size: 18px; }

        /* PORTFOLIO SCROLL */
        .portfolio-scroll {
            display: flex; overflow-x: auto; gap: 15px; padding-bottom: 10px; scrollbar-width: none;
        }
        .portfolio-item {
            min-width: 130px; background: #f1f5f9; border-radius: 12px; padding: 15px;
            text-align: center; border: 1px solid #e2e8f0;
        }
        .file-icon { font-size: 28px; margin-bottom: 5px; display: block; }
        .file-name { font-size: 12px; font-weight: bold; color: var(--secondary); }

        /* HOW IT WORKS STEPS */
        .step-container { display: flex; justify-content: space-around; margin-top: 20px; text-align: center; }
        .step-box { flex: 1; margin: 5px; }
        .step-num { 
            width: 40px; height: 40px; line-height: 40px; border-radius: 50%; 
            margin: 0 auto 10px auto; font-weight: bold; font-size: 18px;
        }
        .step-title { font-weight: bold; font-size: 14px; margin-bottom: 5px; color: var(--primary); }
        .step-desc { font-size: 12px; color: #64748b; }

        /* FORM */
        .form-group { margin-bottom: 20px; }
        label { display: block; font-weight: 700; margin-bottom: 8px; color: var(--secondary); }
        select, input { 
            width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 12px; 
            font-size: 16px; background: #f8fafc; box-sizing: border-box; 
        }
        select:focus, input:focus { border-color: var(--gold); background: white; outline: none; }

        /* SUBJECT PILLS (Moved Down) */
        .tags-container { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 10px; }
        .tag {
            background: #e0f2fe; color: var(--primary); padding: 5px 12px;
            border-radius: 20px; font-size: 12px; font-weight: bold; border: 1px solid #bae6fd; cursor: pointer;
        }

        /* WHATSAPP BUTTON */
        .wa-btn {
            background: linear-gradient(to right, #16a34a, #22c55e);
            color: white; width: 100%; padding: 18px; border: none; border-radius: 12px; 
            font-size: 18px; font-weight: bold; cursor: pointer; 
            display: flex; align-items: center; justify-content: center;
            box-shadow: 0 8px 20px -5px rgba(34, 197, 94, 0.4);
        }

        /* TESTIMONIALS GRID */
        .testimonial-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        @media (max-width: 600px) { .testimonial-grid { grid-template-columns: 1fr; } }
        
        .review-box {
            background: #f1f5f9; /* Darker grey for contrast */
            padding: 15px; border-radius: 12px; border-left: 4px solid var(--gold); font-size: 14px;
        }
        .stars { color: var(--gold); margin-bottom: 5px; font-size: 16px; }

        /* FAQ COLLAPSIBLE */
        details { border-bottom: 1px solid #e2e8f0; padding: 15px 0; }
        summary { font-weight: bold; color: var(--primary); cursor: pointer; list-style: none; display: flex; justify-content: space-between; }
        summary::after { content: "+"; color: var(--gold); font-weight: bold; }
        details[open] summary::after { content: "-"; }
        .faq-answer { margin-top: 10px; font-size: 14px; color: #64748b; }

        /* PAYMENT ROW (Fixed Alignment) */
        .payment-row { 
            display: flex; justify-content: center; align-items: center; 
            gap: 10px; margin-top: 10px; flex-wrap: wrap; 
        }
        .pay-icon { height: 35px; width: auto; border-radius: 4px; border: 1px solid #e2e8f0; padding: 2px; background: white; }
        .zamtel-badge {
            height: 35px; /* Matches images exactly */
            padding: 0 10px; background: #009639; color: white; 
            font-weight: bold; font-size: 11px; display: flex; 
            align-items: center; justify-content: center; border-radius: 4px;
        }

        /* FOOTER */
        .footer { text-align: center; color: #64748b; padding-bottom: 30px; font-size: 13px; margin-top: 40px; }
        .footer-links { margin-bottom: 15px; font-weight: bold; color: var(--primary); }
        .disclaimer { font-size: 12px; color: #94a3b8; margin-top: 10px; opacity: 1; } /* Increased visibility */
    </style>
</head>
<body>

    <div class="header">
        <img src="https://cdn-icons-png.flaticon.com/512/3135/3135810.png" alt="Logo" class="logo-img">
        <div class="brand">PRIMEGRADE SOLUTIONS</div>
        <div class="sub-headline">Zambia's Leading Engineering & Academic Consultancy</div>
        <a href="#order-form" class="header-btn">Get a Quote Now ➤</a>
    </div>

    <div class="container">
        
        <div class="card">
            <h3>📂 Recent Projects</h3>
            <div class="portfolio-scroll">
                <div class="portfolio-item"><span class="file-icon">⚡</span><div class="file-name">Circuit Analysis<br>(Distinction)</div></div>
                <div class="portfolio-item"><span class="file-icon">🏗️</span><div class="file-name">Fluid Mechanics<br>Calculation</div></div>
                <div class="portfolio-item"><span class="file-icon">📝</span><div class="file-name">Research Proposal<br>(Approved)</div></div>
                <div class="portfolio-item"><span class="file-icon">💼</span><div class="file-name">CV Design<br>(Mopani Mine)</div></div>
            </div>
        </div>

        <div class="card">
            <h2>About Us</h2>
            <p style="color: #475569;"><strong>PrimeGrade Solutions</strong> bridges the gap between complex engineering concepts and academic success. Precision, integrity, and results.</p>
        </div>

        <div class="card">
            <h2>How It Works</h2>
            <div class="step-container">
                <div class="step-box">
                    <div class="step-num" style="background: #e0f2fe; color: var(--primary);">1</div>
                    <div class="step-title">Send Details</div>
                    <div class="step-desc">Fill the form below</div>
                </div>
                <div class="step-box">
                    <div class="step-num" style="background: #fef3c7; color: #b45309;">2</div>
                    <div class="step-title">Get Quote</div>
                    <div class="step-desc">Receive fixed price</div>
                </div>
                <div class="step-box">
                    <div class="step-num" style="background: #dcfce7; color: #15803d;">3</div>
                    <div class="step-title">Success</div>
                    <div class="step-desc">Get your work</div>
                </div>
            </div>
        </div>

        <div class="card">
            <h2>Trusted by Students</h2>
            <div class="testimonial-grid">
                <div class="review-box">
                    <div class="stars">★★★★★</div>
                    <p>"The circuit analysis breakdown was clear and helped me pass my exam."</p>
                    <div style="font-weight:bold; margin-top:5px; font-size:12px;">— CBU Student</div>
                </div>
                <div class="review-box">
                    <div class="stars">★★★★★</div>
                    <p>"Fastest CV service I've used. Got the internship interview immediately."</p>
                    <div style="font-weight:bold; margin-top:5px; font-size:12px;">— UNZA Graduate</div>
                </div>
            </div>
        </div>

        <div class="card" id="order-form">
            <h2>Start Your Order</h2>
            <p style="text-align: center; color: #64748b; margin-bottom: 25px;">Select your service for an instant quote.</p>

            <div class="form-group">
                <label>Service Required</label>
                <select id="service">
                    <option value="Engineering Calculation">⚙️ Engineering / Math Calculation</option>
                    <option value="Academic Assignment">📝 Academic Assignment (Essay/Report)</option>
                    <option value="Research/Thesis Support">🎓 Research Proposal or Thesis</option>
                    <option value="CV/Resume Design">💼 Professional CV / Resume Design</option>
                    <option value="Homework Q&A">🔓 Homework Q&A (Chegg/CourseHero)</option>
                </select>
            </div>

            <div class="form-group">
                <label>Urgency</label>
                <select id="urgency">
                    <option value="Standard (3-5 Days)">Standard (3-5 Days)</option>
                    <option value="Priority (24-48 Hours)">🔥 Priority (24-48 Hours)</option>
                    <option value="CRITICAL (ASAP - Today)">🚨 CRITICAL (ASAP - Today)</option>
                </select>
            </div>

            <div class="form-group">
                <label>Topic / Module</label>
                <input type="text" id="topic" placeholder="e.g. Power Systems...">
                
                <div class="tags-container">
                    <div class="tag">Calculus</div>
                    <div class="tag">Fluids</div>
                    <div class="tag">Structures</div>
                    <div class="tag">Thermodynamics</div>
                </div>
            </div>

            <button class="wa-btn" onclick="sendToWhatsApp()">➤ Send Inquiry via WhatsApp</button>
        </div>

        <div class="card">
            <h2>FAQ</h2>
            <details><summary>Is my information confidential?</summary><div class="faq-answer">Yes, 100%. We never share client data.</div></details>
            <details><summary>How do I make payment?</summary><div class="faq-answer">We accept Mobile Money (MTN, Airtel, Zamtel) and PayPal.</div></details>
            <details><summary>Can you handle urgent deadlines?</summary><div class="faq-answer">Yes! Select "CRITICAL" for same-day work.</div></details>
        </div>

        <div class="card" style="text-align: center;">
            <h3 style="margin-bottom:5px;">💳 Payment Options</h3>
            <p style="font-size:12px; color:#94a3b8;">ZAMBIA & INTERNATIONAL</p>
            
            <div class="payment-row">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/MTN_Logo.svg/200px-MTN_Logo.svg.png" alt="MTN" class="pay-icon">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/Airtel_Logo.svg/200px-Airtel_Logo.svg.png" alt="Airtel" class="pay-icon">
                <div class="zamtel-badge">ZAMTEL</div>
                <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal" class="pay-icon">
            </div>
        </div>

        <div class="footer">
            <div class="footer-links">
                <a href="#">Home</a> | <a href="#service">Services</a> | <a href="https://wa.me/260951036866">Contact</a> | <a href="#">Terms</a>
            </div>
            <div>© 2026 PrimeGrade Solutions. All Rights Reserved.</div>
            <div class="disclaimer">Disclaimer: All services are provided for research, reference, and academic assistance purposes only.</div>
        </div>

    </div>

    <script>
        function sendToWhatsApp() {
            var service = document.getElementById("service").value;
            var urgency = document.getElementById("urgency").value;
            var topic = document.getElementById("topic").value;
            var phone = "260951036866"; 
            var text = "*New Inquiry for PrimeGrade Solutions* %0a%0a📌 *Service:* " + service + "%0a⏰ *Urgency:* " + urgency + "%0a";
            if(topic) { text += "📚 *Topic:* " + topic + "%0a"; }
            text += "%0a_Hello, I would like a quote for this work._";
            window.open("https://wa.me/" + phone + "?text=" + text, '_blank');
        }
    </script>
</body>
</html>
