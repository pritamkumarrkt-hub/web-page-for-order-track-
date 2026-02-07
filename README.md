# web-page-for-order-track-
so here i wrote a amazon type order page using html and css. i also use Ai for this project .
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; /* Cleaner font stack */
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

.delivery-header {
    background-color: #232f3e; /* Amazon Dark Blue */
    color: white;
    text-align: center;
    padding: 20px;
}

/* Main Card Container */
.order-details {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    overflow: hidden; /* Fix: Ensures child elements don't spill out of rounded corners */
}

/* Fix: Added padding for the top text section */
.order-info {
    padding: 20px;
    border-bottom: 1px solid #eee;
}

/* Fix: The Flexbox Layout */
.map-container {
    display: flex;
    flex-direction: row; /* Side-by-side on Desktop */
    min-height: 400px;   /* Changed height to min-height to avoid overflow */
}

.driver-info {
    flex: 0 0 30%;      /* Fix: Driver info takes exactly 30% width */
    padding: 20px;
    background-color: #fafafa;
    border-right: 1px solid #eee; /* Visual divider */
    box-sizing: border-box; /* Ensures padding doesn't affect width */
}

/* Fix: Image Handling */
.map-container img {
    flex: 1;            /* Fix: Image takes the remaining 70% space */
    width: 100%;        /* Fills its own container */
    height: 100%;       /* Fills height */
    object-fit: cover;  /* Fix: Crops image instead of stretching it */
    display: block;     /* Removes tiny white space under images */
}

.delivery-footer {
    text-align: center;
    padding: 20px;
    background-color: #232f3e;
    color: white;
    font-size: 14px;
    margin-top: 40px;
}

/* NEW: Mobile Responsiveness */
@media (max-width: 768px) {
    .map-container {
        flex-direction: column; /* Stack vertically on phones */
    }

    .driver-info {
        flex: auto;       /* Reset width */
        width: 100%;
        border-right: none;
        border-bottom: 1px solid #eee;
    }

    .map-container img {
        height: 250px;    /* Smaller map height for mobile */
    }
}    
and here is html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Delivery Tracker - Amazon Style</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="delivery-header">
        <div class="container">
            <h1>Your Order Tracking</h1>
            <p>Track your delivery in real-time.</p>
        </div>
    </header>

    <main class="container">
        <section class="tracking-stepper">
            <div class="step completed">
                <div class="circle">✓</div>
                <p>Ordered</p>
            </div>
            <div class="step completed">
                <div class="circle">✓</div>
                <p>Shipped</p>
            </div>
            <div class="step active">
                <div class="circle">3</div>
                <p>Out for Delivery</p>
            </div>
            <div class="step">
                <div class="circle">4</div>
                <p>Arriving</p>
            </div>
        </section>

        <section class="order-grid">
            <div class="order-info card">
                <h2>Order #12345</h2>
                <hr>
                <p><strong>Placed:</strong> Feb 7, 2026, 10:00 AM</p>
                <p><strong>Estimated Delivery:</strong> Today by 8:00 PM</p>
                <div class="driver-info">
                    <h3>Driver: John Doe</h3>
                    <p>Vehicle: Silver Sedan</p>
                </div>
            </div>

            <div class="map-container card">
                <div class="map-placeholder">
                    <img src="https://via.placeholder.com/600x400?text=Map+Location+of+Driver" alt="Delivery Map" class="map-img">
                </div>
            </div>
        </section>
    </main>

    <footer class="delivery-footer">
        <p>&copy; 2026 Delivery Tracker - Amazon Inspired</p>
    </footer>

</body>
</html>
 
