<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GeoJSON Fitness Maps</title>
    <!-- Leaflet CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
    <style>
        :root {
            --primary: #3498db;
            --secondary: #2c3e50;
            --accent: #e74c3c;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: #333;
        }
        header {
            background: var(--secondary);
            color: white;
            padding: 2rem 0;
            text-align: center;
            background: linear-gradient(135deg, var(--secondary) 0%, #1a252f 100%);
        }
        nav {
            background: var(--secondary);
            padding: 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            transition: all 0.3s;
            font-weight: 500;
            background: rgba(255,255,255,0.1);
        }
        nav a:hover {
            background: var(--primary);
            transform: translateY(-2px);
        }
        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 2rem;
        }
        .map-card {
            border: none;
            border-radius: 12px;
            overflow: hidden;
            margin-bottom: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            display: flex;
            background: white;
        }
        .map-card:hover {
            transform: translateY(-5px);
        }
        .map-preview {
            flex: 1;
            min-height: 200px;
            background-size: cover;
            background-position: center;
        }
        .map-info {
            flex: 2;
            padding: 2rem;
        }
        .map-info h3 {
            margin-top: 0;
            color: var(--secondary);
            font-size: 1.5rem;
        }
        .button {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 1rem;
            transition: all 0.3s;
        }
        .button:hover {
            background: #2980b9;
            box-shadow: 0 5px 15px rgba(41, 128, 185, 0.4);
        }
        footer {
            text-align: center;
            padding: 2rem;
            background: var(--secondary);
            color: white;
            margin-top: 3rem;
        }
        @media (max-width: 768px) {
            .map-card {
                flex-direction: column;
            }
            .map-preview {
                min-height: 150px;
            }
            nav ul {
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Outdoor Fitness Maps</h1>
        <p>Discover free workout locations in your city</p>
    </header>

    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="maps/splash-pads.html">Splash Pads</a></li>
            <li><a href="maps/outdoor-gyms.html">Outdoor Gyms</a></li>
            <li><a href="about.html">About This Project</a></li>
        </ul>
    </nav>

    <div class="container">
        <h2>Featured Fitness Locations</h2>
        
        <div class="map-card">
            <div class="map-preview" style="background-image: url('assets/splash-pads-preview.jpg');"></div>
            <div class="map-info">
                <h3><a href="maps/splash-pads.html">Cool Down at Splash Pads</a></h3>
                <p>Find the best water play areas to cool off after your workout. Our map shows all public splash pads with real-time status updates.</p>
                <a href="maps/splash-pads.html" class="button">Explore Splash Pads</a>
            </div>
        </div>

        <div class="map-card">
            <div class="map-preview" style="background-image: url('assets/outdoor-gym-preview.jpg');"></div>
            <div class="map-info">
                <h3><a href="maps/outdoor-gyms.html">Outdoor Gym Locations</a></h3>
                <p>Discover free outdoor fitness stations across the city. Filter by equipment type (calisthenics, cardio machines, etc.) and accessibility features.</p>
                <a href="maps/outdoor-gyms.html" class="button">Find Workout Spots</a>
            </div>
        </div>
    </div>

    <footer>
        <p>Made for fitness enthusiasts by <a href="https://github.com/yourusername" style="color: var(--primary);">Your Name</a></p>
        <p>Data last updated: <span id="update-date"></span></p>
        <script>
            document.getElementById('update-date').textContent = new Date().toLocaleDateString();
        </script>
    </footer>
</body>
</html>
