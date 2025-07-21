# K-DAIRY-FRESH-STOCK-TRACKER-
For president 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>K DAIRY FRESH - Stock Dashboard</title>
    <link rel="stylesheet" href="style.css">
    </head>
<body>
    <div class="header">
        <h1>K DAIRY FRESH Stock Tracker</h1>
        <nav>
            <ul>
                <li><a href="index.html" class="active">Dashboard</a></li>
                <li><a href="current_stock.html">Current Stock</a></li>
                <li><a href="add_stock.html">Add New Stock</a></li>
                <li><a href="sales_records.html">Sales Records</a></li>
                <li><a href="reports.html">Reports</a></li>
            </ul>
        </nav>
    </div>

    <div class="container">
        <div class="dashboard-grid">
            <div class="card summary-card">
                <h2>Overall Stock Summary</h2>
                <p><strong>Total Items in Stock:</strong> <span id="totalItems">540</span></p>
                <p><strong>Total Value of Stock:</strong> KES <span id="totalValue">1,250,000</span></p>
                <p><strong>Items Low on Stock:</strong> <span id="lowStockItems">12</span></p>
            </div>

            <div class="card quick-links">
                <h2>Quick Actions</h2>
                <ul>
                    <li><a href="add_stock.html">Add New Dairy Product</a></li>
                    <li><a href="sales_records.html">Record a Sale</a></li>
                    <li><a href="current_stock.html?filter=low">View Low Stock Items</a></li>
                    <li><a href="reports.html?type=daily">Generate Daily Report</a></li>
                </ul>
            </div>

            <div class="card recent-activity">
                <h2>Recent Activity</h2>
                <div class="activity-list">
                    <p><strong>05/07/2025:</strong> 50L Milk added to stock.</p>
                    <p><strong>04/07/2025:</strong> 20 Kgs Yogurt sold.</p>
                    <p><strong>04/07/2025:</strong> 10 Kgs Cheese received from supplier.</p>
                    <p><strong>03/07/2025:</strong> Low stock alert: Fresh Cream.</p>
                </div>
            </div>

            <div class="card alerts-warnings">
                <h2>Alerts & Warnings</h2>
                <p class="alert low-stock-alert"><strong>Low Stock:</strong> Milk (50L packs), Fresh Cream (1L packs)</p>
                <p class="alert expiring-soon"><strong>Expiring Soon:</strong> Yogurt (10 Kgs, 2 days left)</p>
                </div>

            <div class="card key-metrics">
                <h2>Key Metrics (Past 7 Days)</h2>
                <p><strong>Sales Revenue:</strong> KES <span id="weeklySales">150,000</span></p>
                <p><strong>Items Sold:</strong> <span id="weeklyItemsSold">180</span></p>
                <p><strong>New Stock Added:</strong> <span id="weeklyNewStock">120</span> items</p>
            </div>

            </div>
    </div>

    <div class="footer">
        <p>&copy; 2025 K DAIRY FRESH. All rights reserved.</p>
    </div>

    <script src="script.js"></script>
</body>
</html>
<//* General Body and Container Styles */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f8f4; /* Lighter green tint */
    color: #333;
    line-height: 1.6;
}

.container {
    max-width: 1200px;
    margin: 20px auto;
    padding: 0 20px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
}

