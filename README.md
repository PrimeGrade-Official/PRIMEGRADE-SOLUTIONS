<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PrimeGrade Solutions</title>
    <style>
        body { font-family: sans-serif; margin: 0; padding: 0; background-color: #f8fafc; color: #333; }
        
        /* NAVY AND GOLD THEME */
        .header { background: #0f172a; color: white; padding: 40px 20px; text-align: center; border-bottom: 5px solid #fbbf24; }
        .brand { font-size: 28px; font-weight: bold; margin: 10px 0; }
        .sub-text { color: #cbd5e1; font-size: 14px; }
        
        /* LAYOUT */
        .container { max-width: 700px; margin: auto; padding: 20px; }
        .card { background: white; border-radius: 12px; padding: 20px; margin-bottom: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        h2 { color: #0f172a; border-left: 5px solid #fbbf24; padding-left: 10px; }
        
        /* PORTFOLIO SCROLL */
        .scroll-box { display: flex; overflow-x: auto; gap: 10px; padding-bottom: 10px; }
        .job-item { min-width: 120px; background: #f1f5f9; padding: 10px; border-radius: 8px; text-align: center; font-size: 12px; font-weight: bold; border: 1px solid #e2e8f0; }

        /* FORM */
        select, input { width: 100%; padding: 15px; margin-bottom: 15px; border: 2px solid #e2e8f0; border-radius: 10px; background: #fff; box-sizing: border-box; }
        
        /* BUTTON */
        .btn { display: block; width: 100%; padding: 15px; background: #22c55e; color: white; text-align: center; border-radius: 10px; font-weight: bold; text-decoration: none; border: none; font-size: 18px; }
        
        /* PAYMENT */
        .pay-row { display: flex; justify-content: center; gap: 10px; margin-top: 10px; }
        .pay-Badge { background: #009639; color: white; padding: 10px; border-radius: 5px; font-size: 12px; font-weight: bold; }
    </style>
</head>
<body>

    <div class="header">
        <div class="brand">PRIMEGRADE SOLUTIONS</div>
        <div class="sub-text">Zambia's Leading Academic Consultancy</div>
    </div>

    <div class="container">
        
        <div class="card">
            <h3>📂 Recent Successes</h3>
            <div class="scroll-box">
                <div class="job-item">⚡ Circuit Analysis<br>(Distinction)</div>
                <div class="job-item">🏗️ Fluid Mechanics<br>(Calculation)</div>
                <div class="job-item">📝 Thesis Proposal<br>(Approved)</div>
            </div>
        </div>

        <div class="card">
            <h2>Get a Quote</h2>
            <p style="text-align:center; color:#64748b;">Select your service below:</p>
            
            <label>Service:</label>
            <select id="service">
                <option>Engineering Calculation</option>
                <option>Academic Assignment</option>
                <option>Research/Thesis</option>
                <option>CV/Resume Design</option>
                <option>Homework Q&A</option>
            </select>

            <label>Urgency:</label>
            <select id="urgency">
                <option>Standard (3-5 Days)</option>
                <option>Priority (24-48 Hours)</option>
                <option>CRITICAL (Today)</option>
            </select>

            <label>Topic:</label>
            <input type="text" id="topic" placeholder="e.g. Thermodynamics...">

            <button class="btn" onclick="sendWhatsApp()">➤ Send Inquiry</button>
        </div>

        <div class="card" style="text-align:center;">
            <h3>💳 Payment Methods</h3>
            <div class="pay-row">
                <div class="pay-Badge" style="background:#ffcc00; color:black;">MTN</div>
                <div class="pay-Badge" style="background:#ff0000;">AIRTEL</div>
                <div class="pay-Badge">ZAMTEL</div>
            </div>
        </div>
        
        <p style="text-align:center; font-size:12px; color:#999;">© 2026 PrimeGrade Solutions</p>
    </div>

    <script>
        function sendWhatsApp() {
            var service = document.getElementById("service").value;
            var urgency = document.getElementById("urgency").value;
            var topic = document.getElementById("topic").value;
            var url = "https://wa.me/260951036866?text=" + "I need a quote for: " + service + " (" + urgency + ")";
            window.open(url, '_blank');
        }
    </script>

</body>
</html>
