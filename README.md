# Fund.me
Fundraising 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hope and Healing: Urgent Medical Aid for War Victims in Gaza & Sudan</title>
    <style>
        /* General Reset and Base Styles */
        :root {
            --primary-blue: #0a3d62; /* Dark blue for main elements, taken from PayPal style */
            --accent-blue: #00877a; /* GoFundMe-like green/blue for CTAs */
            --light-grey: #f0f0f0;
            --mid-grey: #d0d0d0;
            --max-width: 1000px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Arial', 'Helvetica Neue', Helvetica, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: var(--light-grey);
            padding-bottom: 50px; /* Space for the footer */
        }

        a {
            color: var(--primary-blue);
            text-decoration: none;
        }
        
        a:hover {
            text-decoration: underline;
        }

        /* Container for Main Content */
        .page-container {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* Header (Minimal GoFundMe-like bar) */
        .header {
            background: #fff;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            padding: 10px 20px;
            text-align: center;
        }

        .header h1 {
            color: var(--primary-blue);
            font-size: 24px;
            font-weight: 700;
        }
        
        /* Two-Column Layout for Hero Section */
        #hero-content {
            display: flex;
            gap: 30px;
            padding: 20px 0;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 16px rgba(0,0,0,0.05);
        }

        .main-content {
            flex: 2; /* Main story/image takes more space */
            padding: 0 20px;
        }

        .sidebar-donation {
            flex: 1; /* Donation box takes less space */
            min-width: 300px;
            padding: 0 20px;
        }

        /* Media Queries for Responsiveness (GoFundMe stacks on mobile) */
        @media (max-width: 768px) {
            #hero-content {
                flex-direction: column;
            }

            .sidebar-donation {
                order: -1; /* Move donation box to the top on mobile */
            }
        }

        /* Hero Image/Video Placeholder */
        .hero-media {
            width: 100%;
            height: 350px;
            background: #ccc url('https://via.placeholder.com/800x450?text=Photo+of+Medical+Humanitarian+Aid+for+War+Victims') no-repeat center center/cover;
            border-radius: 8px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 18px;
            font-weight: bold;
            text-shadow: 1px 1px 2px #000;
        }
        
        .hero-title {
            font-size: 2.2em;
            color: #1a1a1a;
            margin-bottom: 10px;
            line-height: 1.2;
        }

        /* Progress Bar Style */
        .progress-container {
            margin: 20px 0;
            background-color: var(--light-grey);
            border-radius: 10px;
            height: 10px;
            overflow: hidden;
        }

        .progress-bar {
            height: 100%;
            width: 45%; /* Placeholder progress */
            background-color: var(--accent-blue);
            transition: width 0.5s ease;
        }

        .progress-details {
            display: flex;
            justify-content: space-between;
            font-size: 1.1em;
            font-weight: bold;
            color: var(--primary-blue);
        }

        .progress-details span {
            color: #555;
            font-weight: normal;
        }

        /* General Section Styling (Story, Use of Funds, Organizer) */
        section {
            background: #fff;
            padding: 30px 40px;
            border-radius: 8px;
            box-shadow: 0 4px 16px rgba(0,0,0,0.05);
        }

        section h2 {
            color: var(--primary-blue);
            font-size: 1.8em;
            margin-bottom: 20px;
            border-bottom: 2px solid var(--light-grey);
            padding-bottom: 10px;
        }

        /* Specific Styles for Story Section */
        #story p {
            margin-bottom: 15px;
            color: #555;
            font-size: 1.05em;
        }
        
        .emphasized-quote {
            font-style: italic;
            border-left: 4px solid var(--accent-blue);
            padding-left: 15px;
            margin: 20px 0;
            color: #333;
        }

        /* Use of Funds Section */
        .fund-breakdown ul {
            list-style: none;
            padding: 0;
        }

        .fund-breakdown li {
            padding: 10px 0;
            border-bottom: 1px dashed var(--mid-grey);
            display: flex;
            justify-content: space-between;
        }

        .fund-breakdown li:last-child {
            border-bottom: none;
        }

        .fund-breakdown strong {
            color: var(--accent-blue);
        }

        /* Organizer Section */
        .organizer-profile {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .organizer-profile img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--mid-grey);
        }

        .organizer-info h3 {
            margin-bottom: 5px;
            color: var(--primary-blue);
        }
        
        .organizer-info p {
            color: #777;
            font-size: 0.9em;
        }

        /* Final CTA Section */
        #final-cta {
            text-align: center;
            padding: 40px;
            background: var(--primary-blue);
            color: #fff;
        }
        
        #final-cta h2 {
            color: #fff;
            border-bottom: none;
            margin-bottom: 10px;
        }
        
        .main-donate-btn {
            display: inline-block;
            background: var(--accent-blue);
            color: white;
            padding: 15px 30px;
            border-radius: 8px;
            font-size: 1.2em;
            font-weight: bold;
            margin-top: 20px;
            transition: background 0.3s;
        }
        
        .main-donate-btn:hover {
            background: #00a08e;
            text-decoration: none;
        }

        /* --- PayPal Custom Block CSS (DO NOT ALTER STRUCTURE) --- */

        .donation-box {
            max-width: 420px;
            margin: 30px auto;
            padding: 25px;
            background: #ffffff;
            border-radius: 14px;
            box-shadow: 0 4px 16px rgba(0,0,0,0.09);
            text-align: center;
            font-family: Arial, sans-serif;
            border: 1px solid var(--mid-grey); /* Added border for better separation */
        }

        .donation-box h2 {
            margin-bottom: 18px;
            font-size: 22px;
            color: var(--primary-blue);
            border-bottom: none;
            padding-bottom: 0;
        }

        .amount-buttons button {
            margin: 6px;
            padding: 10px 18px;
            border-radius: 8px;
            border: 1px solid #d0d0d0;
            background: #f5f5f5;
            cursor: pointer;
            transition: 0.25s;
            font-size: 1em;
            color: #333;
        }

        .amount-buttons button.active {
            background: var(--primary-blue);
            color: #fff;
            border-color: var(--primary-blue);
        }

        .amount-buttons button:hover {
            opacity: 0.8;
        }

        #customAmount {
            margin-top: 14px;
            padding: 10px;
            width: 180px;
            border-radius: 8px;
            border: 1px solid #ccc;
            text-align: center;
        }

        #paypal-button-container {
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>Medical Aid for War Victims</h1>
    </div>

    <div class="page-container">
        
        <div id="hero-content">
            
            <div class="sidebar-donation">
                
                <div class="progress-details">
                    <span id="raised-amount">$45,000</span> raised
                    <span id="goal-amount"> of $200,000 goal</span>
                </div>
                <div class="progress-container">
                    <div class="progress-bar" style="width: 22.5%;"></div>
                </div>
                <p style="font-size: 0.9em; text-align: right; color: #777;">987 people donated</p>
                
                <script src="https://www.paypal.com/sdk/js?client-id=BAAC0yEtUR9x7Uem-fxiee6diJI5p8YiHbxvA8wB0NRtOCct_9MF8ATmSUQ98EaqdfewMTkzXCEjgzqrL8&currency=USD"></script>

                <div class="donation-box">
                    <h2>Choose Your Donation</h2>

                    <div class="amount-buttons">
                        <button data-amount="10">10 USD</button>
                        <button data-amount="25" class="active">25 USD</button>
                        <button data-amount="50">50 USD</button>
                        <button data-amount="100">100 USD</button>
                    </div>

                    <input id="customAmount" type="number" placeholder="Enter custom amount" />

                    <div id="paypal-button-container"></div>
                </div>

                <script>
                    let selectedAmount = 25; // default

                    const presetButtons = document.querySelectorAll('.amount-buttons button');

                    // Set initial active state based on default
                    document.querySelector('.amount-buttons button[data-amount="25"]').classList.add('active');


                    presetButtons.forEach(btn => {
                        btn.addEventListener('click', () => {
                            presetButtons.forEach(b => b.classList.remove('active'));
                            btn.classList.add('active');
                            selectedAmount = parseFloat(btn.dataset.amount);
                            document.getElementById('customAmount').value = ''; // Clear custom input
                        });
                    });

                    document.getElementById('customAmount').addEventListener('input', function() {
                        let value = parseFloat(this.value);
                        if (value > 0) {
                            selectedAmount = value;
                            presetButtons.forEach(b => b.classList.remove('active'));
                        }
                    });

                    // Ensure the SDK is loaded before accessing paypal object
                    if (typeof paypal !== 'undefined') {
                        paypal.Buttons({
                            style: {
                                color: 'blue',
                                shape: 'rect',
                                label: 'donate',
                                layout: 'vertical'
                            },

                            createOrder: function(data, actions) {
                                return actions.order.create({
                                    purchase_units: [{
                                        amount: { value: selectedAmount.toFixed(2) },
                                        description: "Donation for medical aid and prosthetic limbs"
                                    }]
                                });
                            },

                            onApprove: function(data, actions) {
                                return actions.order.capture().then(function(details) {
                                    document.querySelector('.donation-box').innerHTML =
                                        "<h2 style='color:#0a3d62;'>Thank you ♥ Your donation has been received.</h2>";
                                });
                            },

                            onError: function(err) {
                                alert("There was an error. Please try again.");
                                console.error(err);
                            }

                        }).render('#paypal-button-container');
                    } else {
                         document.getElementById('paypal-button-container').innerHTML = 
                            '<p style="color:red; margin-top:10px;">PayPal SDK failed to load. Please check network connection.</p>';
                    }
                </script>
                </div>
            
            <div class="main-content">
                <div class="hero-title">Hope and Healing: Urgent Medical Aid for War Victims in Gaza & Sudan</div>
                <div class="hero-media">
                    Photo related to humanitarian medical aid (Prosthetics/Medical Team)
                </div>
            </div>
            
        </div>

        <section id="story">
            <h2>The Need for Hope and Mobility</h2>
            <p>The conflicts in Gaza and Sudan have created a humanitarian crisis of unimaginable scale. Beyond the immediate needs for food and shelter, thousands of war victims—including countless children—are suffering from life-altering injuries. Many have lost limbs and require urgent, specialized medical care and prosthetic devices to regain their independence and quality of life.</p>

            <div class="emphasized-quote">
                "Our mission is simple: to restore dignity and mobility. A prosthetic limb is not just a piece of equipment; it is a path back to school, work, and a normal life for a survivor who has lost everything."
            </div>
            
            <p>Your support directly funds crucial surgeries, trauma care, and the production of custom-fit prosthetic limbs. We are partnering with local, vetted medical organizations operating on the ground who have the expertise to deliver this highly specialized aid.</p>

            <div style="text-align: center; margin: 30px 0;">
                <img src="https://via.placeholder.com/600x200?text=Photo+of+Medical+Supplies+or+Patient+with+Aid" alt="Photo of humanitarian aid supplies" style="max-width: 100%; border-radius: 8px; opacity: 0.8;">
            </div>
            
            <p>The demand far outweighs the current resources. Every second counts, and every dollar brings us closer to securing the future for a survivor who has lost a limb. Join us in transforming lives from surviving to thriving.</p>
        </section>

        <section id="use-of-funds">
            <h2>Transparent Use of Funds</h2>
            <p>We are committed to full transparency. 100% of the net funds raised will be allocated directly to medical aid and prosthetic support in Gaza and Sudan. Here is how your donation will be used:</p>
            
            <div class="fund-breakdown">
                <ul>
                    <li><strong>Prosthetic Limbs & Rehabilitation:</strong> <span>60%</span></li>
                    <li><strong>Emergency Surgeries & Trauma Care:</strong> <span>30%</span></li>
                    <li><strong>Medical Supplies & Logistics:</strong> <span>10%</span></li>
                </ul>
            </div>
            
            <p style="margin-top: 20px; font-style: italic;">We will provide detailed reports and photographic proof of fund disbursement to ensure every supporter sees the impact of their generosity. Our administrative costs are covered by a separate endowment to maximize the direct aid provided.</p>
        </section>

        <section id="organizer">
            <h2>About the Organizer</h2>
            <div class="organizer-profile">
                <img src="https://via.placeholder.com/100x100?text=Organizer+Photo" alt="Organizer Profile Photo">
                <div class="organizer-info">
                    <h3>The Global Health Initiative (GHI)</h3>
                    <p>Verified Humanitarian Aid Organization</p>
                    <p>The GHI has been providing medical relief in conflict zones for over a decade. Our team includes specialized orthopedic surgeons, trauma nurses, and logistics experts dedicated to delivering life-saving assistance where it is needed most. We have established secure corridors for delivering aid into both Gaza and Sudan.</p>
                    <p><a href="#use-of-funds">See how your donation is protected and used.</a></p>
                </div>
            </div>
        </section>

        <section id="final-cta">
            <h2>Be the reason someone walks again.</h2>
            <p>Your compassion can bridge the gap between injury and independence. Donate today.</p>
            <a href="#" class="main-donate-btn">DONATE NOW & HEAL LIVES</a> 
        </section>

    </div>
</body>
</html>
