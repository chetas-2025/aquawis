# aquawise

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AquaWise - Smart Water Conservation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #e0f7fa;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #00796b;
            color: white;
            padding: 20px;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
            background-color: #004d40;
            overflow: hidden;
        }

        nav ul li {
            display: inline;
            padding: 15px;
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            cursor: pointer;
        }

        section {
            display: none;
            padding: 20px;
        }

        .active {
            display: block;
        }

        button {
            background-color: #00796b;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background-color: #004d40;
        }

        footer {
            background-color: #00796b;
            color: white;
            padding: 10px;
            margin-top: 20px;
        }

        section p {
            margin-bottom: 20px;
        }

        .tip-list {
            text-align: left;
            display: inline-block;
        }

        section img {
            width: 100%;
            max-width: 600px;
            height: auto;
            margin-top: 20px;
            border-radius: 8px;
        }
    </style>
</head>
<body>

<header>
    <h1>AquaWise</h1>
    <p>Smart AI Water Usage Guide</p>
</header>

<nav>
    <ul>
        <li><a onclick="showSection('home')">Home</a></li>
        <li><a onclick="showSection('usage')">Water Usage</a></li>
        <li><a onclick="showSection('calculator')">WaterWatch Calculator</a></li>
        <li><a onclick="showSection('tips')">Water-Saving Tips</a></li>
        <li><a onclick="showSection('conclusion')">Conclusion</a></li>
    </ul>
</nav>

<section id="home" class="active">
    <h2>Welcome to AquaWise</h2>
    <p>Water is one of our most valuable renewable resources, yet many households unknowingly waste more than they need. 
    AquaWise helps families understand their water usage and find ways to conserve it using AI-powered insights. This platform 
    provides personalized suggestions to ensure your water consumption is as efficient as possible.</p>
    <p>Our WaterWatch AI tool gives households the ability to track their water usage with precision, compare it with national averages, 
    and suggest targeted improvements based on real-time data.</p>
    <img src="images/water.png" alt="AquaWise Home Image">
</section>

<section id="usage">
    <h2>Understanding Household Water Usage</h2>
    <p>Household water usage is affected by a variety of factors. These include the number of people in the household, the number 
    of bathrooms, and the types of water-using appliances present. Understanding where the most water is used can help pinpoint 
    areas for conservation. Here’s a breakdown of key water usage contributors:</p>
    <div class="tip-list">
        <ul>
            <li><strong>Showers:</strong> The average person uses between 20-30 gallons of water per shower. Long showers waste water.</li>
            <li><strong>Toilets:</strong> Older toilets use up to 7 gallons per flush, while modern, water-efficient toilets use as little as 1.28 gallons.</li>
            <li><strong>Dishwashers:</strong> A dishwasher uses between 3-5 gallons per load, but energy-efficient models can save both water and electricity.</li>
            <li><strong>Washing Machines:</strong> A full load uses around 15-40 gallons per wash, with newer models being much more efficient.</li>
        </ul>
    </div>
    <p>Small changes can add up to substantial savings. Replacing old fixtures with water-saving ones or changing daily habits can 
    reduce household water use considerably.</p>
    <img src="images/consumption.png" alt="Household Water Usage">
</section>

<section id="calculator">
    <h2>WaterWatch AI Calculator</h2>
    <p>Use the WaterWatch AI tool to estimate your household’s water usage. The tool will calculate the ideal water consumption 
    based on your family size, bathroom count, and appliance usage, and compare it to your actual usage.</p>
    <p>The calculator will also show how your usage compares to other households in your state, so you can identify areas for improvement.</p>

    <label>Household Size:</label>
    <input type="number" id="householdSize">

    <label>Bathrooms:</label>
    <input type="number" id="bathrooms">

    <label>Showers:</label>
    <input type="number" id="showers">

    <label>Dishwashers:</label>
    <input type="number" id="dishwashers">

    <label>Monthly Water Usage (Gallons):</label>
    <input type="number" id="actualUsage">

    <label for="state">Select your state:</label>
    <select id="state">
        <option value="Alabama" data-usage="7200">Alabama</option>
        <option value="Alaska" data-usage="6500">Alaska</option>
        <option value="Arizona" data-usage="7500">Arizona</option>
        <option value="Arkansas" data-usage="7100">Arkansas</option>
        <!-- Add more states as necessary -->
    </select>

    <button onclick="calculateWaterUsage()">Analyze Usage</button>

    <div id="result"></div>
    <img src="images/waterwatch.png" alt="WaterWatch Calculator">
