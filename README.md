# my-gardening-app
Public 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Garden Pro | My Business</title>
    <style>
        /* DESIGN (CSS) */
        :root {
            --primary-green: #2e7d32;
            --light-green: #e8f5e9;
            --dark-green: #1b5e20;
            --white: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--light-green);
            color: #333;
        }

        header {
            background-color: var(--primary-green);
            color: var(--white);
            padding: 40px 20px;
            text-align: center;
            border-bottom-left-radius: 30px;
            border-bottom-right-radius: 30px;
        }

        .container {
            padding: 20px;
            max-width: 600px;
            margin: auto;
        }

        h2 {
            color: var(--dark-green);
            border-left: 5px solid var(--primary-green);
            padding-left: 10px;
        }

        /* Services Styling */
        .card {
            background: var(--white);
            padding: 15px;
            border-radius: 15px;
            margin-bottom: 15px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        /* Gallery Styling */
        .gallery {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .gallery-item {
            background: #ddd;
            height: 150px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            color: #666;
            background-size: cover;
            background-position: center;
        }

        /* Form Styling */
        form {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        input, select, button {
            padding: 15px;
            border-radius: 10px;
            border: 1px solid #ccc;
            font-size: 1rem;
        }

        button {
            background-color: var(--primary-green);
            color: white;
            font-weight: bold;
            border: none;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            background-color: var(--dark-green);
        }

        footer {
            text-align: center;
            padding: 40px;
            font-size: 0.9rem;
            color: #777;
        }
    </style>
</head>
<body>

    <header>
        <h1>🌿 My Gardening Pro</h1>
        <p>Quality lawn care by a local entrepreneur!</p>
    </header>

    <div class="container">
        
        <!-- SERVICE SECTION -->
        <section>
            <h2>My Services</h2>
            <div class="card">
                <strong>🌱 Basic Mow:</strong> £15 - £25
            </div>
            <div class="card">
                <strong>🍂 Leaf Raking:</strong> £10 per bag
            </div>
            <div class="card">
                <strong>✂️ Hedge Trimming:</strong> From £20
            </div>
        </section>

        <!-- GALLERY SECTION -->
        <section>
            <h2>My Work</h2>
            <div class="gallery">
                <!-- Replace the URLs below with your own photos later! -->
                <div class="gallery-item" style="background-image: url('https://via.placeholder.com/200?text=Fresh+Lawn')">Lawn 1</div>
                <div class="gallery-item" style="background-image: url('https://via.placeholder.com/200?text=Hedges')">Hedges</div>
                <div class="gallery-item" style="background-image: url('https://via.placeholder.com/200?text=Garden+Clear')">Cleanup</div>
                <div class="gallery-item" style="background-image: url('https://via.placeholder.com/200?text=Before+and+After')">Transformation</div>
            </div>
        </section>

        <!-- BOOKING SECTION -->
        <section>
            <h2>Book a Service</h2>
            <div class="card">
                <form id="bookingForm">
                    <input type="text" id="custName" placeholder="Your Name" required>
                    <input type="tel" id="custPhone" placeholder="Your Phone Number" required>
                    <select id="serviceType">
                        <option value="Mowing">Lawn Mowing</option>
                        <option value="Raking">Leaf Raking</option>
                        <option value="Hedges">Hedge Trimming</option>
                    </select>
                    <button type="submit">Send Booking Request</button>
                </form>
            </div>
        </section>

    </div>

    <footer>
        <p>&copy; 2024 My Gardening Business</p>
    </footer>

    <!-- LOGIC (JavaScript) -->
    <script>
        document.getElementById('bookingForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const name = document.getElementById('custName').value;
            const service = document.getElementById('serviceType').value;
            
            // This displays a success message
            alert("Success! Thanks " + name + ", I have received your request for " + service + ". I will call you shortly!");
            
            // Clears the form
            this.reset();
        });
    </script>

</body>
</html>