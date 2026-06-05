<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>einstenium | profile</title>
    
    <!-- Google Fonts: Space Grotesk for sleek text, Playfair Display for elegant philosophy -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,600&family=Space+Grotesk:wght@300;400;600;700&display=swap" rel="stylesheet">

    <style>
        /* Modern CSS reset and variables */
        :root {
            --bg-color: #050505;
            --card-bg: rgba(15, 15, 15, 0.65);
            --card-border: rgba(255, 255, 255, 0.08);
            --text-primary: #ffffff;
            --text-secondary: #a1a1aa;
            --accent-glow: rgba(147, 51, 234, 0.15); /* Purple accent */
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Space Grotesk', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-primary);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* Ambient background lights (Guns.lol vibe) */
        body::before, body::after {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: var(--accent-glow);
            filter: blur(120px);
            z-index: 0;
            pointer-events: none;
        }

        body::before {
            top: 20%;
            left: 20%;
        }

        body::after {
            bottom: 20%;
            right: 20%;
        }

        /* Main glassmorphism profile card */
        .profile-card {
            position: relative;
            z-index: 1;
            width: 100%;
            max-width: 440px;
            padding: 40px 30px;
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 24px;
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            text-align: center;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
            animation: cardEntrance 1s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        /* Elegant image wrapper with glowing border */
        .avatar-container {
            position: relative;
            width: 110px;
            height: 110px;
            margin: 0 auto 25px auto;
        }

        .avatar-container::after {
            content: '';
            position: absolute;
            top: -3px;
            left: -3px;
            right: -3px;
            bottom: -3px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(255,255,255,0.2), rgba(255,255,255,0.02));
            z-index: -1;
        }

        .profile-image {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid #111;
            box-shadow: 0 8px 24px rgba(0,0,0,0.5);
        }

        /* Title styling */
        .username {
            font-size: 1.8rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            margin-bottom: 12px;
            color: var(--text-primary);
        }

        /* The philosophical quote */
        .philosophical-quote {
            font-family: 'Playfair Display', serif;
            font-size: 1.05rem;
            font-style: italic;
            line-height: 1.6;
            color: var(--text-secondary);
            margin-bottom: 30px;
            padding: 0 10px;
        }

        /* Discord Button with icon and hover transitions */
        .discord-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            width: 100%;
            padding: 16px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 12px;
            color: var(--text-primary);
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
            cursor: pointer;
        }

        .discord-btn svg {
            width: 20px;
            height: 20px;
            fill: currentColor;
            transition: transform 0.3s ease;
        }

        .discord-btn:hover {
            background: var(--text-primary);
            color: var(--bg-color);
            border-color: var(--text-primary);
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.15);
            transform: translateY(-2px);
        }

        .discord-btn:hover svg {
            transform: scale(1.1);
        }

        /* Subtle subtle animation on page load */
        @keyframes cardEntrance {
            from {
                opacity: 0;
                transform: translateY(30px) scale(0.98);
            }
            to {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        /* Small screen handling */
        @media (max-width: 480px) {
            body {
                padding: 20px;
            }
            .profile-card {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>

    <div class="profile-card">
        <!-- Visual Profile Area using the requested image verbatim -->
        <div class="avatar-container">
            <img src="93481932.webp" alt="einstenium image" class="profile-image">
        </div>

        <!-- Name -->
        <h1 class="username">einstenium</h1>

        <!-- Philosophical quote -->
        <p class="philosophical-quote">
            "We dance for laughter, we dance for tears, we dance for madness, we dance for fears, we are the creators of the dream."
        </p>

        <!-- Discord Interaction Button -->
        <a href="discord://~/users/118335032822700032" class="discord-btn">
            <svg viewBox="0 0 127.14 96.36">
                <path d="M107.7,8.07A105.15,105.15,0,0,0,77.26,0a77.19,77.19,0,0,0-3.3,6.83A96.67,96.67,0,0,0,53.22,6.83,77.19,77.19,0,0,0,49.88,0,105.15,105.15,0,0,0,19.44,8.07C3.66,31.58-1.86,54.65,1,77.53A105.73,105.73,0,0,0,32,96.36a77.7,77.7,0,0,0,6.63-10.85,68.43,68.43,0,0,1-10.45-5c.87-.64,1.72-1.31,2.53-2a75.46,75.46,0,0,0,72.77,0c.81.69,1.66,1.36,2.53,2a68.43,68.43,0,0,1-10.45,5,77.7,77.7,0,0,0,6.63,10.85,105.73,105.73,0,0,0,31-18.83C129.91,48.49,123.75,25.68,107.7,8.07ZM42.45,65.69C36.18,65.69,31,60,31,53S36.18,40.36,42.45,40.36,53.83,46,53.83,53,48.72,65.69,42.45,65.69Zm42.24,0C78.41,65.69,73.24,60,73.24,53S78.41,40.36,84.69,40.36,96.07,46,96.07,53,91,65.69,84.69,65.69Z"/>
            </svg>
            @eistenium
        </a>
    </div>

</body>
</html>
```eof
