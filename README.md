# Alex
For alex
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday ALEXXX!!</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            height: 100%;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            overflow: hidden;
        }

        .slide {
            width: 100%;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transition: all 0.6s ease-in-out;
            opacity: 0;
            position: absolute;
            top: 0;
            left: 0;
        }

        .slide.active {
            opacity: 1;
            z-index: 10;
        }

        .text-box {
            padding: 30px 60px;
            border-radius: 20px;
            font-size: 3.5rem;
            font-weight: bold;
            text-align: center;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
            margin-bottom: 40px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        .btn {
            padding: 12px 30px;
            font-size: 1.2rem;
            font-weight: bold;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.3);
        }

        /* Slide 1 */
        #slide1 {
            background-color: white;
        }

        #slide1 .text-box {
            background-color: #ff69b4; /* hot pink */
            color: #ff1493; /* deeper hot pink */
        }

        #slide1 .btn {
            background-color: #ff69b4;
            color: white;
        }

        /* Slide 2 */
        #slide2 {
            background-color: #ff69b4;
        }

        #slide2 .text-box {
            background-color: #ff1493;
            color: white;
        }

        #slide2 .btn {
            background-color: white;
            color: #ff69b4;
        }

        /* Slide 3 */
        #slide3 {
            background-color: #ff69b4;
        }

        #slide3 .text-box {
            background-color: #ff1493;
            color: white;
        }

        /* Cake SVG */
        .cake-container {
            margin: 30px 0;
        }

        /* Candle flame animation */
        @keyframes flicker {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.7; transform: scale(0.95); }
        }

        .flame {
            animation: flicker 0.8s infinite alternate;
        }

        .candle-lit .flame {
            fill: #ffd700;
            filter: drop-shadow(0 0 8px #ff8c00);
        }

        .candle-extinguished .flame {
            display: none;
        }
    </style>
</head>
<body>

    <!-- Slide 1 -->
    <div id="slide1" class="slide active">
        <div class="text-box">happy birthday ALEXXX!!</div>
        <button class="btn" onclick="nextSlide(2)">thanks</button>
    </div>

    <!-- Slide 2 -->
    <div id="slide2" class="slide">
        <div class="text-box">make a wish!</div>
        <div class="cake-container">
            <!-- Birthday Cake with Lit Candles -->
            <svg width="200" height="180" viewBox="0 0 200 180" class="candle-lit">
                <!-- Cake base -->
                <rect x="50" y="100" width="100" height="50" rx="10" fill="#f4a460"/>
                <rect x="45" y="95" width="110" height="10" rx="5" fill="#deb887"/>
                
                <!-- Frosting -->
                <path d="M55 95 Q65 85, 75 95 Q85 85, 95 95 Q105 85, 115 95 Q125 85, 135 95 Q145 85, 145 95 L145 100 L55 100 Z" fill="#fff0f5"/>
                
                <!-- Candles -->
                <rect x="75" y="70" width="8" height="25" rx="2" fill="#87ceeb"/>
                <rect x="95" y="70" width="8" height="25" rx="2" fill="#ffb6c1"/>
                <rect x="115" y="70" width="8" height="25" rx="2" fill="#98fb98"/>
                
                <!-- Flames -->
                <path class="flame" d="M77 65 Q79 60, 81 65 Q79 62, 77 65 Z" fill="#ffd700"/>
                <path class="flame" d="M97 65 Q99 60, 101 65 Q99 62, 97 65 Z" fill="#ffd700"/>
                <path class="flame" d="M117 65 Q119 60, 121 65 Q119 62, 117 65 Z" fill="#ffd700"/>
            </svg>
        </div>
        <button class="btn" onclick="nextSlide(3)">blow!</button>
    </div>

    <!-- Slide 3 -->
    <div id="slide3" class="slide">
        <div class="text-box">wish granted! 🎉</div>
        <div class="cake-container">
            <!-- Birthday Cake with Extinguished Candles -->
            <svg width="200" height="180" viewBox="0 0 200 180" class="candle-extinguished">
                <!-- Cake base -->
                <rect x="50" y="100" width="100" height="50" rx="10" fill="#f4a460"/>
                <rect x="45" y="95" width="110" height="10" rx="5" fill="#deb887"/>
                
                <!-- Frosting -->
                <path d="M55 95 Q65 85, 75 95 Q85 85, 95 95 Q105 85, 115 95 Q125 85, 135 95 Q145 85, 145 95 L145 100 L55 100 Z" fill="#fff0f5"/>
                
                <!-- Candles (no flames) -->
                <rect x="75" y="70" width="8" height="25" rx="2" fill="#87ceeb"/>
                <rect x="95" y="70" width="8" height="25" rx="2" fill="#ffb6c1"/>
                <rect x="115" y="70" width="8" height="25" rx="2" fill="#98fb98"/>
            </svg>
        </div>
    </div>

    <script>
        function nextSlide(slideNumber) {
            // Hide all slides
            document.querySelectorAll('.slide').forEach(slide => {
                slide.classList.remove('active');
            });

            // Show target slide
            setTimeout(() => {
                document.getElementById(`slide${slideNumber}`).classList.add('active');
            }, 300);
        }

        // Optional: Add confetti on final slide
        document.getElementById('slide3').addEventListener('transitionend', function(e) {
            if (e.target === this && this.classList.contains('active')) {
                createConfetti();
            }
        });

        function createConfetti() {
            const colors = ['#ff69b4', '#ff1493', '#ffd700', '#ffffff', '#98fb98'];
            for (let i = 0; i < 80; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.style.position = 'fixed';
                    confetti.style.width = '10px';
                    confetti.style.height = '10px';
                    confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.left = Math.random() * 100 + 'vw';
                    confetti.style.top = '-10px';
                    confetti.style.borderRadius = Math.random() > 0.5 ? '50%' : '0';
                    confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                    confetti.style.pointerEvents = 'none';
                    confetti.style.zIndex = '1000';
                    document.body.appendChild(confetti);

                    const duration = 2 + Math.random() * 2;
                    const delay = Math.random() * 0.5;

                    confetti.animate([
                        { top: '-10px', transform: `rotate(${Math.random() * 360}deg)` },
                        { top: '100vh', transform: `rotate(${Math.random() * 720}deg)` }
                    ], {
                        duration: duration * 1000,
                        delay: delay * 1000,
                        easing: 'cubic-bezier(0.1, 0.1, 0.1, 1)'
                    }).onfinish = () => confetti.remove();
                }, i * 30);
            }
        }
    </script>

</body>
</html>
