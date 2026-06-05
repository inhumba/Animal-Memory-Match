# **🐾 Animal Memory Match \- Kids Adventure\!**

A delightful, highly interactive, and educational **Memory Matching Game** designed specifically for children. Built entirely from scratch using a high-performance HTML5 \<canvas\> rendering engine, Tailwind CSS, and native Web APIs, this single-file web app offers a premium, kid-friendly gaming experience across all devices.

## **🎮 Live Demo**

Play the game in your browser — no install required:

**👉 [Animal Memory Match — Live Demo](https://inhumba.github.io/Animal-Memory-Match/)**

## **✨ Features**

* **🎮 12 Immersive Themes:**  
  * 🦁 **Safari:** Lion, Zebra, Elephant, Giraffe, Monkey, Hippo, Tiger, Leopard, Rhino, Crocodile, Flamingo, Gorilla.  
  * 🦊 **Forest:** Bear, Fox, Squirrel, Owl, Deer, Bunny, Hedgehog, Raccoon, Wolf, Boar, Beaver, Badger.  
  * 🐬 **Ocean:** Whale, Dolphin, Octopus, Shark, Turtle, Fish, Crab, Seal, Blowfish, Lobster, Shrimp, Squid.  
  * 🐶 **Pets:** Dog, Cat, Hamster, Bunny, Parrot, Fish, Turtle, Unicorn, Mouse, Lizard, Pig, Chicken.  
  * 👕 **Clothing:** Shirt, Dress, Pants, Coat, Socks, Sneaker, Hat, Crown, Scarf, Gloves, Sunglasses, Boot.  
  * 🍎 **Fruit:** Apple, Banana, Grapes, Orange, Watermelon, Strawberry, Cherry, Pineapple, Mango, Peach, Lemon, Kiwi.  
  * 🚀 **Vehicles:** Rocket, Helicopter, Train, Car, Bicycle, Ship, Ambulance, Firetruck, Police Car, Bus, Tractor, Airplane.  
  * 🦖 **Fantasy:** T-Rex, Dinosaur, Unicorn, Dragon, Castle, Fairy, Mermaid, Wizard, Ghost, Egg, Volcano, Magic Ball.  
  * 🧸 **Toys:** Teddy Bear, Balloon, Kite, Soccer Ball, Basketball, Art Paint, Video Game, Puzzle, Dice, Skateboard, Guitar, Saxophone.  
  * 🌈 **Nature:** Sun, Rain, Snowflake, Rainbow, Lightning, Cloud, Moon, Star, Mushroom, Wave, Clover, Fire.  
  * 🦋 **Insects:** Butterfly, Ladybug, Bee, Ant, Spider, Caterpillar, Snail, Grasshopper, Mosquito, Scorpion, Web, Beetle.  
  * 🍰 **Sweets:** Pizza, Burger, Fries, Hot Dog, Popcorn, Fried Egg, Donut, Cupcake, Ice Cream, Cake, Lollipop, Chocolate.  
* **📈 4 Difficulty Levels:**  
  * **Easy:** 3 Pairs — Perfect for toddlers.  
  * **Medium:** 6 Pairs — Balanced fun.  
  * **Hard:** 8 Pairs — A healthy brain exercise.  
  * **Expert:** 12 Pairs — The ultimate memory championship\!  
* **🗣️ Audio-Assisted Learning (Voice & SFX):**  
  * **Web Speech API integration:** Pronounces the animal name in a friendly voice whenever a card is flipped, turning the game into an interactive flashcard learning tool. Works on desktop and mobile browsers (Chrome & Safari on phones/tablets).  
  * **Procedural Audio Synthesizer (Web Audio API):** Generates custom playful sound effects on-the-fly for card flips, successful matches, mismatches, and victory fanfares without using external audio files.  
  * **Mute toggle:** A header button mutes both speech and SFX together.  
* **🎨 Stunning Procedural Animations:**  
  * High-DPI (Retina-ready) automated canvas scaling for ultra-sharp rendering.  
  * 3D horizontal card-flipping calculations.  
  * "Shaking" mismatch animations to gently signal errors.  
  * Explosive custom particle physics (confetti, hearts, and stars) on matches and victory.  
  * **Focused in-game HUD:** During play, the header shows **Flips** and **Pairs Left** only — clear live progress without score pressure. **Score** and **Best** appear after a round is won; personal bests are saved per theme and difficulty in browser `localStorage`.
* **🏆 Star-Based Scoring (0–100):**  
  * No timer — speed is not scored, so kids are not rushed.  
  * **Flips** count how many two-card turns you take (lower is better for earning stars).  
  * **Stars (1–3)** are awarded from flip count at the end of the round, per difficulty.  
  * **Round score** is tied to stars: **1★ = 55**, **2★ = 75**, **3★ = 95**, plus **+5 streak bonus** when you match **2 or more pairs in a row** without a miss (maximum **100**).  
  * The victory screen shows stars, rank message, flips, and final score out of 100.

## **🛠️ Tech Stack**

* **Markup & Layout:** HTML5, [Tailwind CSS](https://tailwindcss.com/) (loaded via CDN)  
* **Typography:** [Google Fonts](https://fonts.google.com/) — **Margarine** (headings & playful UI), **Quicksand** (body text)  
* **Engine:** Vanilla JavaScript \+ HTML5 Canvas API  
* **Audio & Speech:** Web Audio API & Web Speech Synthesis API  
* **State & Storage:** LocalStorage (for best round scores, keyed by theme + difficulty)

## **🚀 Quick Start / Local Setup**

Because the entire game is built as a **single, self-contained file**, there are no complex build tools, compilers, or server setups required\!

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/inhumba/Animal-Memory-Match.git
   cd Animal-Memory-Match
   ```

2. **Launch the Game:**  
   Simply double-click the index.html file or open it directly inside any modern web browser (Chrome, Safari, Edge, Firefox).

## **📱 Mobile & Tablet Optimization**

* Designed with mobile-first responsiveness.  
* Large touch targets tailored for small children's fingers.  
* Integrated unified touch event listeners (`touchstart` & `mousedown`) to eliminate tapping delays.  
* Dynamic canvas orientation adjustments on window resize to ensure no horizontal scrolling occurs.  
* Setup menu and victory screen use scrollable, full-viewport layouts on phones to prevent content clipping.  
* **Speech on iOS/Android:** Voices are cached when the browser loads them, the speech engine is woken on **Play** (and on the first card tap if needed), and overlapping utterances are handled safely for mobile Safari/Chrome.

## **📋 Recent Updates**

* **Scoring & HUD:** Replaced flip-count “high scores” with a **0–100 star-based score** (55 / 75 / 95 by stars, +5 streak bonus, max 100). No timer. Header shows **Flips + Pairs Left** during play; **Score + Best** appear only after victory. Best scores persist per theme and difficulty in `localStorage` (`animal_memory_best_scores`).
* **Mobile speech:** Fixed animal-name voice-over on phones and tablets (iOS/Android Chrome & Safari). Voices load via `voiceschanged`, the engine primes on Play, and `speak()` is deferred correctly after `cancel()` on WebKit.
* **Victory screen:** Fixed mobile clipping by moving the overlay outside the canvas container, using a full-screen modal on phones, and tightening responsive spacing.
* **Favicon:** Added `favicon.ico` at the project root and linked it in `index.html` for browser tab branding.
* **Mobile layout:** Fixed menu overlap on phones/tablets by switching to `min-h-dvh`, natural-flow setup screen, and responsive game board toggling.
* **Typography:** Playful UI font updated from Fredoka One to **Margarine** (Google Fonts); Quicksand remains for body text.
* **Difficulty modes:** Top tier renamed from **Hardest** to **Expert** (12 pairs, 6×4 grid).

## **📝 License**

This project is open-source and free to use or modify. Have fun playing and learning with your kids\! 💖
