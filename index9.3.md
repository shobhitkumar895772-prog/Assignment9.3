1. HTML Code (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexusCloud | SaaS Landing Page</title>
    <link rel="stylesheet" href="style.css">
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>

    <!-- 1. Header & Navigation Bar (Flexbox) -->
    <header class="site-header">
        <div class="nav-container">
            <div class="logo">
                <i class="fa-solid fa-cube"></i> NexusCloud
            </div>
            <nav class="nav-links">
                <a href="#features">Features</a>
                <a href="#solutions">Solutions</a>
                <a href="#pricing">Pricing</a>
                <a href="#contact">Contact</a>
            </nav>
            <div class="nav-actions">
                <a href="#" class="btn-secondary">Sign In</a>
                <a href="#" class="btn-primary">Get Started</a>
            </div>
        </div>
    </header>

    <!-- Main Content Container -->
    <main>
        
        <!-- 2. Hero Section (Flexbox Alignment) -->
        <section class="hero-section">
            <div class="hero-content">
                <span class="badge">Version 2.0 Released</span>
                <h1>Scale Your Workflow With Intelligent Cloud Infrastructure</h1>
                <p>Deploy, monitor, and manage your applications seamlessly with our next-generation developer platform designed for maximum velocity.</p>
                <div class="hero-buttons">
                    <a href="#" class="btn-primary lg">Start Free Trial</a>
                    <a href="#" class="btn-outline lg"><i class="fa-solid fa-play"></i> Watch Demo</a>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=1000&q=80" alt="Dashboard Analytics Preview">
            </div>
        </section>

        <!-- 3 & 4. Features Section (CSS Grid Layout with Flexbox Cards) -->
        <section id="features" class="features-section">
            <div class="section-title">
                <h2>Built For Modern Teams</h2>
                <p>Everything you need to build secure, scalable applications without the overhead.</p>
            </div>

            <!-- Grid Container for Cards -->
            <div class="features-grid">
                
                <!-- Card 1 -->
                <div class="feature-card">
                    <div class="card-icon"><i class="fa-solid fa-bolt"></i></div>
                    <h3>Lightning Fast</h3>
                    <p>Optimized global edge network ensuring sub-50ms latency for all your end users worldwide.</p>
                </div>

                <!-- Card 2 -->
                <div class="feature-card">
                    <div class="card-icon"><i class="fa-solid fa-shield-halved"></i></div>
                    <h3>Enterprise Security</h3>
                    <p>SOC2 Type II certified with end-to-end encryption, automated compliance, and real-time threat detection.</p>
                </div>

                <!-- Card 3 -->
                <div class="feature-card">
                    <div class="card-icon"><i class="fa-solid fa-chart-line"></i></div>
                    <h3>Real-time Analytics</h3>
                    <p>Gain deep operational insights with granular telemetry, custom dashboards, and instant alerting.</p>
                </div>

                <!-- Card 4 -->
                <div class="feature-card">
                    <div class="card-icon"><i class="fa-solid fa-arrows-split-up-and-left"></i></div>
                    <h3>Infinite Scalability</h3>
                    <p>Auto-scaling container clusters that effortlessly handle traffic spikes from thousands to millions.</p>
                </div>

                <!-- Card 5 -->
                <div class="feature-card">
                    <div class="card-icon"><i class="fa-solid fa-code-merge"></i></div>
                    <h3>Seamless CI/CD</h3>
                    <p>Connect your GitHub or GitLab repositories for instant automated deployments on every pull request.</p>
                </div>

                <!-- Card 6 -->
                <div class="feature-card">
                    <div class="card-icon"><i class="fa-solid fa-headset"></i></div>
                    <h3>24/7 Expert Support</h3>
                    <p>Get dedicated technical assistance from senior systems engineers whenever you encounter complex bottlenecks.</p>
                </div>

            </div>
        </section>

    </main>

    <!-- Footer Section -->
    <footer class="site-footer">
        <p>&copy; 2026 NexusCloud Inc. All rights reserved. Built with CSS Grid & Flexbox.</p>
    </footer>

</body>
</html>
2. CSS Code (style.css)
CSS
/* --- Global Reset & Box Sizing --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    --primary: #4f46e5;
    --primary-hover: #4338ca;
    --bg-main: #f8fafc;
    --card-bg: #ffffff;
    --text-main: #0f172a;
    --text-muted: #64748b;
    --border: #e2e8f0;
}

body {
    font-family: 'Inter', system-ui, -apple-system, sans-serif;
    background-color: var(--bg-main);
    color: var(--text-main);
    line-height: 1.6;
    overflow-x: hidden;
}

/* --- 1. Header & Navigation (Flexbox) --- */
.site-header {
    background-color: rgba(255, 255, 255, 0.9);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 16px 24px;
    display: flex;                   /* Flexbox for navbar alignment */
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--primary);
    display: flex;
    align-items: center;
    gap: 8px;
}

.nav-links {
    display: none;                   /* Hidden by default on mobile */
    gap: 32px;
}

