# Fund.me
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أمل وشفاء: مساعدة طبية عاجلة لضحايا الحرب</title>
    <style>
        /* General Reset and Base Styles (Arabic Support) */
        :root {
            --primary-blue: #0a3d62; 
            --accent-blue: #00877a; 
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
            font-family: 'Tahoma', 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: var(--light-grey);
            direction: rtl; /* Set direction for Arabic */
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

        /* Header (Minimal Bar) */
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
            /* Ensure the donation box is highly visible */
        }

        /* Media Queries for Responsiveness (Stacking on mobile) */
        @media (max-width: 768px) {
            #hero-content {
                flex-direction: column;
            }

            .sidebar-donation {
                order: -1; /* Move donation box to the top on mobile */
            }
        }

        /* Hero Image Placeholder */
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
            text-align: center;
        }
        
        .hero-title {
            font-size: 2.2em;
            color: #1a1a1a;
            margin-bottom: 10px;
            line-height: 1.2;
        }

        /* Progress Bar Style */
        .progress-container {
            margin: 20px 0 5px 0;
            background-color: var(--light-grey);
            border-radius: 10px;
            height: 10px;
            overflow: hidden;
        }

        .progress-bar {
            height: 100%;
            width: 22.5%; /* Placeholder progress: 45,000 / 200,000 */
            background-color: var(--accent-blue);
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

        /* General Section Styling */
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

        /* Story Section */
        #story p {
            margin-bottom: 15px;
            color: #555;
            font-size: 1.05em;
        }
        
        .emphasized-quote {
            font-style: italic;
            border-right: 4px solid var(--accent-blue); /* Adjusted border for RTL */
            padding-right: 15px;
            padding-left: 0;
            margin: 20px 0;
            color: #333;
            text-align: justify;
        }

        /* Transparency & Organizer Section */
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

        .organizer-profile {
            margin-top: 25px;
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .organizer-profile img {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--mid-grey);
        }

        /* --- PayPal Custom Block CSS (As provided) --- */

        .donation-box {
            max-width: 420px;
            margin: 30px auto;
            padding: 25px;
            background: #ffffff;
            border-radius: 14px;
            box-shadow: 0 4px 16px rgba(0,0,0,0.09);
            text-align: center;
            font-family: Arial, sans-serif;
            border: 1px solid var(--mid-grey); 
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
        <h1>مبادرة إنسانية: مساعدة طبية عاجلة</h1>
    </div>

    <div class="page-container">
        
        <div id="hero-content">
            
            <div class="sidebar-donation">
                
                <div class="progress-details">
                    <span id="raised-amount">45,000 دولار</span> تم جمعه
                    <span id="goal-amount"> من هدف 200,000 دولار</span>
                </div>
                <div class="progress-container">
                    <div class="progress-bar" style="width: 22.5%;"></div>
                </div>
                <p style="font-size: 0.9em; text-align: left; color: #777;">987 متبرعًا</p>
                
                <script src="https://www.paypal.com/sdk/js?client-id=BAAC0yEtUR9x7Uem-fxiee6diJI5p8YiHbxvA8wB0NRtOCct_9MF8ATmSUQ98EaqdfewMTkzXCEjgzqrL8&currency=USD"></script>

                <div class="donation-box">
                    <h2>اختر قيمة تبرعك</h2>

                    <div class="amount-buttons">
                        <button data-amount="10">10 دولار</button>
                        <button data-amount="25" class="active">25 دولار</button>
                        <button data-amount="50">50 دولار</button>
                        <button data-amount="100">100 دولار</button>
                    </div>

                    <input id="customAmount" type="number" placeholder="أدخل مبلغ مخصص" />

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
                                        "<h2 style='color:#0a3d62;'>شكراً لك ♥ لقد تم استلام تبرعك بنجاح.</h2>";
                                });
                            },

                            onError: function(err) {
                                alert("حدث خطأ. يرجى المحاولة مرة أخرى.");
                                console.error(err);
                            }

                        }).render('#paypal-button-container');
                    } else {
                         document.getElementById('paypal-button-container').innerHTML = 
                            '<p style="color:red; margin-top:10px;">فشل تحميل حزمة PayPal. يرجى التحقق من اتصال الشبكة.</p>';
                    }
                </script>
                </div>
            
            <div class="main-content">
                <div class="hero-title">أمل وشفاء: مساعدة طبية عاجلة لضحايا الحرب في غزة والسودان</div>
                <div class="hero-media">
                    صورة متعلقة بالإغاثة الطبية والإنسانية (لأطراف صناعية/فريق طبي)
                </div>
            </div>
            
        </div>

        <section id="story">
            <h2>إعادة الأمل والحركة</h2>
            <p>لقد أدت الصراعات في غزة والسودان إلى أزمة إنسانية مروعة. الآلاف من ضحايا الحرب، بمن فيهم عدد كبير من الأطفال، يعانون من إصابات خطيرة ومغيرة للحياة. فقد الكثيرون أطرافهم وهم بحاجة ماسة إلى رعاية طبية متخصصة وأجهزة أطراف صناعية لاستعادة استقلالهم وكرامتهم.</p>

            <div class="emphasized-quote">
                "مهمتنا بسيطة: استعادة الكرامة والحركة. الطرف الصناعي ليس مجرد جهاز، بل هو طريق العودة إلى الحياة الطبيعية والعمل لمن فقد كل شيء."
            </div>
            
            <p>تبرعك يمول بشكل مباشر العمليات الجراحية الحيوية، ورعاية الصدمات، وإنتاج أطراف صناعية مصممة خصيصاً. نحن نعمل مع منظمات طبية موثوقة في الميدان لضمان وصول هذه المساعدة المتخصصة. **تبرع الآن لتكن جزءاً من رحلة الشفاء.**</p>
        </section>

        <section id="transparency">
            <h2>شفافية استخدام الأموال والمنظم</h2>
            
            <p style="font-weight: bold; margin-bottom: 10px;">كيف سيتم استخدام تبرعك:</p>
            <div class="fund-breakdown">
                <ul>
                    <li>**الأطراف الصناعية وإعادة التأهيل:** <span>60%</span></li>
                    <li>**الجراحات الطارئة ورعاية الصدمات:** <span>30%</span></li>
                    <li>**الإمدادات الطبية واللوجستيات:** <span>10%</span></li>
                </ul>
            </div>

            <p style="margin-top: 25px; font-weight: bold;">عن المنظم:</p>
            <div class="organizer-profile">
                <img src="https://via.placeholder.com/100x100?text=Organizer+Photo" alt="صورة المنظم">
                <div>
                    <h3>مبادرة الصحة العالمية (GHI)</h3>
                    <p style="color: #777;">منظمة إغاثة إنسانية موثقة</p>
                    <p>تعمل مبادرة الصحة العالمية (GHI) على تقديم الإغاثة الطبية في مناطق النزاع لأكثر من عقد. فريقنا يضم جراحين متخصصين وممرضين لضمان تقديم المساعدة المنقذة للحياة حيث تشتد الحاجة إليها. نحن ملتزمون بنشر تقارير مفصلة عن أوجه الصرف.</p>
                </div>
            </div>
        </section>

    </div>
</body>
</html>
