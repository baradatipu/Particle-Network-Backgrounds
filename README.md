# 🌐 Interactive Particle Network Backgrounds

✨ A collection of stunning interactive particle network backgrounds with custom cursor effects. Each design offers a unique visual experience, from spider web networks to cyberpunk-themed animations.

🔗 [Live Demo](https://baradatipu.github.io/Particle-Network-Backgrounds)

## 🎮 Features

- **Custom Cursor Effects**: Each design includes a unique, animated cursor with dot follower
- **Interactive Particles**: Dynamic particle systems that respond to movement
- **Multiple Designs**:
  - Design 1: Spider Web Network - Classic particle connections with white theme
  - Design 2: Floating Network - Vibrant green particles with smooth animations
  - Design 3: Dynamic Network - Unique particle system with custom effects
  - Design 4: Matrix-Style Network - Green matrix-themed particles with edge shapes
  - Design 5: Cyberpunk Network - Neon-styled particles with cyberpunk aesthetics
  - Design 6: Custom Network - Additional particle system variation

## 🛠️ Technologies Used

- HTML5
- CSS3
- JavaScript
- Particles.js Library

## 📥 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/baradatipu/Particle-Network-Backgrounds.git
   ```
2. Navigate to the project directory
3. Open any HTML file in a modern web browser

## 🎯 Usage

- Navigate between different designs using the navigation menu
- Move your cursor around to interact with particles
- Click to trigger cursor animation effects
- Each page features unique particle behaviors and visual styles

## 🌐 Browser Compatibility

This project works best in modern browsers that support:
- HTML5
- CSS3 Animations
- Modern JavaScript

## 🤝 Contributing

Feel free to fork this project and create your own particle network designs. Pull requests are welcome!

## 📖 Implementation Guide

To implement these particle backgrounds in your project, follow these steps for each design:

### Basic Setup (Required for all designs)

1. Add the particles.js library to your HTML:
   ```html
   <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
   ```

2. Create container elements:
   ```html
   <div class="cursor"></div>
   <div class="cursor-dot"></div>
   <div id="particles-js"></div>
   ```

3. Add basic CSS styling:
   ```css
   #particles-js {
       position: fixed;
       width: 100%;
       height: 100%;
       top: 0;
       left: 0;
       z-index: -1;
   }

   .cursor {
       width: 20px;
       height: 20px;
       border: 2px solid #ffffff;
       border-radius: 50%;
       position: fixed;
       pointer-events: none;
       transition: 0.1s;
   }

   .cursor-dot {
       width: 4px;
       height: 4px;
       background: #ffffff;
       border-radius: 50%;
       position: fixed;
       pointer-events: none;
       transition: 0.15s;
   }
   ```

4. Initialize cursor effects:
   ```javascript
   const cursor = document.querySelector('.cursor');
   const cursorDot = document.querySelector('.cursor-dot');

   document.addEventListener('mousemove', (e) => {
       cursor.style.left = e.clientX + 'px';
       cursor.style.top = e.clientY + 'px';
       cursorDot.style.left = e.clientX + 'px';
       cursorDot.style.top = e.clientY + 'px';
   });

   document.addEventListener('mousedown', () => cursor.classList.add('active'));
   document.addEventListener('mouseup', () => cursor.classList.remove('active'));
   ```

### Design-Specific Configurations

#### Spider Web Network (Design 1)
```javascript
particlesJS('particles-js', {
    particles: {
        number: { value: 80, density: { enable: true, value_area: 800 } },
        color: { value: '#ffffff' },
        shape: { type: 'circle' },
        opacity: { value: 0.5, random: false },
        size: { value: 3, random: true },
        line_linked: {
            enable: true,
            distance: 150,
            color: '#ffffff',
            opacity: 0.4,
            width: 1
        },
        move: { enable: true, speed: 6 }
    }
});
```

#### Cyberpunk Network (Design 5)
```javascript
particlesJS('particles-js', {
    particles: {
        number: { value: 100, density: { enable: true, value_area: 800 } },
        color: { value: '#ff00ff' },
        shape: { type: 'edge' },
        opacity: { value: 0.8, random: true },
        size: { value: 4, random: true },
        line_linked: {
            enable: true,
            distance: 150,
            color: '#00ffff',
            opacity: 0.6,
            width: 1
        },
        move: { enable: true, speed: 8 }
    }
});
```

### Customization Tips

- Adjust particle count using `particles.number.value`
- Modify colors using hex values in `particles.color.value` and `line_linked.color`
- Change particle size with `particles.size.value`
- Adjust movement speed using `particles.move.speed`
- Experiment with different shapes: 'circle', 'edge', 'triangle', 'polygon'

## 📄 License

This project is open source and available under the MIT License.