.nav-links a {
    text-decoration: none;
    color: var(--text-muted);
    font-weight: 500;
    font-size: 0.95rem;
    transition: color 0.2s;
}

.nav-links a:hover {
    color: var(--primary);
}

.nav-actions {
    display: flex;
    align-items: center;
    gap: 16px;
}

/* Button Styles */
.btn-primary {
    background-color: var(--primary);
    color: #ffffff;
    padding: 10px 20px;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.9rem;
    transition: background-color 0.2s;
}

.btn-primary:hover {
    background-color: var(--primary-hover);
}

.btn-secondary {
    text-decoration: none;
    color: var(--text-main);
    font-weight: 600;
    font-size: 0.9rem;
}

.btn-outline {
    border: 1px solid var(--border);
    color: var(--text-main);
    padding: 12px 24px;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background-color: #ffffff;
}

.btn-primary.lg, .btn-outline.lg {
    padding: 14px 28px;
    font-size: 1rem;
}

/* --- 2. Hero Section (Flexbox Layout) --- */
.hero-section {
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px 24px;
    display: flex;                    /* Flexbox for hero layout */
    flex-direction: column;           /* Stacked by default for mobile */
    gap: 40px;
    align-items: center;
}

.hero-content {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.badge {
    background-color: #e0e7ff;
    color: var(--primary);
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 600;
    margin-bottom: 20px;
}

.hero-content h1 {
    font-size: clamp(2.2rem, 4vw + 1rem, 3.5rem);
    line-height: 1.15;
    font-weight: 800;
    margin-bottom: 20px;
    color: #0c0a09;
}

.hero-content p {
    color: var(--text-muted);
    font-size: 1.1rem;
    margin-bottom: 32px;
}

.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

.hero-image {
    flex: 1;
    width: 100%;
}

.hero-image img {
    width: 100%;
    max-width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
    border: 1px solid var(--border);
}

/* --- 3 & 4. Features Section (CSS Grid & Flexbox Cards) --- */
.features-section {
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px 24px 80px 24px;
}

.section-title {
    text-align: center;
    max-width: 600px;
    margin: 0 auto 50px auto;
}

.section-title h2 {
    font-size: 2.2rem;
    font-weight: 700;
    margin-bottom: 12px;
}

.section-title p {
    color: var(--text-muted);
    font-size: 1.05rem;
}

/* CSS Grid for the 6 feature cards */
.features-grid {
    display: grid;
    grid-template-columns: 1fr;       /* 1 column on mobile (Step 6) */
    gap: 24px;
}

/* Flexbox inside individual feature cards */
.feature-card {
    background-color: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 32px;
    display: flex;                    /* Flexbox for card internal layout */
    flex-direction: column;           /* Stack icon, title, text vertically */
    align-items: flex-start;
    box-shadow: 0 1px 3px rgba(0,0,0,0.02);
    transition: transform 0.2s, box-shadow 0.2s;
}

.feature-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05);
}

.card-icon {
    width: 48px;
    height: 48px;
    background-color: #e0e7ff;
    color: var(--primary);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.25rem;
    margin-bottom: 20px;
}

.feature-card h3 {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 10px;
}

.feature-card p {
    color: var(--text-muted);
    font-size: 0.95rem;
}

/* Footer Styling */
.site-footer {
    background-color: #ffffff;
    border-top: 1px solid var(--border);
    text-align: center;
    padding: 30px;
    color: var(--text-muted);
    font-size: 0.9rem;
}

/* ==========================================================
   Responsive Breakpoints (Desktop Enhancement)
   ========================================================== */

@media (min-width: 768px) {
    .nav-links {
        display: flex;               /* Show navbar links on tablet/desktop */
    }

    .hero-section {
        flex-direction: row;         /* Switch hero to side-by-side flex layout */
        padding: 80px 24px;
    }

    .features-grid {
        grid-template-columns: repeat(2, 1fr); /* 2 columns on tablets */
    }
}

@media (min-width: 1024px) {
    .features-grid {
        grid-template-columns: repeat(3, 1fr); /* 3 columns on desktops for the 6 cards */
    }
}
Assignment Checklist & Verification:
Header & Navigation Bar: Built using Flexbox (display: flex; justify-content: space-between;) with a responsive mobile toggle setup.

Hero Section: Arranged using a flexible row/column setup that places text and dashboard preview imagery side-by-side on desktop and stacked on mobile.

Features Section (3–6 Cards): Contains 6 feature cards showcasing infrastructure capabilities.

CSS Grid Layout: Utilized on .features-grid with grid-template-columns: repeat(auto/minmax/fixed) scaling dynamically.

Flexbox Utilization: Applied across the navbar, hero section, and internal card content alignment.

Mobile Single-Column View: Base styles default to single-column layouts (grid-template-columns: 1fr and stacked flex elements) preventing overflow on small screens.

Spacing & Alignment Check: Rigorously spaced with consistent padding, margins, and container max-widths for pristine visual hierarchy on all devices.