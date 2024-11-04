<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>हरियाणा विवाह प्रमाण पत्र आवेदन</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>विवाह प्रमाण पत्र आवेदन</h1>
        <form id="marriageForm">
            <label for="husbandName">पति का नाम:</label>
            <input type="text" id="husbandName" required>

            <label for="wifeName">पत्नी का नाम:</label>
            <input type="text" id="wifeName" required>

            <label for="husbandId">पति का पहचान पत्र नंबर:</label>
            <input type="text" id="husbandId" required>

            <label for="wifeId">पत्नी का पहचान पत्र नंबर:</label>
            <input type="text" id="wifeId" required>

            <label for="addressProof">पता प्रमाण:</label>
            <input type="text" id="addressProof" required>

            <label for="witnesses">गवाहों के नाम (अलग-अलग नाम के लिए कॉमा से अलग करें):</label>
            <input type="text" id="witnesses" required>

            <button type="submit">आवेदन जमा करें</button>
        </form>

        <div id="response" class="response"></div>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 20px;
}

.container {
    max-width: 600px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
}

label {
    display: block;
    margin-top: 10px;
}

input {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    margin-top: 20px;
    padding: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

.response {
    margin-top: 20px;
    text-align: center;
    font-weight: bold;
}
document.getElementById('marriageForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const husbandName = document.getElementById('husbandName').value;
    const wifeName = document.getElementById('wifeName').value;
    const husbandId = document.getElementById('husbandId').value;
    const wifeId = document.getElementById('wifeId').value;
    const addressProof = document.getElementById('addressProof').value;
    const witnesses = document.getElementById('witnesses').value;

    const responseDiv = document.getElementById('response');
    responseDiv.innerHTML = `
        आवेदन सफलतापूर्वक जमा कर दिया गया है!<br>
        पति का नाम: ${husbandName}<br>
        पत्नी का नाम: ${wifeName}<br>
        पति का पहचान पत्र नंबर: ${husbandId}<br>
        पत्नी का पहचान पत्र नंबर: ${wifeId}<br>
        पता प्रमाण: ${addressProof}<br>
        गवाह: ${witnesses}
    `;
});

