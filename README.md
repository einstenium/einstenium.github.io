<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Einstenium | Biography</title>
    <style>
        /* CSS resets */
        body, h1, p, ul {
            margin: 0;
            padding: 0;
        }

        /* Core structure and theme - Minimalist Dark */
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
            background-color: #0d1117; /* GitHub dark bg */
            color: #c9d1d9; /* GitHub subtle text */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* The container for all content */
        .bio-container {
            width: 100%;
            max-width: 600px;
            padding: 40px 20px;
            text-align: center;
            background-color: #161b22; /* Slightly lighter container */
            border-radius: 12px;
            border: 1px solid #30363d;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            animation: fadeIn 1.5s ease;
        }

        /* Profile image styling */
        .profile-picture {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #30363d;
            margin-bottom: 25px;
            pointer-events: none; /* User can't right-click save image */
        }

        /* Username styling */
        h1 {
            font-size: 2.2rem;
            color: #f0f6fc; /* Near white */
            letter-spacing: -1px;
            font-weight: 800;
            margin-bottom: 15px;
        }

        /* The quote / short biography */
        .quote {
            font-size: 1.1rem;
            color: #8b949e;
            font-style: italic;
            line-height: 1.6;
            max-width: 80%;
            margin: 0 auto 30px auto;
        }

        /* The Discord link styling */
        .discord-link {
            display: inline-block;
            text-decoration: none;
            color: #c9d1d9;
            background-color: #30363d;
            padding: 12px 24px;
            border-radius: 6px;
            border: 1px solid #30363d;
            font-weight: 600;
            transition: all 0.2s ease-in-out;
            cursor: pointer;
        }

        .discord-link:hover {
            background-color: #f0f6fc; /* Highlight to near white */
            color: #0d1117;
            border-color: #f0f6fc;
        }

        /* Simple animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Small screen adjustments */
        @media (max-width: 600px) {
            .bio-container {
                border-radius: 0;
                border: none;
                background-color: #0d1117; /* Merge with bg on mobile */
            }
        }
    </style>
</head>
<body>

    <div class="bio-container">
        <!-- Profile Image referenced from your provided image -->
        <img src="93481932.webp" alt="Einstenium Profile Picture" class="profile-picture">

        <!-- Username -->
        <h1>einstenium</h1>

        <!-- Biography / Philosophical Quote -->
        <p class="quote">
            "Imagination is more important than knowledge. For knowledge is limited, whereas imagination embraces the entire world."
        </p>

        <!-- Direct Discord link (simulating dc://protocol for direct opening) -->
        <a href="discord://~/users/118335032822700032" class="discord-link">Contact: @eistenium</a>
    </div>

</body>
</html>
