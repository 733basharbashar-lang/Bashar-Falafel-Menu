<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>طعمية وفلافل بشار التميمي 👑 - قائمة الطلبات</title>
    
    <style>
        /* (الجزء الخاص بـ CSS - تصميم وشكل القائمة) */
        body {
            direction: rtl; 
            font-family: Tahoma, Geneva, sans-serif;
            background-color: #f4f4f4; 
            padding: 20px;
            margin: 0;
            line-height: 1.6;
        }

        h1 {
            color: #CC0000; 
            text-align: center;
            border-bottom: 2px solid #FF7F50; 
            padding-bottom: 10px;
            margin-bottom: 30px;
        }

        p {
            margin: 5px 0;
        }

        ul {
            list-style-type: none; 
            padding: 0;
        }

        li {
            background-color: white;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1); 
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .item-details {
            flex-grow: 1; 
        }

        .item-details h2 {
            margin-top: 0;
            color: #333;
        }

        .item-price {
            font-weight: bold;
            color: #008000;
            font-size: 1.1em;
            margin-top: 5px;
        }

        /* --- تصميم أزرار التحكم بالكمية --- */
        .quantity-control {
            display: flex;
            align-items: center;
            gap: 10px; 
        }
        
        .quantity-control button {
            background-color: #4CAF50; 
            color: white;
            border: none;
            padding: 8px 15px;
            text-align: center;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
            width: 40px; 
        }

        .quantity-control button:hover {
            background-color: #45a049;
        }
        
        .item-quantity {
            font-weight: bold;
            font-size: 1.2em;
            width: 25px; 
            text-align: center;
        }

        .summary {
            background-color: #fff;
            padding: 20px;
            margin-top: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            text-align: center;
        }

        .summary h3 {
            color: #CC0000; 
            font-size: 1.5em;
            margin-bottom: 15px;
        }
        
        .free-item-note {
            text-align: center; 
            color: #1a701a; 
            font-weight: bold;
            margin-bottom: 20px;
        }
        
        /* تصميم زر الواتساب */
        #whatsapp-button {
            background-color: #25D366; 
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
            width: 100%;
            margin-top: 15px;
            transition: background-color 0.3s;
        }

        #whatsapp-button:hover {
            background-color: #1DA851;
        }

        #whatsapp-button:disabled {
            background-color: #ccc;
            cursor: not-allowed;
        }
    </style>
</head>