</section>

<section id="tips">
    <h2>AI-Driven Water-Saving Tips</h2>
    <p>Our AI-powered tips will help you identify practical and effective ways to reduce water waste. These tips are tailored to 
    your household’s usage patterns, aiming to optimize water consumption in areas where it matters most.</p>

    <div class="tip-list">
        <ul>
            <li><strong>Install Water-Efficient Fixtures:</strong> Replacing old faucets, showerheads, and toilets with WaterSense-labeled products can save thousands of gallons annually.</li>
            <li><strong>Fix Leaks:</strong> Leaking faucets and toilets can waste hundreds of gallons of water per year. Repairing leaks as soon as they occur is crucial for conservation.</li>
            <li><strong>Shorten Showers:</strong> Reducing shower time can save up to 2.5 gallons of water per minute. Consider using a timer to help manage shower durations.</li>
            <li><strong>Run Full Loads:</strong> Dishwashers and washing machines should only be run with full loads to maximize water efficiency. Avoid partial washes.</li>
            <li><strong>Water Lawns Smartly:</strong> Water lawns early in the morning or late in the evening to minimize evaporation. Adjust your sprinklers to avoid overwatering.</li>
            <li><strong>Upgrade Appliances:</strong> Use ENERGY STAR-rated dishwashers, washing machines, and water heaters to reduce both water and energy consumption.</li>
        </ul>
    </div>
    <p>These tips will not only reduce your water usage but also save you money on utility bills. By taking simple, mindful steps, 
    you can contribute to a more sustainable future.</p>
    <img src="images/tips.png" alt="Water-Saving Tips">
</section>

<section id="conclusion">
    <h2>Conclusion & Next Steps</h2>
    <p>AquaWise, with its AI-powered WaterWatch calculator, provides users with smart data-driven insights to optimize water usage. 
    By leveraging AI for leak detection, efficient watering schedules, and appliance use, AquaWise helps users conserve water, reduce waste, and promote sustainable habits.</p>
    
    <h3>Next Steps:</h3>
    <p>✅ Gather user feedback to improve accuracy</p>
    <p>✅ Expand features for more detailed analysis</p>
    <p>✅ Form partnerships with sustainability organizations</p>
    <p>✅ Engage the community in water conservation education</p>
    <p>✅ Regularly update the AI model with new data to provide real-time insights and trends.</p>
    <img src="images/save.jpg" alt="AquaWise Conclusion">
</section>

<footer>
    <p>&copy; 2025 AquaWise | Smart Water Conservation</p>
</footer>

<script>
    function showSection(sectionId) {
        let sections = document.querySelectorAll("section");
        sections.forEach(section => section.classList.remove("active"));
        document.getElementById(sectionId).classList.add("active");
    }

    function calculateWaterUsage() {
        let householdSize = document.getElementById("householdSize").value;
        let bathrooms = document.getElementById("bathrooms").value;
        let showers = document.getElementById("showers").value;
        let dishwashers = document.getElementById("dishwashers").value;
        let actualUsage = document.getElementById("actualUsage").value;
        let state = document.getElementById("state").value;
        let stateUsage = document.getElementById("state").selectedOptions[0].dataset.usage;

        if (!householdSize || !bathrooms || !showers || !dishwashers || !actualUsage) {
            alert("Please fill in all fields.");
            return;
        }

        let idealUsage = (householdSize * 1000) + (bathrooms * 500) + (showers * 400) + (dishwashers * 300);

        let resultText = `<h4>Analysis Results</h4>`;
        resultText += `<p><strong>Ideal Water Usage:</strong> ${idealUsage.toFixed(2)} gallons/month</p>`;
        resultText += `<p><strong>Actual Water Usage:</strong> ${actualUsage} gallons/month</p>`;
        resultText += `<p><strong>Average Usage in ${state}:</strong> ${stateUsage} gallons/month</p>`;

        document.getElementById("result").innerHTML = resultText;
    }
</script>

</body>
</html>

