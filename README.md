# Agricilture-management-system
Agriculture Management System is a software-based application designed to help farmers manage farming activities efficiently. It provides information about crops, soil, fertilizers, irrigation, weather conditions, and market prices. 
Agriculture Management System – Project Description
An Agriculture Management System is a software application developed to help farmers manage and monitor agricultural activities efficiently. The main objective of this system is to improve farming productivity by using modern technology and providing useful information to farmers. It helps farmers manage crop details, soil conditions, fertilizers, irrigation, weather information, and market prices.

The system allows farmers to maintain records of different crops, including crop names, planting dates, harvesting schedules, and expected yields. It also provides information about suitable fertilizers, pesticides, and irrigation methods based on crop requirements. Farmers can use the system to monitor weather conditions, rainfall, and temperature to make better decisions about farming activities.

The Agriculture Management System can also include features such as farmer registration, login authentication, crop management, fertilizer management, equipment management, and sales management. An administrator can manage farmer details, update agricultural information, and monitor system activities.

By implementing this system, farmers can reduce manual paperwork, save time, minimize resource wastage, and improve crop production. It also helps farmers make informed decisions and adopt modern agricultural practices.
Main Features
1. Farmer Registration: Allows farmers to create accounts and manage their profiles.
2. Crop Management: Stores crop details, planting information, and harvesting schedules.
3. Soil Management: Provides information about soil types and soil conditions.
4. Fertilizer Management: Helps farmers select suitable fertilizers for different crops.
5. Irrigation Management: Provides information about watering schedules and irrigation methods.
6. Weather Information: Displays weather conditions to support farming decisions.
7. Equipment Management: Maintains details of agricultural tools and machinery.
8. Market Price Information: Helps farmers check crop prices in the market.
9. Admin Management: Allows administrators to manage farmers and agricultural records.
Objectives
- To improve agricultural productivity.
- To reduce manual work and paperwork.
- To provide useful farming information.
- To manage agricultural resources effectively.
- To support better crop planning and decision-making.
- To encourage the use of modern technology in agriculture.
Technologies Used
Component	Technology
Frontend	HTML, CSS, JavaScript
Backend	Python / PHP
Database	MySQL
Development Tool	VS Code
Platform	Web Application

Conclusion: The Agriculture Management System provides a simple and effective way to manage farming activities. It helps farmers access important agricultural information, improve productivity, reduce costs, and make agriculture more efficient through technology.

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Agriculture Management System</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: #f1f8e9;
    color: #333;
}

header {
    background: #2e7d32;
    color: white;
    padding: 20px;
    text-align: center;
}

nav {
    background: #1b5e20;
    padding: 15px;
    text-align: center;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 12px;
    font-weight: bold;
}

nav a:hover {
    color: #ffeb3b;
}

.container {
    padding: 25px;
}

h2 {
    color: #2e7d32;
    margin-bottom: 15px;
}

.dashboard {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-bottom: 30px;
}

.card {
    background: white;
    padding: 25px;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 3px 8px #ccc;
}

.card h3 {
    color: #388e3c;
    margin-bottom: 10px;
}

section {
    background: white;
    padding: 25px;
    margin-bottom: 25px;
    border-radius: 10px;
    box-shadow: 0 2px 6px #ddd;
}

input, select, button {
    padding: 10px;
    margin: 7px 3px;
    border: 1px solid #aaa;
    border-radius: 5px;
}

button {
    background: #2e7d32;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background: #1b5e20;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 15px;
}

th, td {
    border: 1px solid #ddd;
    padding: 12px;
    text-align: center;
}

th {
    background: #388e3c;
    color: white;
}

footer {
    background: #1b5e20;
    color: white;
    padding: 15px;
    text-align: center;
}

@media(max-width:600px) {
    nav a {
        display: inline-block;
        margin: 7px;
    }
    table {
        font-size: 12px;
    }
}
</style>
</head>

<body>

<header>
    <h1>🌾 Agriculture Management System</h1>
    <p>Smart Farming for Better Future</p>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#crops">Crops</a>
    <a href="#fertilizers">Fertilizers</a>
    <a href="#irrigation">Irrigation</a>
    <a href="#market">Market Prices</a>
