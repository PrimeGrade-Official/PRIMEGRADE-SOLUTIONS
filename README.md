<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PrimeGrade Solutions | Excellence, Integrity, Precision</title>
    <style>
        :root {
            --primary: #0f172a; /* Deep Navy */
            --secondary: #1e293b; /* Dark Slate */
            --accent: #22c55e;  /* WhatsApp Green */
            --gold: #fbbf24;    /* Academic Gold */
            --light: #f1f5f9;
        }
        body { font-family: 'Segoe UI', sans-serif; margin: 0; padding: 0; background-color: var(--light); color: #333; line-height: 1.6; }
        
        /* HEADER */
        .header { 
            background: linear-gradient(135deg, var(--primary), var(--secondary)); 
            color: white; 
            padding: 30px 20px; 
            text-align: center; 
            border-bottom: 4px solid var(--gold);
        }
        
        .logo-img { 
            width: 80px; height: 80px; 
            background-color: white; 
            border-radius: 50%; 
            padding: 5px; 
            object-fit: contain; 
            border: 3px solid var(--gold); 
            margin-bottom: 10px;
        }

        .brand { font-size: 28px; font-weight: 800; letter-spacing: 1px; margin: 5px 0; }
        .tagline { color: var(--gold); font-size: 14px; font-weight: 500; text-transform: uppercase; letter-spacing: 2px; }

        /* CONTAINER */
        .container { max-width: 700px; margin: -30px auto 80px auto; padding: 20px; }

        /* CARDS */
        .card {
            background: white;
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
            margin-bottom: 25px;
        }

        h2 { color: var(--primary); border-left: 5px solid var(--gold); padding-left: 15px; margin-top: 0; }
        h3 { color: var(--secondary); margin-bottom: 10px; font-size: 18px; }

        /* ABOUT SECTION */
        .founder-badge {
            background-color: #f8fafc;
            border-left: 4px solid var(--primary);
            padding: 15px;
            margin-top: 20px;
            border-radius: 0 8px 8px 0;
            font-style: italic;
        }

        /* HOW IT WORKS STEPS */
        .step-container { display: flex; justify-content: space-around; margin-top: 20px; flex-wrap: wrap; text-align: center; }
        .step-box { flex: 1; min-width: 140px; margin: 10px; }
        .step-num { font-size: 24px; width: 50px; height: 50px; line-height: 50px; border-radius: 50%; margin: 0 auto; font-weight: bold; }
        
        /* PAYMENT LOGOS */
        .payment-section { margin-top: 20px; }
        .payment-label { font-size: 14px; color: #64748b; font-weight: bold; margin-bottom: 10px; text-transform: uppercase; letter-spacing: 1px; }
        .payment-row { display: flex; justify-content: center; gap: 15px; margin-bottom: 20px; flex-wrap: wrap; }
        
        .pay-icon {
            height: 45px;
            width: auto;
            border-radius: 6px;
            border: 1px solid #e2e8f0;
            padding: 5px;
            background: white;
        }

        /* FORM */
        .form-group { margin-bottom: 20px; }
        label { display: block; font-weight: 700; margin-bottom: 8px; color: var(--secondary); }
        select, input { width: 100%; padding: 14px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 16px; background: #f8fafc; box-sizing: border-box; }
        
        /* WHATSAPP BUTTONS */
        .wa-btn {
            background: linear-gradient(to right, #16a34a, #22c55e);
            color: white; width: 100%; padding: 18px; border: none; border-radius: 12px; font-size: 18px; font-weight: bold; cursor: pointer; display: flex; align-items: center; justify-content: center;
        }
        .float-btn {
            position: fixed; bottom: 20px; right: 20px; background-color: #25D366; color: white; border-radius: 50%; width: 60px; height: 60px; text-align: center; font-size: 30px; line-height: 60px; box-shadow: 2px 2px 10px rgba(0,0,0,0.3); z-index: 1000; text-decoration: none;
        }

        .footer { text-align: center; font-size: 13px; color: #94a3b8; padding-bottom: 30px; }
    </style>
</head>
<body>

    <div class="header">
        <img src="https://cdn-icons-png.flaticon.com/512/3135/3135810.png" alt="Logo" class="logo-img">
        <div class="brand">PRIMEGRADE SOLUTIONS</div>
        <div class="tagline">Excellence • Integrity • Precision</div>
    </div>

    <div class="container">
        
        <div class="card">
            <h2>About Us</h2>
            <p style="color: #475569;"><strong>PrimeGrade Solutions</strong> is Zambia's leading academic consultancy. We bridge the gap between complex engineering concepts and academic distinction. We don't just provide answers; we provide understanding.</p>
            <div class="founder-badge">
                <p>"Founded by an Electromechanical Engineering specialist to bring precision and reliability to academic support."</p>
                <p style="margin-top:10px; font-weight:bold;">— Raphael Muselema</p>
            </div>
        </div>

        <div class="card">
            <h2>How It Works</h2>
            <div class="step-container">
                <div class="step-box">
                    <div class="step-num" style="background: #e0f2fe; color: var(--primary);">1</div>
                    <h4 style="margin: 10px 0;">Send Details</h4>
                    <p style="font-size: 13px; color: #64748b;">Fill the form below or WhatsApp us.</p>
                </div>
                <div class="step-box">
                    <div class="step-num" style="background: #fef3c7; color: #b45309;">2</div>
                    <h4 style="margin: 10px 0;">Get Quote</h4>
                    <p style="font-size: 13px; color: #64748b;">Receive a fixed price based on urgency.</p>
                </div>
                <div class="step-box">
                    <div class="step-num" style="background: #dcfce7; color: #15803d;">3</div>
                    <h4 style="margin: 10px 0;">Receive Work</h4>
                    <p style="font-size: 13px; color: #64748b;">Get Distinction-grade solutions.</p>
                </div>
            </div>
        </div>

        <div class="card">
            <h2>Start Your Order</h2>
            <p style="text-align: center; color: #64748b; margin-bottom: 25px;">Select your service for an instant quote.</p>

            <div class="form-group">
                <label>Service Required</label>
                <select id="service">
                    <option value="Engineering Calculation">⚙️ Engineering / Math Calculation</option>
                    <option value="Academic Assignment">📝 Academic Assignment (Essay/Report)</option>
                    <option value="Research/Thesis Support">🎓 Research Proposal or Thesis</option>
                    <option value="CV/Resume Design">💼 Professional CV / Resume Design</option>
                    <option value="Chegg/Bartleby Unlock">🔓 Homework Q&A (Chegg/Bartleby)</option>
                    <option value="AutoCAD Design">🏗️ AutoCAD Design & Drafting</option>
                </select>
            </div>

            <div class="form-group">
                <label>Urgency Level</label>
                <select id="urgency">
                    <option value="Standard (3-5 Days)">Standard (3-5 Days)</option>
                    <option value="Priority (24-48 Hours)">🔥 Priority (24-48 Hours)</option>
                    <option value="CRITICAL (ASAP - Today)">🚨 CRITICAL (ASAP - Today)</option>
                </select>
            </div>

            <div class="form-group">
                <label>Topic / Module (Optional)</label>
                <input type="text" id="topic" placeholder="e.g. Circuit Analysis, Marketing...">
            </div>

            <button class="wa-btn" onclick="sendToWhatsApp()">
                <span style="margin-right:10px; font-size:20px;">➤</span> Send Inquiry via WhatsApp
            </button>
        </div>

        <div class="card" style="text-align: center;">
            <h3>💳 Payment Options</h3>
            
            <div class="payment-section">
                <div class="payment-label">🇿🇲 Local Clients (Zambia)</div>
                <div class="payment-row">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/MTN_Logo.svg/200px-MTN_Logo.svg.png" alt="MTN Money" class="pay-icon">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/Airtel_Logo.svg/200px-Airtel_Logo.svg.png" alt="Airtel Money" class="pay-icon">
                    <div class="pay-icon" style="display:flex; align-items:center; justify-content:center; background:#009639; color:white; font-weight:bold; width:80px; font-size:12px;">ZAMTEL</div>
                </div>
            </div>

            <div class="payment-section">
                <div class="payment-label">🌍 International Clients</div>
                <div class="payment-row">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal" class="pay-icon">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/Payoneer_logo.svg" alt="Payoneer" class="pay-icon">
                </div>
            </div>
        </div>

        <div class="footer">
            <p>© 2026 PrimeGrade Solutions. All Rights Reserved.</p>
        </div>

    </div>

    <a href="https://wa.me/260951036866" target="_blank" class="float-btn">💬</a>

    <script>
        function sendToWhatsApp() {
            var service = document.getElementById("service").value;
            var urgency = document.getElementById("urgency").value;
            var topic = document.getElementById("topic").value;
            var phone = "260951036866"; 

            var text = "*New Inquiry for PrimeGrade Solutions* %0a%0a";
            text += "📌 *Service:* " + service + "%0a";
            text += "⏰ *Urgency:* " + urgency + "%0a";
            if(topic) { text += "📚 *Topic:* " + topic + "%0a"; }
            text += "%0a_Hello, I would like a quote for this work._";

            var url = "https://wa.me/" + phone + "?text=" + text;
            window.open(url, '_blank');
        }
    </script>

</body>
</html>

