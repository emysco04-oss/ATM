<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Isabel's Premium ATM</title>
    <style>
        body { background: #1a1a1a; color: #ff85a2; font-family: 'Courier New', monospace; display: flex; align-items: center; justify-content: center; height: 100vh; margin: 0; }
        #atm-screen { background: #2d2d2d; border: 5px solid #ff85a2; border-radius: 20px; padding: 30px; width: 320px; box-shadow: 0 0 20px #ff85a2; text-align: center; }
        .balance { font-size: 2rem; margin: 20px 0; color: #00ff41; text-shadow: 0 0 5px #00ff41; }
        .btn-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        button { background: transparent; border: 1px solid #ff85a2; color: #ff85a2; padding: 10px; cursor: pointer; border-radius: 5px; font-size: 0.8rem; }
        button:hover { background: #ff85a2; color: white; }
        #message { margin-top: 20px; font-weight: bold; min-height: 40px; }
    </style>
</head>
<body>

    <div id="atm-screen">
        <h3>ISABEL CORP. ATM</h3>
        <p>Current Debt to Supplier:</p>
        <div class="balance">800,000 DOLS</div>
        
        <div class="btn-grid">
            <button onclick="update('Withdraw 1 Smile')">WITHDRAW SMILE</button>
            <button onclick="update('Withdraw 1 Voice Note')">VOICE NOTE (LOCK)</button>
            <button onclick="update('Pay 1 Hug')">PAY 1 HUG</button>
            <button onclick="update('Mystery Gift')">SURPRISE</button>
        </div>

        <div id="message">Please select a transaction...</div>
    </div>

    <script>
        function update(type) {
            const msg = document.getElementById('message');
            if(type === 'Withdraw 1 Smile') {
                msg.innerText = "Transaction Successful: You just made me smile back through the screen. 😊";
            } else if (type === 'Withdraw 1 Voice Note') {
                msg.innerText = "Error: Voice notes cost 800k dols. Please insert more Joy to unlock. 🎙️";
            } else if (type === 'Pay 1 Hug') {
                msg.innerText = "HUG RECEIVED. Processing... Connection feels warmer now. ❤️";
            } else {
                msg.innerText = "SURPRISE: Check your WhatsApp for a 'Mi Lady' appreciation text. ✨";
            }
        }
    </script>
</body>
</html>