<body>
    
    <h1>طعمية وفلافل بشار التميمي 👑</h1>
    <p style="text-align: center; font-size: 1.1em;">أهلاً بك يا زبون! تفضل باختيار طلبك:</p>
    
    <p class="free-item-note">✅ الصوص الحار متوفر مجاناً عند الطلب!</p>
    
    <ul id="menu-items">
        <li data-item-id="1" data-item-name="بطاطس مقرمشة" data-price="300">
            <div class="item-details">
                <h2>بطاطس مقرمشة</h2>
                <p class="item-price">السعر: 300 ريال يمني</p>
            </div>
            <div class="quantity-control">
                <button class="quantity-minus" data-id="1">-</button>
                <span class="item-quantity" id="qty-1">0</span>
                <button class="quantity-plus" data-id="1">+</button>
            </div>
        </li>
        
        <li data-item-id="2" data-item-name="ساندويتش فلافل" data-price="300">
            <div class="item-details">
                <h2>ساندويتش فلافل (طعمية)</h2>
                <p class="item-price">السعر: 300 ريال يمني</p>
            </div>
            <div class="quantity-control">
                <button class="quantity-minus" data-id="2">-</button>
                <span class="item-quantity" id="qty-2">0</span>
                <button class="quantity-plus" data-id="2">+</button>
            </div>
        </li>
        
        <li data-item-id="3" data-item-name="وجبة خاصة (بطاطس وفلافل)" data-price="600">
            <div class="item-details">
                <h2>وجبة خاصة (بطاطس وفلافل)</h2>
                <p class="item-price">السعر: 600 ريال يمني</p>
            </div>
            <div class="quantity-control">
                <button class="quantity-minus" data-id="3">-</button>
                <span class="item-quantity" id="qty-3">0</span>
                <button class="quantity-plus" data-id="3">+</button>
            </div>
        </li>
        
        <li data-item-id="4" data-item-name="إضافة صوص حار" data-price="0">
            <div class="item-details">
                <h2>هل تطلب صوص حار؟ (مجاني)</h2>
                <p class="item-price">مجاني</p>
            </div>
            <div class="quantity-control">
                <button class="quantity-minus" data-id="4">-</button>
                <span class="item-quantity" id="qty-4">0</span>
                <button class="quantity-plus" data-id="4">+</button>
            </div>
        </li>
    </ul>
    
    <div class="summary">
        <h3 id="total-display">إجمالي الطلب: 0 ريال يمني</h3>
        
        <button id="whatsapp-button" disabled>أرسل الطلب الآن (واتساب)</button>
    </div>


    <script>
        // (الجزء الخاص بـ JavaScript - المنطق والوظائف)
        let cart = {}; 
        let totalPrice = 0; 
        
        const totalDisplay = document.getElementById('total-display');
        const whatsappButton = document.getElementById('whatsapp-button');
        const menuItems = document.querySelectorAll('#menu-items li');

        // الرقم الخاص بك يا بشار التميمي 
        const YOUR_WHATSAPP_NUMBER = "967733971941"; 
        
        // تفاصيل الدفع 
        const PAYMENT_DETAILS = 
            `\n---\n*طرق الدفع المتاحة:*\n` +
            `* 💵 نقداً عند الاستلام (العربة).\n` +
            `* 📱 خدمة حاسب (رمز الدفع: 1466204) على الرقم 967733971941.`;


        menuItems.forEach(item => {
            const itemId = item.getAttribute('data-item-id');
            cart[itemId] = 0;
        });

        function updateOrderSummary() {
            totalPrice = 0;
            let totalItems = 0;
            
            menuItems.forEach(item => {
                const itemId = item.getAttribute('data-item-id');
                const itemPrice = parseInt(item.getAttribute('data-price'));
                const quantity = cart[itemId];
                
                totalPrice += quantity * itemPrice;
                totalItems += quantity;

                document.getElementById(`qty-${itemId}`).textContent = quantity;
            });

            totalDisplay.textContent = `إجمالي الطلب: ${totalPrice} ريال يمني`;
            
            whatsappButton.disabled = totalItems === 0;
        }


        // دالة تعديل الكمية (مع التأكد من أن الصوص الحار لا يزيد عن 1)
        function changeQuantity(itemId, action) {
            let currentQty = cart[itemId];
            const isHotSauce = itemId === '4'; 

            if (action === 'plus') {
                // إذا كان صوص حار وكميته 1، لا تزد العدد
                if (isHotSauce && currentQty >= 1) {
                    return; 
                }
                cart[itemId] = currentQty + 1;
            } else if (action === 'minus' && currentQty > 0) {
                cart[itemId] = currentQty - 1;
            }
            
            updateOrderSummary();
        }

        // ربط الأزرار
        document.querySelectorAll('.quantity-plus').forEach(button => {
            button.addEventListener('click', () => {
                const itemId = button.getAttribute('data-id');
                changeQuantity(itemId, 'plus');
            });
        });

        document.querySelectorAll('.quantity-minus').forEach(button => {
            button.addEventListener('click', () => {
                const itemId = button.getAttribute('data-id');
                changeQuantity(itemId, 'minus');
            });
        });

        
        // دالة إرسال الطلب عبر الواتساب 
        whatsappButton.addEventListener('click', () => {
            let itemsList = [];
            
            menuItems.forEach(item => {
                const itemId = item.getAttribute('data-item-id');
                const itemName = item.getAttribute('data-item-name');
                const quantity = cart[itemId];
                
                if (quantity > 0) {
                    itemsList.push(`(${quantity}x) ${itemName}`);
                }
            });
            
            const itemsListText = itemsList.join('\n');
            
            const whatsappMessage = 
                `*طلب جديد من عربة بشار التميمي* 👑\n\n` +
                `*قائمة الطلبات:*\n${itemsListText}\n\n` +
                `*الإجمالي النهائي:* ${totalPrice} ريال يمني\n` +
                PAYMENT_DETAILS + 
                `\n---\n` + 
                `*شكراً لاختيارك طعمية وفلافل بشار التميمي!*`; 

            const encodedMessage = encodeURIComponent(whatsappMessage);
            
            const whatsappUrl = `whatsapp://send?phone=${YOUR_WHATSAPP_NUMBER}&text=${encodedMessage}`;
            
            window.open(whatsappUrl, '_system');
        });
        
    </script>
    
</body>
</html>
