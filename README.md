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
