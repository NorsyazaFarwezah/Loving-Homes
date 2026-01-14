
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loving Homes - A Home Away From Home</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #8B7355; /* Brown */
            --secondary: #D2B48C; /* Light brown/Tan */
            --light: #F5F5DC; /* Beige */
            --dark: #654321; /* Dark brown */
            --success: #8FBC8F; /* Sage green */
            --gray: #A9A9A9; /* Gray */
            --light-gray: #E8E4D8; /* Light beige-gray */
            --white: #FFFFFF;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--white);
            overflow-x: hidden;
            width: 100%;
            max-width: 100%;
        }

        h1, h2, h3, h4, h5 {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
        }

        /* UPDATED: Full width container */
        .container {
            width: 100%;
            max-width: 1400px; /* Increased from 1200px */
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 60px 0;
            width: 100%;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            text-align: center;
        }

        .btn:hover {
            background-color: #7A6349;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }

        /* BACK BUTTON STYLES */
        .back-btn {
            display: inline-block;
            padding: 10px 24px;
            background-color: var(--secondary);
            color: var(--dark);
            border: none;
            border-radius: 4px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            text-align: center;
            margin: 20px 0;
            text-decoration: none;
        }

        .back-btn:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .back-btn i {
            margin-right: 8px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.2rem;
            color: var(--primary);
            position: relative;
            width: 100%;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* Header & Navigation */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
            width: 100%;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
            position: relative;
            width: 100%;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
            z-index: 1001;
        }

        .logo i {
            margin-right: 10px;
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
            font-size: 1rem;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .nav-links a.active {
            color: var(--secondary);
        }

        .nav-links a.active::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 2px;
            background-color: var(--secondary);
            bottom: -5px;
            left: 0;
        }

        .hamburger {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: var(--primary);
            z-index: 1001;
            background: none;
            border: none;
            padding: 5px;
        }

        /* Hero Section - UPDATED for full width */
        .hero {
            background: linear-gradient(rgba(139, 115, 85, 0.7), rgba(139, 115, 85, 0.7)), url('https://images.unsplash.com/photo-1543466835-00a7907e9de1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 120px 20px;
            width: 100%;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            max-width: 1200px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        /* Quick Links */
        .quick-links {
            background-color: var(--light);
            width: 100%;
        }

        .quick-links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            width: 100%;
        }

        .quick-link-card {
            background-color: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            text-align: center;
            padding: 30px 20px;
            border: 1px solid var(--light-gray);
            width: 100%;
        }

        .quick-link-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }

        .quick-link-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .quick-link-card h3 {
            font-size: 1.5rem;
            color: var(--dark);
        }

        /* Packages Section */
        .packages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            width: 100%;
        }

        .package-card {
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            background-color: var(--white);
            width: 100%;
        }

        .package-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }

        .package-header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
        }

        .package-header h3 {
            font-size: 1.8rem;
            margin-bottom: 5px;
        }

        .package-price {
            font-size: 2rem;
            font-weight: 700;
            margin: 15px 0;
        }

        .package-features {
            padding: 25px;
        }

        .package-features ul {
            margin-bottom: 25px;
        }

        .package-features li {
            padding: 8px 0;
            border-bottom: 1px solid var(--light-gray);
        }

        .package-features li:last-child {
            border-bottom: none;
        }

        .package-features li i {
            color: var(--success);
            margin-right: 10px;
        }

        /* Instagram Feed */
        .instagram-feed {
            background-color: var(--light);
            width: 100%;
        }

        .instagram-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            width: 100%;
        }

        .instagram-item {
            height: 200px;
            border-radius: 8px;
            overflow: hidden;
            border: 3px solid var(--white);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            background: linear-gradient(45deg, #405de6, #5851db, #833ab4, #c13584, #e1306c, #fd1d1d);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            padding: 20px;
        }

        .instagram-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.2));
        }

        .instagram-text {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            font-size: 1.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }

        .instagram-handle {
            font-size: 0.9rem;
            opacity: 0.9;
            margin-top: 5px;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 60px 0 30px;
            width: 100%;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
            width: 100%;
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--white);
        }

        .footer-links h4, .newsletter h4 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .footer-links ul li {
            margin-bottom: 10px;
        }

        .footer-links ul li a:hover {
            color: var(--secondary);
        }

        .newsletter-form {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .newsletter-form input {
            flex: 1;
            min-width: 200px;
            padding: 12px 15px;
            border: none;
            border-radius: 4px;
            background-color: rgba(255,255,255,0.9);
        }

        .newsletter-form .btn {
            background-color: var(--secondary);
            color: var(--dark);
        }

        .newsletter-form .btn:hover {
            background-color: var(--primary);
            color: white;
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: rgba(255,255,255,0.7);
        }

        /* Page Specific Styles */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            width: 100%;
        }

        .service-card {
            background-color: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            text-align: center;
            padding: 40px 25px;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 1px solid var(--light-gray);
            width: 100%;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .service-card i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .tour-section {
            background-color: var(--light);
            text-align: center;
            padding: 80px 20px;
            width: 100%;
        }

        .tour-section h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            color: var(--primary);
        }

        .tour-section p {
            max-width: 700px;
            margin: 0 auto 30px;
            font-size: 1.1rem;
        }

        /* About Page */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto 60px;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--primary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
        }

        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
        }

        .timeline-content {
            padding: 20px 30px;
            background-color: var(--white);
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border: 1px solid var(--light-gray);
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            right: -13px;
            background-color: var(--white);
            border: 4px solid var(--secondary);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }

        .timeline-item:nth-child(even)::after {
            left: -12px;
        }

        /* Facilities Section */
        .facilities-section {
            margin-bottom: 60px;
        }

        .facilities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
            width: 100%;
        }

        .facility-card {
            background-color: var(--white);
            border-radius: 8px;
            padding: 40px 25px;
            text-align: center;
            border: 1px solid var(--light-gray);
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            width: 100%;
        }

        .facility-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }

        .facility-card i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .facility-card h3 {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            width: 100%;
        }

        .value-card {
            text-align: center;
            padding: 30px 20px;
            background-color: var(--white);
            border-radius: 8px;
            border: 1px solid var(--light-gray);
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
        }

        .value-card i {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .value-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }

        /* Packages Page */
        .pricing-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
            width: 100%;
        }

        .package-builder {
            background-color: var(--light);
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            border: 1px solid var(--light-gray);
            width: 100%;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: 'Open Sans', sans-serif;
            background-color: var(--white);
        }

        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .form-row .form-group {
            flex: 1;
            min-width: 200px;
        }

        .add-ons {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }

        .add-on-item {
            background-color: var(--white);
            padding: 15px;
            border-radius: 4px;
            border: 1px solid #ddd;
            cursor: pointer;
            transition: all 0.3s;
        }

        .add-on-item:hover {
            border-color: var(--secondary);
            background-color: rgba(210, 180, 140, 0.05);
        }

        .add-on-item.selected {
            border-color: var(--secondary);
            background-color: rgba(210, 180, 140, 0.1);
        }

        .quote-result {
            margin-top: 30px;
            padding: 20px;
            background-color: var(--white);
            border-radius: 8px;
            display: none;
            border: 1px solid var(--light-gray);
        }

        .quote-result.show {
            display: block;
        }

        /* Contact Page */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
            width: 100%;
        }

        .contact-form .form-group {
            margin-bottom: 25px;
        }

        .contact-info {
            padding: 20px;
        }

        .contact-info-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }

        .contact-info-item i {
            font-size: 1.5rem;
            color: var(--primary);
            margin-right: 15px;
            width: 30px;
        }

        .map-container {
            height: 300px;
            border-radius: 8px;
            overflow: hidden;
            margin-bottom: 30px;
            background-color: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--light-gray);
            width: 100%;
        }

        /* Digital Map Styles */
        .digital-map {
            width: 100%;
            height: 100%;
            border: 0;
        }
        
        .map-placeholder {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 20px;
        }
        
        .map-placeholder i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .map-placeholder p {
            color: var(--dark);
            margin-bottom: 10px;
        }

        .hours-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }

        .hours-table tr {
            border-bottom: 1px solid #ddd;
        }

        .hours-table td {
            padding: 10px 0;
        }

        .hours-table td:last-child {
            text-align: right;
            font-weight: 600;
        }

        .faq-section {
            margin-top: 60px;
        }

        .faq-item {
            margin-bottom: 15px;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            overflow: hidden;
            background-color: var(--white);
        }

        .faq-question {
            padding: 20px;
            background-color: var(--light);
            font-weight: 600;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--primary);
        }

        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
        }

        .faq-item.active .faq-answer {
            padding: 20px;
            max-height: 500px;
        }

        .faq-item.active .faq-question i {
            transform: rotate(180deg);
        }

        /* Hide all pages except active one */
        .page {
            display: none;
            width: 100%;
        }
        
        .page.active {
            display: block;
        }

        /* Mobile Overlay */
        .mobile-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 998;
        }
        
        .mobile-overlay.active {
            display: block;
        }

        /* =========================
           FULL-WIDTH DESKTOP STYLES
           ========================= */
        
        @media (min-width: 1401px) {
            /* Remove max-width for very large screens */
            .container {
                max-width: 100%;
                padding: 0 40px;
            }
            
            .hero {
                padding: 150px 20px;
            }
            
            .hero h1 {
                font-size: 3.5rem;
                max-width: 1400px;
            }
            
            .packages-grid,
            .services-grid,
            .quick-links-grid,
            .pricing-cards,
            .facilities-grid {
                grid-template-columns: repeat(3, 1fr);
                max-width: 1400px;
                margin-left: auto;
                margin-right: auto;
            }
            
            .instagram-grid {
                grid-template-columns: repeat(5, 1fr);
                max-width: 1400px;
                margin-left: auto;
                margin-right: auto;
            }
            
            .values-grid {
                grid-template-columns: repeat(4, 1fr);
                max-width: 1400px;
                margin-left: auto;
                margin-right: auto;
            }
            
            /* Make sections more spacious */
            section {
                padding: 80px 0;
            }
        }

        /* =========================
           MOBILE RESPONSIVE STYLES
           ========================= */
        
        @media (max-width: 768px) {
            /* Mobile Navigation */
            .hamburger {
                display: block;
                position: relative;
                width: 30px;
                height: 30px;
            }
            
            .hamburger i {
                font-size: 1.8rem;
            }
            
            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: 80%;
                max-width: 320px;
                height: 100vh;
                background-color: var(--white);
                flex-direction: column;
                align-items: flex-start;
                justify-content: flex-start;
                padding-top: 100px;
                padding-left: 40px;
                transition: right 0.4s cubic-bezier(0.68, -0.55, 0.27, 1.55);
                box-shadow: -5px 0 25px rgba(0,0,0,0.15);
                z-index: 999;
                overflow-y: auto;
            }
            
            .nav-links.active {
                right: 0;
            }
            
            .nav-links li {
                margin: 0 0 25px 0;
                width: 100%;
            }
            
            .nav-links a {
                font-size: 1.3rem;
                padding: 10px 0;
                display: block;
                width: 100%;
                border-bottom: 1px solid rgba(139, 115, 85, 0.1);
            }
            
            .nav-links a.active::after {
                display: none;
            }
            
            .nav-links a.active {
                color: var(--primary);
                font-weight: 700;
            }
            
            /* Mobile Close Button */
            .mobile-close {
                position: absolute;
                top: 25px;
                right: 25px;
                font-size: 1.8rem;
                color: var(--primary);
                background: none;
                border: none;
                cursor: pointer;
                z-index: 1000;
            }
            
            /* Hero Section Mobile */
            .hero {
                padding: 80px 20px;
            }
            
            .hero h1 {
                font-size: 2rem;
                padding: 0 15px;
                line-height: 1.3;
            }
            
            .hero p {
                font-size: 1.1rem;
                padding: 0 15px;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
                gap: 15px;
                padding: 0 20px;
            }
            
            .hero-buttons .btn {
                width: 100%;
                max-width: 300px;
                margin-bottom: 10px;
            }
            
            /* Section Title Mobile */
            .section-title {
                font-size: 1.8rem;
                margin-bottom: 40px;
                padding: 0 15px;
            }
            
            .section-title::after {
                width: 60px;
                height: 3px;
                bottom: -8px;
            }
            
            /* Cards Mobile */
            .quick-links-grid,
            .packages-grid,
            .services-grid,
            .pricing-cards,
            .values-grid,
            .facilities-grid {
                grid-template-columns: 1fr;
                gap: 20px;
                padding: 0 10px;
            }
            
            .quick-link-card,
            .package-card,
            .service-card,
            .value-card,
            .facility-card {
                margin-bottom: 10px;
                padding: 25px 20px;
            }
            
            /* Instagram Grid Mobile */
            .instagram-grid {
                grid-template-columns: repeat(2, 1fr);
                padding: 0 15px;
            }
            
            .instagram-item {
                height: 150px;
                padding: 15px;
            }
            
            /* Package Builder Mobile */
            .package-builder {
                padding: 25px 20px;
                margin: 0 10px;
            }
            
            .form-row {
                flex-direction: column;
                gap: 15px;
            }
            
            .form-row .form-group {
                min-width: 100%;
            }
            
            .add-ons {
                grid-template-columns: 1fr;
            }
            
            /* Contact Page Mobile */
            .contact-container {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .contact-form,
            .contact-info {
                padding: 0 15px;
            }
            
            .map-container {
                height: 250px;
                margin: 0 15px 20px 15px;
            }
            
            /* Footer Mobile */
            .footer-content {
                grid-template-columns: 1fr;
                gap: 30px;
                padding: 0 20px;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .newsletter-form input {
                min-width: 100%;
                margin-bottom: 10px;
            }
            
            /* Timeline Mobile */
            .timeline {
                margin: 0 20px 60px;
            }
            
            /* FAQ Mobile */
            .faq-question {
                padding: 15px;
                font-size: 1rem;
            }
            
            .faq-answer {
                padding: 0 15px;
            }
            
            .faq-item.active .faq-answer {
                padding: 15px;
            }
            
            /* Button Sizing */
            .btn, .back-btn {
                padding: 12px 24px;
                font-size: 1rem;
            }
            
            /* Spacing */
            section {
                padding: 40px 0;
            }
            
            .tour-section {
                padding: 60px 20px;
            }
            
            .tour-section h2 {
                font-size: 1.8rem;
                padding: 0 15px;
            }
            
            .tour-section p {
                padding: 0 15px;
                font-size: 1rem;
            }
        }

        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item::after {
                left: 18px;
            }
            
            .timeline-item:nth-child(even)::after {
                left: 18px;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .logo {
                font-size: 1.5rem;
            }
            
            .package-header h3 {
                font-size: 1.5rem;
            }
            
            .package-price {
                font-size: 1.8rem;
            }
            
            .instagram-grid {
                grid-template-columns: 1fr;
            }
            
            .instagram-item {
                height: 180px;
            }
            
            .hours-table td {
                font-size: 0.9rem;
            }
            
            .btn, .back-btn {
                width: 100%;
                text-align: center;
            }
        }

        @media (max-width: 360px) {
            .hero h1 {
                font-size: 1.6rem;
            }
            
            .logo {
                font-size: 1.3rem;
            }
            
            .nav-links {
                width: 85%;
                padding-left: 30px;
            }
            
            .nav-links a {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
        }

        /* Touch Device Optimizations */
        @media (hover: none) and (pointer: coarse) {
            .quick-link-card:hover,
            .package-card:hover,
            .service-card:hover,
            .facility-card:hover {
                transform: none;
            }
            
            .btn:hover, .back-btn:hover {
                transform: none;
            }
            
            .add-on-item {
                min-height: 60px;
            }
            
            .nav-links a {
                padding: 15px 0;
            }
        }

        /* =========================
           WIDE SCREEN OPTIMIZATIONS
           ========================= */
        @media (min-width: 1600px) {
            .container {
                padding: 0 60px;
            }
            
            .hero h1 {
                font-size: 4rem;
                max-width: 1400px;
            }
            
            .hero p {
                font-size: 1.3rem;
                max-width: 800px;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
            
            .quick-link-card,
            .package-card,
            .service-card,
            .facility-card {
                padding: 40px 30px;
            }
            
            .quick-link-card i,
            .service-card i,
            .facility-card i {
                font-size: 3.5rem;
            }
            
            .quick-link-card h3,
            .service-card h3,
            .facility-card h3 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Mobile Overlay -->
    <div class="mobile-overlay" id="mobileOverlay"></div>
    
    <!-- Header & Navigation -->
    <header>
        <div class="container header-container">
            <a href="#home" class="logo" id="logo-link">
                <i class="fas fa-paw"></i> Loving Homes
            </a>
            
            <button class="hamburger" id="hamburger" aria-label="Toggle navigation">
                <i class="fas fa-bars"></i>
            </button>
            
            <ul class="nav-links" id="navLinks">
                <li><a href="#home" class="nav-link active" data-page="home">Home</a></li>
                <li><a href="#services" class="nav-link" data-page="services">Services</a></li>
                <li><a href="#packages" class="nav-link" data-page="packages">Packages</a></li>
                <li><a href="#about" class="nav-link" data-page="about">About</a></li>
                <li><a href="#contact" class="nav-link" data-page="contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Home Page -->
    <div id="home-page" class="page active">
        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <h1>A Home Away From Home</h1>
                <p>Providing loving, safe, and comfortable care for your pets while you're away. Our premium facilities and dedicated staff ensure your furry friends feel right at home.</p>
                <div class="hero-buttons">
                    <a href="#packages" class="btn">View Packages</a>
                    <a href="#contact" class="btn">Contact Us</a>
                </div>
            </div>
        </section>

        <!-- Quick Links -->
        <section class="quick-links">
            <div class="container">
                <h2 class="section-title">Our Services</h2>
                <div class="quick-links-grid">
                    <div class="quick-link-card">
                        <i class="fas fa-spa"></i>
                        <h3>Spa & Grooming</h3>
                        <p>Professional grooming services to keep your pet looking and feeling their best.</p>
                    </div>
                    <div class="quick-link-card">
                        <i class="fas fa-bed"></i>
                        <h3>Luxury Rooms</h3>
                        <p>Comfortable, spacious accommodations with cozy bedding and climate control.</p>
                    </div>
                    <div class="quick-link-card">
                        <i class="fas fa-walking"></i>
                        <h3>Daily Walks</h3>
                        <p>Regular exercise and playtime in our secure, outdoor play areas.</p>
                    </div>
                    <div class="quick-link-card">
                        <i class="fas fa-stethoscope"></i>
                        <h3>Vet On Call</h3>
                        <p>24/7 access to veterinary care for peace of mind during your pet's stay.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Package Highlights -->
        <section class="package-highlights">
            <div class="container">
                <h2 class="section-title">Package Highlights</h2>
                <div class="packages-grid">
                    <div class="package-card">
                        <div class="package-header">
                            <h3>Premium</h3>
                            <p>The Ultimate Experience</p>
                            <div class="package-price">$89<span>/night</span></div>
                        </div>
                        <div class="package-features">
                            <ul>
                                <li><i class="fas fa-check"></i> Luxury Suite Accommodation</li>
                                <li><i class="fas fa-check"></i> Daily Grooming Session</li>
                                <li><i class="fas fa-check"></i> 3 Daily Walks & Playtime</li>
                                <li><i class="fas fa-check"></i> Gourmet Meals</li>
                                <li><i class="fas fa-check"></i> Webcam Access</li>
                            </ul>
                            <a href="#packages" class="btn" style="width: 100%;">Select Plan</a>
                        </div>
                    </div>
                    <div class="package-card">
                        <div class="package-header">
                            <h3>Classic</h3>
                            <p>Comfort & Care</p>
                            <div class="package-price">$65<span>/night</span></div>
                        </div>
                        <div class="package-features">
                            <ul>
                                <li><i class="fas fa-check"></i> Standard Room Accommodation</li>
                                <li><i class="fas fa-check"></i> Weekly Grooming Session</li>
                                <li><i class="fas fa-check"></i> 2 Daily Walks & Playtime</li>
                                <li><i class="fas fa-check"></i> Premium Meals</li>
                                <li><i class="fas fa-check"></i> Daily Photo Updates</li>
                            </ul>
                            <a href="#packages" class="btn" style="width: 100%;">Select Plan</a>
                        </div>
                    </div>
                    <div class="package-card">
                        <div class="package-header">
                            <h3>Day Care</h3>
                            <p>Perfect for Day Trips</p>
                            <div class="package-price">$35<span>/day</span></div>
                        </div>
                        <div class="package-features">
                            <ul>
                                <li><i class="fas fa-check"></i> Play Area Access</li>
                                <li><i class="fas fa-check"></i> 2 Walks & Supervised Play</li>
                                <li><i class="fas fa-check"></i> Lunch & Treats Included</li>
                                <li><i class="fas fa-check"></i> Nap Time Accommodations</li>
                                <li><i class="fas fa-check"></i> Pickup/Dropoff Service Available</li>
                            </ul>
                            <a href="#packages" class="btn" style="width: 100%;">Select Plan</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Instagram Feed -->
        <section class="instagram-feed">
            <div class="container">
                <h2 class="section-title">Follow Us on Instagram</h2>
                <div class="instagram-grid">
                    <div class="instagram-item">
                        <i class="fab fa-instagram instagram-icon"></i>
                        <div class="instagram-text">@LovingHomesPets</div>
                        <div class="instagram-handle">Follow our daily adventures</div>
                    </div>
                    <div class="instagram-item">
                        <i class="fas fa-heart instagram-icon"></i>
                        <div class="instagram-text">Happy Pets</div>
                        <div class="instagram-handle">See their smiling faces</div>
                    </div>
                    <div class="instagram-item">
                        <i class="fas fa-camera instagram-icon"></i>
                        <div class="instagram-text">Daily Updates</div>
                        <div class="instagram-handle">Photos & videos daily</div>
                    </div>
                    <div class="instagram-item">
                        <i class="fas fa-paw instagram-icon"></i>
                        <div class="instagram-text">Behind the Scenes</div>
                        <div class="instagram-handle">See how we care</div>
                    </div>
                    <div class="instagram-item">
                        <i class="fas fa-star instagram-icon"></i>
                        <div class="instagram-text">Testimonials</div>
                        <div class="instagram-handle">Happy pet parents</div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Back Button for Home Page -->
        <div class="container" style="text-align: center; margin-top: 30px; margin-bottom: 30px;">
            <a href="#" class="back-btn" onclick="window.scrollTo(0, 0); return false;">
                <i class="fas fa-arrow-up"></i> Back to Top
            </a>
        </div>
    </div>

    <!-- Services Page -->
    <div id="services-page" class="page">
        <section class="services-main">
            <div class="container">
                <!-- Back Button -->
                <a href="#home" class="back-btn">
                    <i class="fas fa-arrow-left"></i> Back to Home
                </a>
                
                <h1 class="section-title">Our Services</h1>
                <div class="services-grid">
                    <div class="service-card">
                        <i class="fas fa-spa"></i>
                        <h3>Grooming</h3>
                        <p>Professional bathing, brushing, nail trimming, and styling to keep your pet looking and feeling their best.</p>
                    </div>
                    <div class="service-card">
                        <i class="fas fa-bed"></i>
                        <h3>Luxury Rooms</h3>
                        <p>Spacious, climate-controlled suites with comfortable bedding, toys, and relaxing music.</p>
                    </div>
                    <div class="service-card">
                        <i class="fas fa-stethoscope"></i>
                        <h3>Vet Services</h3>
                        <p>On-call veterinary care, medication administration, and regular health check-ups.</p>
                    </div>
                    <div class="service-card">
                        <i class="fas fa-car"></i>
                        <h3>Chauffeur Service</h3>
                        <p>Door-to-door pickup and drop-off service for your pet's convenience.</p>
                    </div>
                    <div class="service-card">
                        <i class="fas fa-tree"></i>
                        <h3>Paddocks</h3>
                        <p>Secure outdoor play areas with agility equipment and plenty of space to run.</p>
                    </div>
                    <div class="service-card">
                        <i class="fas fa-walking"></i>
                        <h3>Walks & Playtime</h3>
                        <p>Regular supervised walks and interactive play sessions to keep pets active and engaged.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="tour-section">
            <div class="container">
                <h2>See Our Facility For Yourself</h2>
                <p>Schedule a tour to meet our staff, see our accommodations, and learn more about how we care for your pets.</p>
                <a href="#contact" class="btn">Book a Tour</a>
            </div>
        </section>
        
        <!-- Back Button -->
        <div class="container" style="text-align: center; margin-top: 30px; margin-bottom: 30px;">
            <a href="#services" class="back-btn" onclick="window.scrollTo(0, 0); return false;">
                <i class="fas fa-arrow-up"></i> Back to Top
            </a>
        </div>
    </div>

    <!-- Packages Page -->
    <div id="packages-page" class="page">
        <section class="packages-main">
            <div class="container">
                <!-- Back Button -->
                <a href="#home" class="back-btn">
                    <i class="fas fa-arrow-left"></i> Back to Home
                </a>
                
                <h1 class="section-title">Our Packages</h1>
                
                <div class="pricing-cards">
                    <div class="package-card">
                        <div class="package-header">
                            <h3>Premium</h3>
                            <p>The Ultimate Experience</p>
                            <div class="package-price">$89<span>/night</span></div>
                        </div>
                        <div class="package-features">
                            <ul>
                                <li><i class="fas fa-check"></i> Luxury Suite Accommodation</li>
                                <li><i class="fas fa-check"></i> Daily Grooming Session</li>
                                <li><i class="fas fa-check"></i> 3 Daily Walks & Playtime</li>
                                <li><i class="fas fa-check"></i> Gourmet Meals</li>
                                <li><i class="fas fa-check"></i> Webcam Access</li>
                                <li><i class="fas fa-check"></i> Chauffeur Service Included</li>
                            </ul>
                            <button class="btn select-package" data-plan="premium" style="width: 100%;">Select Plan</button>
                        </div>
                    </div>
                    <div class="package-card">
                        <div class="package-header">
                            <h3>Classic</h3>
                            <p>Comfort & Care</p>
                            <div class="package-price">$65<span>/night</span></div>
                        </div>
                        <div class="package-features">
                            <ul>
                                <li><i class="fas fa-check"></i> Standard Room Accommodation</li>
                                <li><i class="fas fa-check"></i> Weekly Grooming Session</li>
                                <li><i class="fas fa-check"></i> 2 Daily Walks & Playtime</li>
                                <li><i class="fas fa-check"></i> Premium Meals</li>
                                <li><i class="fas fa-check"></i> Daily Photo Updates</li>
                                <li><i class="fas fa-check"></i> Vet On Call</li>
                            </ul>
                            <button class="btn select-package" data-plan="classic" style="width: 100%;">Select Plan</button>
                        </div>
                    </div>
                    <div class="package-card">
                        <div class="package-header">
                            <h3>Day Care</h3>
                            <p>Perfect for Day Trips</p>
                            <div class="package-price">$35<span>/day</span></div>
                        </div>
                        <div class="package-features">
                            <ul>
                                <li><i class="fas fa-check"></i> Play Area Access</li>
                                <li><i class="fas fa-check"></i> 2 Walks & Supervised Play</li>
                                <li><i class="fas fa-check"></i> Lunch & Treats Included</li>
                                <li><i class="fas fa-check"></i> Nap Time Accommodations</li>
                                <li><i class="fas fa-check"></i> Pickup/Dropoff Service Available</li>
                                <li><i class="fas fa-check"></i> Basic Grooming Add-on</li>
                            </ul>
                            <button class="btn select-package" data-plan="daycare" style="width: 100%;">Select Plan</button>
                        </div>
                    </div>
                </div>

                <h2 class="section-title">Custom Package Builder</h2>
                <div class="package-builder">
                    <form id="package-builder-form">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="nights">Number of Nights</label>
                                <select id="nights" class="form-control">
                                    <option value="1">1 Night</option>
                                    <option value="2">2 Nights</option>
                                    <option value="3">3 Nights</option>
                                    <option value="4">4 Nights</option>
                                    <option value="5">5 Nights</option>
                                    <option value="6">6 Nights</option>
                                    <option value="7">7 Nights</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="room-type">Room Type</label>
                                <select id="room-type" class="form-control">
                                    <option value="standard">Standard Room</option>
                                    <option value="deluxe">Deluxe Suite</option>
                                    <option value="luxury">Luxury Suite</option>
                                </select>
                            </div>
                        </div>
                        
                        <div class="form-group">
                            <label>Add-on Services</label>
                            <div class="add-ons">
                                <div class="add-on-item" data-service="grooming" data-price="25">
                                    <h4>Grooming Session</h4>
                                    <p>$25</p>
                                </div>
                                <div class="add-on-item" data-service="chauffeur" data-price="30">
                                    <h4>Chauffeur Service</h4>
                                    <p>$30</p>
                                </div>
                                <div class="add-on-item" data-service="training" data-price="40">
                                    <h4>Training Session</h4>
                                    <p>$40</p>
                                </div>
                                <div class="add-on-item" data-service="spa" data-price="35">
                                    <h4>Spa Treatment</h4>
                                    <p>$35</p>
                                </div>
                            </div>
                        </div>
                        
                        <button type="button" id="calculate-quote" class="btn">Get Quote</button>
                    </form>
                    
                    <div id="quote-result" class="quote-result">
                        <h3>Your Custom Quote</h3>
                        <p>Base Package: <span id="base-price">$0</span></p>
                        <p>Add-ons: <span id="addons-price">$0</span></p>
                        <h4>Total: $<span id="total-price">0</span></h4>
                        <a href="#contact" class="btn">Book Now</a>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Back Button -->
        <div class="container" style="text-align: center; margin-top: 30px; margin-bottom: 30px;">
            <a href="#packages" class="back-btn" onclick="window.scrollTo(0, 0); return false;">
                <i class="fas fa-arrow-up"></i> Back to Top
            </a>
        </div>
    </div>

    <!-- About Page -->
    <div id="about-page" class="page">
        <section class="about-main">
            <div class="container">
                <!-- Back Button -->
                <a href="#home" class="back-btn">
                    <i class="fas fa-arrow-left"></i> Back to Home
                </a>
                
                <h1 class="section-title">About Loving Homes</h1>
                
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>2010 - Founded</h3>
                            <p>Loving Homes was founded by Sarah Johnson, a lifelong animal lover with a vision to create a premium pet care facility that feels like home.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>2012 - First Expansion</h3>
                            <p>We expanded our facility to include luxury suites and added grooming services to our offerings.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>2015 - Award Winning</h3>
                            <p>Received "Best Pet Care Facility" award from the National Pet Care Association for our outstanding services and facilities.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>2018 - Vet Partnership</h3>
                            <p>Established partnership with local veterinary clinic to provide on-call medical care for all our guests.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>2022 - Major Renovation</h3>
                            <p>Completed a major renovation adding indoor play areas, a grooming spa, and expanding our outdoor facilities.</p>
                        </div>
                    </div>
                </div>

                <!-- Facilities Section -->
                <div class="facilities-section">
                    <h2 class="section-title">Our Facilities</h2>
                    <div class="facilities-grid">
                        <div class="facility-card">
                            <i class="fas fa-home"></i>
                            <h3>Luxury Suites</h3>
                            <p>Spacious, climate-controlled suites with comfortable bedding and soothing music</p>
                        </div>
                        <div class="facility-card">
                            <i class="fas fa-spa"></i>
                            <h3>Grooming Salon</h3>
                            <p>Professional grooming station with premium products and equipment</p>
                        </div>
                        <div class="facility-card">
                            <i class="fas fa-tree"></i>
                            <h3>Outdoor Play Areas</h3>
                            <p>Secure, fenced yards with agility equipment and plenty of space to run</p>
                        </div>
                        <div class="facility-card">
                            <i class="fas fa-heartbeat"></i>
                            <h3>Medical Center</h3>
                            <p>On-site medical facility with vet on call 24/7 for emergencies</p>
                        </div>
                        <div class="facility-card">
                            <i class="fas fa-utensils"></i>
                            <h3>Kitchen & Dining</h3>
                            <p>Commercial kitchen for preparing gourmet meals and special diets</p>
                        </div>
                        <div class="facility-card">
                            <i class="fas fa-camera"></i>
                            <h3>Webcam Areas</h3>
                            <p>Designated areas with webcams so you can check on your pet anytime</p>
                        </div>
                    </div>
                </div>

                <h2 class="section-title">Our Values</h2>
                <div class="values-grid">
                    <div class="value-card">
                        <i class="fas fa-heart"></i>
                        <h3>Compassion</h3>
                        <p>We treat every pet with the same love and care we would give our own family members.</p>
                    </div>
                    <div class="value-card">
                        <i class="fas fa-shield-alt"></i>
                        <h3>Safety</h3>
                        <p>Our facility is designed and staffed to ensure the highest levels of safety for all pets in our care.</p>
                    </div>
                    <div class="value-card">
                        <i class="fas fa-handshake"></i>
                        <h3>Trust</h3>
                        <p>We build lasting relationships with pet owners through transparency and reliable care.</p>
                    </div>
                    <div class="value-card">
                        <i class="fas fa-star"></i>
                        <h3>Excellence</h3>
                        <p>We continuously improve our services and facilities to provide the best possible experience.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Back Button -->
        <div class="container" style="text-align: center; margin-top: 30px; margin-bottom: 30px;">
            <a href="#about" class="back-btn" onclick="window.scrollTo(0, 0); return false;">
                <i class="fas fa-arrow-up"></i> Back to Top
            </a>
        </div>
    </div>

    <!-- Contact Page -->
    <div id="contact-page" class="page">
        <section class="contact-main">
            <div class="container">
                <!-- Back Button -->
                <a href="#home" class="back-btn">
                    <i class="fas fa-arrow-left"></i> Back to Home
                </a>
                
                <h1 class="section-title">Contact Us</h1>
                
                <div class="contact-container">
                    <div class="contact-form">
                        <form id="bookingForm" action="https://formspree.io/f/mlgdwpzj" method="POST">
                            <div class="form-group">
                                <label for="name">Full Name</label>
                                <input type="text" id="name" name="full_name" class="form-control" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="email">Email Address</label>
                                <input type="email" id="email" name="email" class="form-control" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="phone">Phone Number</label>
                                <input type="tel" id="phone" name="phone" class="form-control">
                            </div>
                            
                            <div class="form-group">
                                <label for="subject">Subject</label>
                                <select id="subject" name="subject" class="form-control">
                                    <option value="General Inquiry">General Inquiry</option>
                                    <option value="Booking Inquiry">Booking Inquiry</option>
                                    <option value="Schedule a Tour">Schedule a Tour</option>
                                    <option value="Service Questions">Service Questions</option>
                                    <option value="Other">Other</option>
                                </select>
                            </div>
                            
                            <div class="form-group">
                                <label for="message">Message</label>
                                <textarea id="message" name="message" class="form-control" rows="5" required></textarea>
                            </div>
                            
                            <button type="submit" class="btn">Send Message</button>
                        </form>
                    </div>
                    
                    <div class="contact-info">
                        <!-- Digital Location Map -->
                        <div class="map-container">
                            <iframe 
                                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3691.82783459556!2d114.15275531495416!3d22.284377485331302!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x340401323d6b6b9d%3A0x97462c787c1b381b!2sHong%20Kong!5e0!3m2!1sen!2shk!4v1647422345678!5m2!1sen!2shk" 
                                class="digital-map"
                                allowfullscreen="" 
                                loading="lazy"
                                title="Loving Homes Location">
                            </iframe>
                        </div>
                        
                        <div class="contact-info-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <h4>Address</h4>
                                <p>123 Pet Paradise Road<br>Hong Kong</p>
                            </div>
                        </div>
                        
                        <div class="contact-info-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <h4>Phone</h4>
                                <p>(555) 123-4567</p>
                            </div>
                        </div>
                        
                        <div class="contact-info-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <h4>Email</h4>
                                <p>info@lovinghomes.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-info-item">
                            <i class="fas fa-clock"></i>
                            <div>
                                <h4>Business Hours</h4>
                                <table class="hours-table">
                                    <tr>
                                        <td>Monday - Friday</td>
                                        <td>7:00 AM - 7:00 PM</td>
                                    </tr>
                                    <tr>
                                        <td>Saturday</td>
                                        <td>8:00 AM - 5:00 PM</td>
                                    </tr>
                                    <tr>
                                        <td>Sunday</td>
                                        <td>9:00 AM - 4:00 PM</td>
                                    </tr>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="faq-section">
                    <h2 class="section-title">Frequently Asked Questions</h2>
                    
                    <div class="faq-item">
                        <div class="faq-question">
                            <span>What vaccinations are required for my pet to stay?</span>
                            <i class="fas fa-chevron-down"></i>
                        </div>
                        <div class="faq-answer">
                            <p>We require proof of up-to-date vaccinations for Rabies, Distemper, and Bordetella (kennel cough). We also recommend flea and tick prevention.</p>
                        </div>
                    </div>
                    
                    <div class="faq-item">
                        <div class="faq-question">
                            <span>What should I bring for my pet's stay?</span>
                            <i class="fas fa-chevron-down"></i>
                        </div>
                        <div class="faq-answer">
                            <p>Please bring your pet's food, any medications, a favorite toy or blanket, and their leash. We provide beds, bowls, and toys, but familiar items from home can help your pet feel more comfortable.</p>
                        </div>
                    </div>
                    
                    <div class="faq-item">
                        <div class="faq-question">
                            <span>How often will I receive updates about my pet?</span>
                            <i class="fas fa-chevron-down"></i>
                        </div>
                        <div class="faq-answer">
                            <p>We provide daily photo and text updates for all our guests. For premium package guests, we offer webcam access so you can check in on your pet anytime.</p>
                        </div>
                    </div>
                    
                    <div class="faq-item">
                        <div class="faq-question">
                            <span>What happens if my pet gets sick during their stay?</span>
                            <i class="fas fa-chevron-down"></i>
                        </div>
                        <div class="faq-answer">
                            <p>We have a veterinarian on call 24/7 and will immediately contact you if there are any health concerns. If emergency care is needed, we will take your pet to our partner veterinary clinic.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Back Button -->
        <div class="container" style="text-align: center; margin-top: 30px; margin-bottom: 30px;">
            <a href="#contact" class="back-btn" onclick="window.scrollTo(0, 0); return false;">
                <i class="fas fa-arrow-up"></i> Back to Top
            </a>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">
                        <i class="fas fa-paw"></i> Loving Homes
                    </div>
                    <p>Providing loving, safe, and comfortable care for your pets while you're away. A home away from home for your furry family members.</p>
                </div>
                
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#packages">Packages</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div class="newsletter">
                    <h4>Newsletter</h4>
                    <p>Subscribe to get updates on special offers and pet care tips.</p>
                    <form class="newsletter-form" id="newsletterForm">
                        <input type="email" placeholder="Your email address" required>
                        <button type="submit" class="btn">Subscribe</button>
                    </form>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Loving Homes. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // DOM Elements
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        const mobileOverlay = document.getElementById('mobileOverlay');
        const navLinksItems = document.querySelectorAll('.nav-link');
        const pages = document.querySelectorAll('.page');
        const logoLink = document.getElementById('logo-link');

        // Mobile Navigation Toggle
        function toggleMobileMenu() {
            navLinks.classList.toggle('active');
            mobileOverlay.classList.toggle('active');
            document.body.style.overflow = navLinks.classList.contains('active') ? 'hidden' : '';
            
            // Toggle hamburger icon
            const icon = hamburger.querySelector('i');
            if (navLinks.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        }

        hamburger.addEventListener('click', toggleMobileMenu);
        mobileOverlay.addEventListener('click', toggleMobileMenu);

        // Close menu when clicking on a link
        navLinksItems.forEach(link => {
            link.addEventListener('click', () => {
                if (window.innerWidth <= 768) {
                    toggleMobileMenu();
                }
            });
        });

        // Function to show a specific page
        function showPage(pageId) {
            // Hide all pages
            pages.forEach(page => {
                page.classList.remove('active');
            });
            
            // Show the selected page
            document.getElementById(pageId + '-page').classList.add('active');
            
            // Update active nav link
            navLinksItems.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('data-page') === pageId) {
                    link.classList.add('active');
                }
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        // Navigation click handlers
        navLinksItems.forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const pageId = link.getAttribute('data-page');
                showPage(pageId);
                
                // Update URL hash
                window.location.hash = pageId;
            });
        });

        // Logo link handler
        logoLink.addEventListener('click', (e) => {
            e.preventDefault();
            showPage('home');
            window.location.hash = 'home';
        });

        // Handle URL hash on page load
        window.addEventListener('load', () => {
            const hash = window.location.hash.substring(1);
            if (hash && document.getElementById(hash + '-page')) {
                showPage(hash);
            } else {
                showPage('home');
            }
        });

        // Handle browser back/forward buttons
        window.addEventListener('hashchange', () => {
            const hash = window.location.hash.substring(1);
            if (hash && document.getElementById(hash + '-page')) {
                showPage(hash);
            }
        });

        // Package Builder Functionality
        const addOnItems = document.querySelectorAll('.add-on-item');
        const calculateBtn = document.getElementById('calculate-quote');
        const quoteResult = document.getElementById('quote-result');

        addOnItems.forEach(item => {
            item.addEventListener('click', function() {
                this.classList.toggle('selected');
            });
        });

        calculateBtn.addEventListener('click', function() {
            // Calculate base price based on nights and room type
            const nights = parseInt(document.getElementById('nights').value);
            const roomType = document.getElementById('room-type').value;
            
            let basePricePerNight = 65; // Default standard room
            
            if (roomType === 'deluxe') basePricePerNight = 75;
            if (roomType === 'luxury') basePricePerNight = 89;
            
            const basePrice = basePricePerNight * nights;
            
            // Calculate add-ons
            let addonsPrice = 0;
            document.querySelectorAll('.add-on-item.selected').forEach(item => {
                const price = parseInt(item.getAttribute('data-price'));
                addonsPrice += price;
            });
            
            // Calculate total
            const totalPrice = basePrice + addonsPrice;
            
            // Update display
            document.getElementById('base-price').textContent = `$${basePrice}`;
            document.getElementById('addons-price').textContent = `$${addonsPrice}`;
            document.getElementById('total-price').textContent = totalPrice;
            
            // Show result
            quoteResult.classList.add('show');
        });

        // Package Selection
        document.querySelectorAll('.select-package').forEach(button => {
            button.addEventListener('click', function() {
                const plan = this.getAttribute('data-plan');
                alert(`You've selected the ${plan} package! You can now proceed to book this package.`);
                // Show contact page for booking
                showPage('contact');
                window.location.hash = 'contact';
            });
        });

        // FAQ Accordion
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', function() {
                const item = this.parentElement;
                item.classList.toggle('active');
            });
        });

        // Newsletter Form Submission
        document.getElementById('newsletterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const email = this.querySelector('input').value;
            alert(`Thank you for subscribing with ${email}! You'll receive our next newsletter soon.`);
            this.reset();
        });

        // Booking Form Submission
        document.getElementById('bookingForm').addEventListener('submit', function(e) {
            // Form will submit to Formspree
            // You can add additional validation here if needed
            console.log('Form submitted to Formspree');
        });

        // Make all buttons with href attributes work
        document.querySelectorAll('a.btn[href^="#"], a.back-btn[href^="#"]').forEach(button => {
            button.addEventListener('click', function(e) {
                const href = this.getAttribute('href');
                if (href && href !== '#') {
                    const pageId = href.substring(1);
                    if (document.getElementById(pageId + '-page')) {
                        e.preventDefault();
                        showPage(pageId);
                        window.location.hash = pageId;
                    }
                }
            });
        });

        // Back button functionality for "Back to Top"
        document.querySelectorAll('.back-btn[href="#"]').forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });
        });

        // Touch device optimizations
        if ('ontouchstart' in window) {
            // Add touch feedback for interactive elements
            document.querySelectorAll('.btn, .add-on-item, .service-card, .quick-link-card, .back-btn').forEach(el => {
                el.style.cursor = 'pointer';
            });
        }

        // Close menu when clicking outside on mobile
        document.addEventListener('click', function(e) {
            if (window.innerWidth <= 768) {
                if (!navLinks.contains(e.target) && !hamburger.contains(e.target) && navLinks.classList.contains('active')) {
                    toggleMobileMenu();
                }
            }
        });

        // Handle window resize
        window.addEventListener('resize', function() {
            if (window.innerWidth > 768) {
                // Reset mobile menu on desktop
                navLinks.classList.remove('active');
                mobileOverlay.classList.remove('active');
                document.body.style.overflow = '';
                
                // Reset hamburger icon
                const icon = hamburger.querySelector('i');
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });

        // Add loading state for images
        document.querySelectorAll('img').forEach(img => {
            img.addEventListener('load', function() {
                this.style.opacity = '1';
            });
            img.style.opacity = '0';
            img.style.transition = 'opacity 0.3s ease';
        });
    </script>
</body>
</html>
