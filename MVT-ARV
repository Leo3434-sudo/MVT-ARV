<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MVT ARV</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 100%;
            width: 100%;
            box-sizing: border-box;
            margin: 0 10px;
        }
        h1 {
            font-size: 24px;
            margin-bottom: 20px;
            text-align: center;
        }
        form {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        .form-group {
            width: 100%;
            margin-bottom: 15px;
            box-sizing: border-box;
        }
        .form-group.half-width {
            width: calc(50% - 10px);
        }
        label {
            margin-bottom: 5px;
            font-weight: bold;
            display: block;
        }
        input[type="text"],
        input[type="time"],
        input[type="number"],
        select {
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
            width: 100%;
            box-sizing: border-box;
        }
        button {
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
        }
        button:hover {
            background-color: #45a049;
        }
        textarea {
            width: calc(100% - 16px);
            resize: none;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
            box-sizing: border-box;
        }
        .output-container {
            margin-top: 20px;
            text-align: center;
        }
    </style>
    <script>
        function createMessage() {
            var flightNumber = document.getElementById('flightNumber').value;
            var reg = document.getElementById('reg').value || "RA73";
            var pp = document.getElementById('pp').value || "E2";
            var td = document.getElementById('td').value || "14:42";
            var ob = document.getElementById('ob').value || "15:02";
            var doTime = document.getElementById('doTime').value || "15:30";
            var paxC = document.getElementById('paxC').value;
            var paxY = document.getElementById('paxY').value;
            var paxINF = document.getElementById('paxINF').value;
            var paxINAD = document.getElementById('paxINAD').value;
            var bags = document.getElementById('bags').value || "N/A";
            var cgo = document.getElementById('cgo').value || "❌";
            var wch = document.getElementById('wch').value || "❌";
            var crewAssist = document.getElementById('crewAssist').value || "❌";

            var paxMessage = "PAX: ";
            if (paxC || paxY || paxINF || paxINAD) {
                if (paxC) paxMessage += paxC + "C+ ";
                if (paxY) paxMessage += paxY + "Y+ ";
                if (paxINF) paxMessage += paxINF + "INF+ ";
                if (paxINAD) paxMessage += paxINAD + "INAD ";
            } else {
                paxMessage += "N/A";
            }

            var today = new Date();
            var dd = String(today.getDate()).padStart(2, '0');
            var mm = today.toLocaleString('default', { month: 'short' }).toUpperCase();
            var formattedDate = dd + mm;

            var message =
                flightNumber + "/" + formattedDate + "/" + reg + "\n" +
                "PP " + pp + "\n" +
                "TD " + td + "\n" +
                "OB " + ob + "\n" +
                "DO " + doTime + "\n" +
                paxMessage + "\n" +
                "BAG " + bags + "\n" +
                "CGO " + cgo + "\n" +
                "WCH " + wch + "\n" +
                "CREW ASSIST " + crewAssist;

            document.getElementById('output').value = message;
        }

        function copyToClipboard() {
            var output = document.getElementById('output');
            output.select();
            output.setSelectionRange(0, 99999); // For mobile devices

            try {
                document.execCommand('copy');
                alert('Message copied to clipboard');
            } catch (err) {
                alert('Failed to copy message');
            }

            window.location.href = "https://chat.whatsapp.com/EXAJWqIDyk91zBHukgg020";
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>MVT ARV</h1>
        <form oninput="createMessage()">
            <div class="form-group full-width">
                <label for="flightNumber">Uçuş No:</label>
                <input type="text" id="flightNumber">
            </div>
            <div class="form-group half-width">
                <label for="reg">Reg:</label>
                <input type="text" id="reg" value="RA73">
            </div>
            <div class="form-group half-width">
                <label for="pp">PP:</label>
                <input type="text" id="pp" value="E2">
            </div>
            <div class="form-group half-width">
                <label for="td">TD:</label>
                <input type="time" id="td">
            </div>
            <div class="form-group half-width">
                <label for="ob">OB:</label>
                <input type="time" id="ob">
            </div>
            <div class="form-group half-width">
                <label for="doTime">DO:</label>
                <input type="time" id="doTime">
            </div>
            <div class="form-group full-width">
                <label for="paxC">PAX:</label>
                <input type="number" id="paxC" placeholder="C" style="width: 22%;">
                <input type="number" id="paxY" placeholder="Y" style="width: 22%;">
                <input type="number" id="paxINF" placeholder="INF" style="width: 22%;">
                <input type="number" id="paxINAD" placeholder="INAD" style="width: 22%;">
            </div>
            <div class="form-group half-width">
                <label for="bags">BAG:</label>
                <input type="text" id="bags" placeholder="PCS/KGS">
            </div>
            <div class="form-group half-width">
                <label for="cgo">CGO:</label>
                <input type="text" id="cgo" placeholder="PCS/KGS">
            </div>
            <div class="form-group half-width">
                <label for="wch">WCH:</label>
                <select id="wch">
                    <option value="❌">❌</option>
                    <option value="1️⃣">1️⃣</option>
                    <option value="2️⃣">2️⃣</option>
                    <option value="3️⃣">3️⃣</option>
                    <option value="4️⃣">4️⃣</option>
                    <option value="5️⃣">5️⃣</option>
                </select>
            </div>
            <div class="form-group half-width">
                <label for="crewAssist">CREW ASSIST:</label>
                <select id="crewAssist">
                    <option value="❌">❌</option>
                    <option value="✅">✅</option>
                </select>
            </div>
            <button type="button" onclick="copyToClipboard()">MVT'yi Kopyala, WhatsApp'ı Aç</button>
        </form>
        <div class="output-container">
            <h2>MVT ARV Ön İzleme</h2>
            <textarea id="output" rows="12"></textarea>
        </div>
    </div>
</body>
</html>