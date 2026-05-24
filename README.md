# **🐾 Animal Memory Match \- Kids Adventure\!**

A delightful, highly interactive, and educational **Memory Matching Game** designed specifically for children. Built entirely from scratch using a high-performance HTML5 \<canvas\> rendering engine, Tailwind CSS, and native Web APIs, this single-file web app offers a premium, kid-friendly gaming experience across all devices.

## **🎮 Live Demo**

Play the game in your browser — no install required:

**👉 [Animal Memory Match — Live Demo](https://inhumba.github.io/Animal-Memory-Match/)**

## **✨ Features**

* **🎮 4 Immersive Animal Themes:**  
  * 🦁 **Safari:** Lion, Zebra, Elephant, Giraffe, Monkey, Hippo, Tiger, Leopard, Rhino, Crocodile, Flamingo, Gorilla.  
  * 🦊 **Forest:** Bear, Fox, Squirrel, Owl, Deer, Bunny, Hedgehog, Raccoon, Wolf, Boar, Beaver, Badger.  
  * 🐬 **Ocean:** Whale, Dolphin, Octopus, Shark, Turtle, Fish, Crab, Seal, Blowfish, Lobster, Shrimp, Squid.  
  * 🐶 **Pets:** Dog, Cat, Hamster, Bunny, Parrot, Fish, Turtle, Unicorn, Mouse, Lizard, Pig, Chicken.  
* **📈 4 Difficulty Levels:**  
  * **Easy:** 3 Pairs (![][image1] grid) — Perfect for toddlers.  
  * **Medium:** 6 Pairs (![][image2] grid) — Balanced fun.  
  * **Hard:** 8 Pairs (![][image3] grid) — A healthy brain exercise.  
  * **Expert:** 12 Pairs (![][image4] grid) — The ultimate memory championship\!  
* **🗣️ Audio-Assisted Learning (Voice & SFX):**  
  * **Web Speech API integration:** Pronounces the name of the animal out loud in a friendly voice whenever a card is flipped, transforming the game into an interactive flashcard learning tool.  
  * **Procedural Audio Synthesizer (Web Audio API):** Generates custom playful sound effects on-the-fly for card flips, successful matches, mismatches, and victory fanfares without using external audio files.  
* **🎨 Stunning Procedural Animations:**  
  * High-DPI (Retina-ready) automated canvas scaling for ultra-sharp rendering.  
  * 3D horizontal card-flipping calculations.  
  * "Shaking" mismatch animations to gently signal errors.  
  * Explosive custom particle physics (confetti, hearts, and stars) on matches and victory.  
  * Interactive scoreboard HUD with moves tracker, remaining pairs, and persistent High Scores (saves to browser localStorage).

## **🛠️ Tech Stack**

* **Markup & Layout:** HTML5, [Tailwind CSS](https://tailwindcss.com/) (loaded via CDN)  
* **Typography:** [Google Fonts](https://fonts.google.com/) — **Margarine** (headings & playful UI), **Quicksand** (body text)  
* **Engine:** Vanilla JavaScript \+ HTML5 Canvas API  
* **Audio & Speech:** Web Audio API & Web Speech Synthesis API  
* **State & Storage:** LocalStorage (for High Scores saving)

## **🚀 Quick Start / Local Setup**

Because the entire game is built as a **single, self-contained file**, there are no complex build tools, compilers, or server setups required\!

1. **Clone the Repository:**  
   git clone https://github.com/inhumba/Animal-Memory-Match.git
   cd Animal-Memory-Match

2. **Launch the Game:**  
   Simply double-click the index.html file or open it directly inside any modern web browser (Chrome, Safari, Edge, Firefox).

## **📱 Mobile & Tablet Optimization**

* Designed with mobile-first responsiveness.  
* Large touch targets tailored for small children's fingers.  
* Integrated unified touch event listeners (touchstart & mousedown) to eliminate tapping delays.  
* Dynamic canvas orientation adjustments on window resize to ensure no horizontal scrolling occurs.

## **📝 License**

This project is open-source and free to use or modify. Have fun playing and learning with your kids\! 💖

## **📋 Recent Updates**

* **Typography:** Playful UI font updated from Fredoka One to **Margarine** (Google Fonts); Quicksand remains for body text.
* **Difficulty modes:** Top tier renamed from **Hardest** to **Expert** (12 pairs, 6×4 grid).

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC4AAAAZCAYAAABOxhwiAAABx0lEQVR4Xu2Vvy4EURTGZUUkBCFkkp2xszu7yVaqLRQ8gifQeAUPYDU6rUShJaHXegAlOi2NQsOy2PXvO3KGO587f2yyCuaXnOzc75wz97sz984ODOTk/BNKpdKi7/vXiDfEMaQC1/wGmPtIPbTK5fIK5yOgaAuxbYzb0ozFBGZdv8GcT/gZlOt6vT6mHi6o7AspwOrmWZMwtX4Cg+s6ZzPUEj04jjNqK7BpNlCzzJpJo9EYkqfHOuN53pzMhwUshVqqByQ30LBAWnKTUqlUHNTdsC7oQ+mwnhX10GI9EW16Zd2G67oeau9MTU13TS0rQRBMyMNAtDmXCPb7mRgvFosjnIujWq3OoudertX0M9dkAX1NxA7iwTc+GKnIIRXTtVpthnNphOZ7Nc2IDwnWv4F9PqmmhzmXBRywKfR35Wlxrhdwn0M1v885kwKvDuNdc5xEaFquscWm/R/uT9SfIG5JW1Pj8WfFtxxEaC+s2dA3Fbm5mv/Y81lQg5FzhfGeaLj/gVn7CZKdsJGDaxlsq3HUPbIuqPnI1yYO1F0iNkmL94BX7LJZI1L3Kg7zKmsm8ucjC2DdBuY71XnP9feKa3JycnJy/gbvciiVE7uC9qAAAAAASUVORK5CYII=>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC4AAAAZCAYAAABOxhwiAAAB0ElEQVR4Xu2Vu0oDQRSGBVELL3gLC9ndbG4aCaLgtnZ2VoKdDyCW1voGYqNgJVgJgrX4AhYKPoCFlaidFoI3jEn8TzgTxkN2Z5MiIM4Hh53555ydfy8z09NjsfwTcrncfBAEz4g64iqbzY7KnG5DXlzXnZB6E5jcQNK+6qN9zA+woOd1E8x9YjTOJusmrVt4njeOue+SGH+QJpMaR86a1HTCMOwrlUrDUo+D5vV9f9ZoXIKCLTa+LMckWBsO8l6kTjiOM4ixL6nHgfwj/LozbRtH0QoV4Lonx6LAzT3UvOoam67omolUKjWEmmtqt2UcibswfIprNZPJLMnxOAqFgo+6N2qz6W+ZYwI1NdVuy7gCi8OlIsSZHItDme/Q9A5eVqj6HRkn2LhxcerwblBBfMixOMrlcj9qbnQtkXEkVBGHQmsYx1tY1PUolGlqp9PpSbTfZU4UqJ1C/oWIW/ZwSX1ZQwZXlUmhK61X11uBhxsLxEJk841/vhNwz3Wa3/TG68VicUD1scXNsfFzPa8VqBtB3qfUCTb/a7dJCuq2yUM+n5+WY034M9c4ntj0gcxrBXahTanp0OFDDyD1KPjrkQc6FO8Rj0HEOWGxWCyWv8sPGT6NiZPIh+UAAAAASUVORK5CYII=>

[image3]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC4AAAAZCAYAAABOxhwiAAABmklEQVR4Xu2Vu0rEQBSGt9HGC3gJgdw2N40Eu7yND2Bt7xv4BoLYWgl2goWNhYVga2ElKljYCK6KK67/WWZgPOYySeEizgcDJ2fOSb5kMkmvZzD8Q6Io6oMRz/825OC67hLPV0INkxbH9Q9aiYdheIKGwSTFPc9bxPVvtMVR5AVBcISGR11x1G3wnEpRFFNZls3xfB10bd/317XFpWwbcewHG7VPPE/Ytj2DuXeerwP1+1j1NW1xFB0mSeKLWFucoJVC/bOaE9JDNdeEZVmz6LmgWEucJlF0Ko/bihN00+gZUCykP3hNE+j5lLGWOJfsIk5I+Y7SO9hfhTxuFMf7tEvvlJrrKi6+BkOMVz5XR57n0+i5UnON4pg8xjhjYyQGxXu8pwwpTbHjOMuIX3hNFehdKXG4Fg7ndMx7ShEN2k8cS7wgpSVCfvzOdwHn3CSHyideRhvxNE3nUfvG84SQ//a10QV92+QQx/Eqn/sBCi8xHjBuxaB4/HmqAvtji+dU6OdDN8DzVYjVoz12Jxzu+xX/CYPBYDD8Xb4AT5WK5wRoTK4AAAAASUVORK5CYII=>

[image4]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC4AAAAZCAYAAABOxhwiAAAB4ElEQVR4Xu2WO0sDQRSFbRTxBT6WhWQ3m5dGg91i4W/wF2hlZSfYW4iVYG1tIyK2gq2NhYUgioWFWoiPykbwhRHjueEOTC6ZnSRFQJwPLsycuTNzZu8yu11dDsc/olQqDUZRdIuoIs7keKchH+l0elTqdWSz2UVKjOO4m/qZTGYN/ReZ1ymw957VeLFY9CgJ5nuVxk+9qud1iiAIRrD3ndV4I5OpVKpP75vAvAWp6VAF6RWUehLkJQzD6WaNX3J7tpWNcrmcHxleKd/3+zH2JfUkkL+Nyk9ajWNwio3vIi54sy3SZK4JLB4g/1XXeJ2KrtnwPG8Ac06pbTWO082z8Tqj6P8gPnQtiUKhECL/jdps+lvm2KA9VdtqHINzbPxJ6EfyMDaU+TZNb+Imi1XfahzvaMTGd3QdlTggHQvM6HoSfBtUohYqRZTL5R7MudI1q3GCEmB0X2iHpOfz+QldN6FMUxs30hja7zLHBOaOI/9YxDXtjzihvpxTgxNuhHZOuq6ZQImHlWkFm6+98+2ANZdo/8Qnrsqia9RHFdZ1rRH4eA0h91PqBJuvu22aBfNWyYO14jjhMj/52r8K+hsypxE43IrUdOibQAeQugmu3jPiAXGPeIwM3wmHw+Fw/F1+ATxLlCcjENhrAAAAAElFTkSuQmCC>