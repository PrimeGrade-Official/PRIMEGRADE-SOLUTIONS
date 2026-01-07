<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PrimeGrade Solutions | Excellence, Integrity, Precision</title>
    <style>
        :root {
            /* 1. VISUAL UPDATES */
            --primary: #0f172a; /* Deep Navy */
            --secondary: #334155; /* Slate */
            --gold: #fbbf24;    /* Bright Gold */
            --light: #f8fafc;
            --white: #ffffff;
        }
        body { font-family: 'Segoe UI', sans-serif; margin: 0; padding: 0; background-color: var(--light); color: #333; line-height: 1.6; }
        
        /* 2. HEADER & GLOW EFFECT */
        .header { 
            background: linear-gradient(135deg, var(--primary), #1e293b); 
            color: white; 
            padding: 40px 20px 30px 20px; 
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
            margin-bottom: 15px;
            /* Glow Effect */
            box-shadow: 0 0 20px rgba(251, 191, 36, 0.5);
        }
        .brand { font-size: 32px; font-weight: 800; letter-spacing: 1px; margin: 5px 0; }
        .sub-headline { color: #cbd5e1; font-size: 16px; margin-top: 5px; font-weight: 400; }

        /* CONTAINER */
        .container { max-width: 800px; margin: -25px auto 40px auto; padding: 20px; }

        /* CARDS (Rounded Corners) */
        .card {
            background: white;
            border-radius: 16px; /* 3. ROUNDED CORNERS */
            padding: 25px;
            box-shadow: 0 10px 30px -5px rgba(0, 0, 0, 0.1);
            margin-bottom: 25px;
        }

        h2 { color: var(--primary); border-left: 6px solid var(--gold); padding-left: 15px; margin-top: 0; }

        /* 3. PORTFOLIO SCROLL */
        .portfolio-scroll {
            display: flex;
            overflow-x: auto;
            gap: 15px;
            padding-bottom: 10px;
            scrollbar-width: none; /* Hide scrollbar for cleaner look */
        }
        .portfolio-item {
            min-width: 140px;
            background: #f1f5f9;
            border-radius: 12px;
            padding: 15px;
            text-align: center;
            border: 1px solid #e2e8f0;
        }
        .file-icon { font-size: 30px; margin-bottom: 5px; display: block; }
        .file-name { font-size: 13px; font-weight: bold; color: var(--secondary); }

        /* 4. SUBJECT PILLS */
        .tags-container { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 20px; }
        .tag {
            background: #e0f2fe;
            color: var(--primary);
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
            border: 1px solid #bae6fd;
        }

        /* 5. FORM STYLING */
        .form-group { margin-bottom: 20px; }
        label { display: block; font-weight: 700; margin-bottom: 8px; color: var(--secondary); }
        select, input { 
            width: 100%; 
            padding: 15px; /* Increased Padding */
            border: 2px solid #e2e8f0; 
            border-radius: 12px; 
            font-size: 16px; 
            background: #f8fafc; 
            box-sizing: border-box; 
            transition: 0.3s;
        }
        /* Focus State: Gold Border */
        select:focus, input:focus { 
            border-color: var(--gold); 
            background: white; 
            outline: none; 
            box-shadow: 0 0 0 4px rgba(251, 191, 36, 0.1);
        }

        /* BUTTON (Floating Shadow) */
        .wa-btn {
            background: linear-gradient(to right, #16a34a, #22c55e);
            color: white; width: 100%; padding: 18px; border: none; border-radius: 12px; 
            font-size: 18px; font-weight: bold; cursor: pointer; 
            display: flex; align-items: center; justify-content: center;
            box-shadow: 0 8px 20px -5px rgba(34, 197, 94, 0.4); /* Floating Effect */
            transition: transform 0.2s;
        }
        .wa-btn:active { transform: scale(0.98); }

        /* 6. TESTIMONIAL GRID */
        .testimonial-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        @media (max-width: 600px) { .testimonial-grid { grid-template-columns: 1fr; } } /* Stack on mobile */
        
        .review-box {
            background: #f8fafc;
            padding: 15px;
            border-radius: 12px;
            border-left: 4px solid var(--gold);
            font-size: 14px;
        }
        .stars { color: var(--gold); margin-bottom: 5px; font-size: 18px; }

        /* 7. COLLAPSIBLE FAQ */
        details {
            border-bottom: 1px solid #e2e8f0;
            padding: 15px 0;
            cursor: pointer;
        }
        summary { font-weight: bold; color: var(--primary); list-style: none; display: flex; justify-content: space-between; align-items: center; }
        summary::after { content: "+"; font-size: 20px; color: var(--gold); }
        details[open] summary::after { content: "-"; }
        .faq-answer { margin-top: 10px; font-size: 14px; color: #64748b; line-height: 1.5; }

        /* 8. PAYMENT LOGOS */
        .payment-row { display: flex; justify-content: center; gap: 15px; margin-top: 10px; flex-wrap: wrap; }
        .pay-icon { height: 40px; width: auto; border-radius: 6px; border: 1px solid #e2e8f0; padding: 4px; background: white; }
        .zamtel-badge {
            height: 40px; 
            width: 80px; 
            background: #009639; 
            color: white; 
            font-weight: bold; 
            font-size: 12px; 
            display: flex; align-items: center; justify-content: center; 
            border-radius: 6px;
        }

        /* 9. FOOTER */
        .footer { text-align: center; color: #94a3b8; padding-bottom: 30px; font-size: 13px; }
        .disclaimer { font-size: 11px; margin-top: 10px; opacity: 0.7; }

    </style>
</head>
<body>

    <div class="header">
        <img src="https://cdn-icons-png.flaticon.com/512/3135/3135810.png" alt="Logo" class="logo-img">
        <div class="brand">PRIMEGRADE SOLUTIONS</div>
        <div class="sub-headline">Zambia's Leading Engineering & Academic Consultancy</div>
    </div>

    <div class="container">
        
        <div class="card">
            <h3 style="margin-top:0; color:var(--secondary);">📂 Recent Successful Projects</h3>
            <div class="portfolio-scroll">
                <div class="portfolio-item">
                    <span class="file-icon">⚡</span>
                    <div class="file-name">Circuit Analysis<br>(Distinction)</div>
                </div>
                <div class="portfolio-item">
                    <span class="file-icon">🏗️</span>
                    <div class="file-name">Fluid Mechanics<br>Calculation</div>
                </div>
                <div class="portfolio-item">
                    <span class="file-icon">📝</span>
                    <div class="file-name">Research Proposal<br>(Approved)</div>
                </div>
                <div class="portfolio-item">
                    <span class="file-icon">💼</span>
                    <div class="file-name">CV Design<br>(Mopani Mine)</div>
                </div>
            </div>
        </div>

        <div class="card">
            <h2>About Us</h2>
            <p style="color: #475569;"><strong>PrimeGrade Solutions</strong> bridges the gap between complex engineering concepts and academic success. We don't just solve problems; we explain the 'Why' behind them.</p>
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

        <div class="card">
            <h2>Start Your Order</h2>
            
            <div class="tags-container">
                <div class="tag">Calculus</div>
                <div class="tag">Fluids</div>
                <div class="tag">Structures</div>
                <div class="tag">Thermodynamics</div>
                <div class="tag">Electronics</div>
                <div class="tag">Marketing</div>
            </div>

            <p style="text-align: center; color: #64748b; margin-bottom: 25px;">Select your service below for an instant quote.</p>

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
            </div>

            <button class="wa-btn" onclick="sendToWhatsApp()">➤ Send Inquiry via WhatsApp</button>
        </div>

        <div class="card">
            <h2>FAQ</h2>
            
            <details>
                <summary>Is my information confidential?</summary>
                <div class="faq-answer">Yes, 100%. We value your privacy and never share client data.</div>
            </details>

            <details>
                <summary>How do I make payment?</summary>
                <div class="faq-answer">We accept Mobile Money (MTN, Airtel, Zamtel) and PayPal/Payoneer.</div>
            </details>

            <details>
                <summary>Can you handle urgent deadlines?</summary>
                <div class="faq-answer">Yes! Select "CRITICAL" in the form for work needed in less than 24 hours.</div>
            </details>
        </div>

        <div class="card" style="text-align: center;">
            <h3 style="margin-bottom:5px;">💳 Payment Options</h3>
            <p style="font-size:12px; color:#94a3b8; margin-bottom:15px;">ZAMBIA & INTERNATIONAL</p>
            
            <div class="payment-row">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/MTN_Logo.svg/200px-MTN_Logo.svg.png" alt="MTN" class="pay-icon">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/Airtel_Logo.svg/200px-Airtel_Logo.svg.png" alt="Airtel" class="pay-icon">
                <div class="zamtel-badge">ZAMTEL</div>
            </div>
            <div class="payment-row">
                <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal" class="pay-icon">
                <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/Payoneer_logo.svg" alt="Payoneer" class="pay-icon">
            </div>
        </div>

        <div class="footer">
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
