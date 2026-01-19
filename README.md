# Punchbag Game

A simple Vue.js project demonstrating the basics of Vue.js framework. This is an interactive game where users can punch a punchbag and watch its health decrease until it bursts.

## Overview

This project serves as a learning resource for understanding fundamental Vue.js concepts including:
- **Data Binding**: Reactive data properties
- **Directives**: `v-bind`, `v-on`, `v-show`
- **Methods**: Event handlers for user interactions
- **Conditional Rendering**: Showing/hiding elements based on state
- **Dynamic Styling**: Applying CSS classes conditionally

## Features

- **Interactive Punchbag**: Click the "Punch" button to attack the punchbag
- **Health Bar**: Visual representation of the punchbag's remaining health
- **Burst Animation**: When health reaches 0, the bag bursts
- **Restart Game**: Button to reset the game and start over
- **Responsive Design**: Game interface adapts to different screen sizes

## Project Structure

```
punchbag-game/
├── index.html      # Main HTML file with Vue.js template
├── app.js          # Vue.js application logic
├── styles.css      # Styling and animations
├── images/         # Image assets (punchbag sprite)
└── README.md       # This file
```

## Getting Started

### Prerequisites

No build tools or npm packages required! This is a vanilla Vue.js project using the CDN version.

### How to Run

1. Clone the repository:
```bash
git clone https://github.com/yourusername/punchbag-game.git
cd punchbag-game
```

2. Open `index.html` in your web browser

That's it! The game will load and you can start punching.

## How to Play

1. Click the **"Punch"** button to hit the punchbag
2. Each punch reduces the punchbag's health by 10%
3. Watch the health bar turn red when health drops below 30%
4. When health reaches 0%, the punchbag bursts
5. Click **"Restart"** to play again

## Technology Stack

- **Vue.js 2.x**: JavaScript framework for building the interactive UI
- **HTML5**: Structure
- **CSS3**: Styling and animations

## Learning Points

This project demonstrates:
- Vue instance creation and initialization
- Reactive data properties
- Vue methods for handling user interactions
- Computed properties setup
- Class and style bindings
- Conditional rendering with `v-show` and `v-bind`

## Code Example

```javascript
new Vue({
    el: '#vue-app',
    data: {
        health: 100,
        ended: false
    },
    methods: {
        punch: function() {
            this.health -= 10;
            if (this.health <= 0) {
                this.ended = true;
            }
        },
        restart: function() {
            this.health = 100;
            this.ended = false;
        }
    }
});
```

## Customization

Feel free to modify and extend this project:
- Increase/decrease punch damage
- Add sound effects
- Add difficulty levels
- Create multiple enemies
- Add score tracking
- Implement power-ups

## License

MIT License - feel free to use this project for educational purposes.

## Author

Created as a learning project for Vue.js fundamentals.

---

Happy punching! 🥊