</nav>

<div class="container">

<section id="home">
    <h2>Welcome to Agriculture Management System</h2>
    <p>
    This system helps farmers manage agricultural activities,
    monitor crops, maintain fertilizer records, manage irrigation
    and view crop market prices.
    </p>
</section>

<h2>Dashboard</h2>

<div class="dashboard">
    <div class="card">
        <h3>Total Crops</h3>
        <h1 id="cropCount">0</h1>
    </div>

    <div class="card">
        <h3>Fertilizers</h3>
        <h1>5</h1>
    </div>

    <div class="card">
        <h3>Irrigation</h3>
        <h1>Active</h1>
    </div>

    <div class="card">
        <h3>Farm Status</h3>
        <h1>Good</h1>
    </div>
</div>

<section id="crops">
    <h2>Crop Management</h2>

    <input type="text" id="cropName"
    placeholder="Enter crop name">

    <input type="text" id="season"
    placeholder="Enter season">

    <button onclick="addCrop()">Add Crop</button>

    <table>
        <thead>
            <tr>
                <th>Crop Name</th>
                <th>Season</th>
                <th>Action</th>
            </tr>
        </thead>
        <tbody id="cropTable"></tbody>
    </table>
</section>

<section id="fertilizers">
    <h2>Fertilizer Management</h2>

    <table>
        <tr>
            <th>Fertilizer</th>
            <th>Purpose</th>
        </tr>
        <tr>
            <td>Urea</td>
            <td>Nitrogen supply</td>
        </tr>
        <tr>
            <td>DAP</td>
            <td>Root development</td>
        </tr>
        <tr>
            <td>Potash</td>
            <td>Plant growth</td>
        </tr>
        <tr>
            <td>Compost</td>
            <td>Soil improvement</td>
        </tr>
        <tr>
            <td>Vermicompost</td>
            <td>Organic nutrients</td>
        </tr>
    </table>
</section>

<section id="irrigation">
    <h2>Irrigation Management</h2>

    <p>Select irrigation method:</p>

    <select id="irrigationType">
        <option value="Drip Irrigation">Drip Irrigation</option>
        <option value="Sprinkler Irrigation">Sprinkler Irrigation</option>
        <option value="Flood Irrigation">Flood Irrigation</option>
    </select>

    <button onclick="showIrrigation()">Submit</button>

    <p id="irrigationResult"></p>
</section>

<section id="market">
    <h2>Crop Market Information</h2>

    <table>
        <tr>
            <th>Crop</th>
            <th>Sample Price (per quintal)</th>
        </tr>
        <tr>
            <td>Rice</td>
            <td>₹2,369</td>
        </tr>
        <tr>
            <td>Wheat</td>
            <td>₹2,585</td>
        </tr>
        <tr>
            <td>Maize</td>
            <td>₹2,400</td>
        </tr>
        <tr>
            <td>Ragi</td>
            <td>₹4,886</td>
        </tr>
    </table>
    <small>Illustrative sample prices only, not live market rates.</small>
</section>

</div>

<footer>
    <p>© 2026 Agriculture Management System | Smart Farming</p>
</footer>

<script>
let cropCount = 0;

function addCrop() {
    let name = document.getElementById("cropName").value;
    let season = document.getElementById("season").value;

    if (name === "" || season === "") {
        alert("Please enter all crop details");
        return;
    }

    let table = document.getElementById("cropTable");
    let row = table.insertRow();

    row.insertCell(0).innerText = name;
    row.insertCell(1).innerText = season;

    let action = row.insertCell(2);
    let btn = document.createElement("button");
    btn.innerText = "Delete";

    btn.onclick = function() {
        row.remove();
        cropCount--;
        document.getElementById("cropCount").innerText = cropCount;
    };

    action.appendChild(btn);

    cropCount++;
    document.getElementById("cropCount").innerText = cropCount;

    document.getElementById("cropName").value = "";
    document.getElementById("season").value = "";
}

function showIrrigation() {
    let type = document.getElementById("irrigationType").value;

    document.getElementById("irrigationResult").innerText =
        "Selected Irrigation Method: " + type;
}
</script>

</body>
</html>