/* Header Styles */
header {
    background-color: #3cb371; /* Medium Sea Green */
    color: white;
    padding: 25px 0;
    text-align: center;
    border-bottom-left-radius: 15px;
    border-bottom-right-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

header h1 {
    margin: 0;
    font-size: 2.5em;
    letter-spacing: 1px;
}

header p {
    font-size: 1.1em;
    opacity: 0.9;
}

/* Navigation Styles */
nav {
    display: flex;
    justify-content: center;
    background-color: #e0ffe0; /* Very light green */
    padding: 12px;
    border-radius: 10px;
    margin: 20px auto;
    max-width: 800px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

nav a {
    text-decoration: none;
    color: #2e8b57; /* Sea Green */
    padding: 10px 20px;
    margin: 0 8px;
    border-radius: 6px;
    transition: background-color 0.3s ease, color 0.3s ease;
    font-weight: bold;
}

nav a:hover, nav a.active {
    background-color: #90ee90; /* Light Green */
    color: #1e5c3e;
}

/* Feature Card Styles */
.feature-card {
    background-color: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
    transition: transform 0.2s ease-in-out;
}

.feature-card:hover {
    transform: translateY(-5px);
}

.feature-card h2 {
    color: #2e8b57; /* Sea Green */
    margin-top: 0;
    border-bottom: 2px solid #90ee90;
    padding-bottom: 10px;
    margin-bottom: 20px;
}

/* Form Styles */
form label {
    display: block;
    margin-bottom: 8px;
    font-weight: bold;
    color: #555;
}

form input[type="text"],
form input[type="number"],
form input[type="date"],
form select,
form textarea {
    width: calc(100% - 22px); /* Account for padding and border */
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 1em;
    box-sizing: border-box; /* Include padding and border in the element's total width and height */
}

form textarea {
    resize: vertical;
    min-height: 80px;
}

/* Button Styles */
button {
    background-color: #32cd32; /* Lime Green */
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 1.1em;
    font-weight: bold;
    transition: background-color 0.3s ease, transform 0.2s ease;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

button:hover {
    background-color: #228b22; /* Forest Green */
    transform: translateY(-2px);
}

/* Notification Specific Styles */
.notification-item {
    background-color: #fffacd; /* Lemon Chiffon */
    border-left: 6px solid #ff7f50; /* Coral */
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 6px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.notification-item.dismissed {
    opacity: 0.6;
    text-decoration: line-through;
    font-style: italic;
    background-color: #f8f8f8;
    border-left-color: #ccc;
}

.dismiss-btn {
    background-color: #ff6347; /* Tomato Red */
    color: white;
    border: none;
    padding: 5px 10px;
    border-radius: 4px;
    cursor: pointer;
    font-size: 0.9em;
    transition: background-color 0.2s ease;
}

.dismiss-btn:hover {
    background-color: #cc4c3a;
}

/* Record Entry Styles */
.record-entry {
    background-color: #f9fdf9; /* Very light green */
    border: 1px solid #e0ffe0;
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 8px;
    box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.03);
}

.record-entry strong {
    color: #2e8b57;
}

.record-entry p {
    margin: 5px 0;
}

/* Utility / List Styles */
ul {
    list-style: none;
    padding: 0;
}

ul li {
    background-color: #f5fff5;
    border-bottom: 1px dashed #e0ffe0;
    padding: 8px 0;
}

ul li:last-child {
    border-bottom: none;
}

/* Footer Styles */
footer {
    text-align: center;
    margin-top: 50px;
    padding: 25px;
    background-color: #3cb371;
    color: white;
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;
    box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.1);
}

footer p {
    margin: 5px 0;
}

/* Responsive Design (basic) */
@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }
    nav {
        flex-direction: column;
        align-items: center;
    }
    nav a {
        margin: 5px 0;
        width: 80%; /* Make navigation links full width */
        text-align: body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f4f7f6;
    color: #333;
}

.header {
    background-color: #4CAF50; /* K DAIRY FRESH green */
    color: white;
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
}

.header h1 {
    margin: 0;
    font-size: 1.8em;
}

.header nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}

.header nav li {
    margin-left: 20px;
}

.header nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    padding: 5px 10px;
    border-radius: 4px;
    transition: background-color 0.3s ease;
}

.header nav a:hover,
.header nav a.active {
    background-color: #45a049;
}

.container {
    max-width: 1200px;
    margin: 20px auto;
    padding: 0 20px;
}

.dashboard-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
}

.card {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.card h2 {
    color: #4CAF50;
    margin-top: 0;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
    margin-bottom: 15px;
}

/* Specific card styles */
.summary-card p {
    font-size: 1.1em;
    margin: 8px 0;
}

.quick-links ul {
    list-style: none;
    padding: 0;
}

.quick-links li {
    margin-bottom: 10px;
}

.quick-links a {
    display: block;
    background-color: #007BFF; /* Blue for quick actions */
    color: white;
    padding: 10px 15px;
    text-decoration: none;
    border-radius: 5px;
    text-align: center;
    transition: background-color 0.3s ease;
}

.quick-links a:hover {
    background-color: #0056b3;
}

.recent-activity .activity-list p {
    background-color: #f9f9f9;
    padding: 10px;
    border-left: 3px solid #ccc;
    margin-bottom: 8px;
    font-size: 0.95em;
}

.alerts-warnings .alert {
    padding: 10px;
    border-radius: 5px;
    margin-bottom: 10px;
    font-weight: bold;
}

.low-stock-alert {
    background-color: #ffe0b2; /* Light orange */
    color: #e65100; /* Dark orange */
    border-left: 5px solid #ff9800;
}

.expiring-soon {
    background-color: #ffcdd2; /* Light red */
    color: #d32f2f; /* Dark red */
    border-left: 5px solid #f44336;
}

.key-metrics p {
    font-size: 1.1em;
    margin: 8px 0;
}

.footer {
    text-align: center;
    padding: 20px;
    margin-top: 30px;
    background-color: #333;
    color: white;
    font-size: 0.9em;
}



