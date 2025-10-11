# 🔒 Secure Encryption Tool

![Encryption Tool Screenshot](https://via.placeholder.com/800x400.png?text=Secure+Encryption+Tool) <!-- Placeholder for screenshot -->

A modern web-based application for AES-256 encryption and decryption, featuring a sleek, dark-themed UI with dynamic visual effects and robust accessibility. Encrypt sensitive data securely with an intuitive interface.

## 📋 Table of Contents
- [Features](#-features)
- [Technologies](#-technologies)
- [Setup](#-setup)
- [Usage](#-usage)
- [Accessibility](#-accessibility)
- [Visual Effects](#-visual-effects)
- [Performance](#-performance)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features
- **🔐 AES-256 Encryption/Decryption**: Securely encrypt and decrypt text using the industry-standard AES-256 algorithm via CryptoJS.
- **🔑 Key Strength Indicator**: Real-time feedback on secret key strength (Weak, Medium, Strong) with a dynamic progress bar.
- **📄 Result Animation**: Smooth character-by-character fade-in effect for encrypted/decrypted output, with a copy-to-clipboard button.
- **🔔 Toast Notifications**: Success and error messages displayed via animated toasts for user feedback.
- **📱 Responsive Design**: Optimized for desktop and mobile devices with a centered, card-based layout.
- **♿ Accessibility**: ARIA roles and attributes for screen reader support, ensuring inclusive usability.
- **🌟 Dynamic Visuals**: Subtle canvas-based particles, rotating 3D hexagon, and a curly cursor trail for an engaging UI.

## 🛠 Technologies
- **HTML5**: Structure for the web application.
- **CSS3**: Dark-themed styling with animations (e.g., fadeIn, hover effects).
- **JavaScript**: Core logic, canvas animations, and CryptoJS for encryption.
- **CryptoJS (4.1.1)**: AES-256 encryption/decryption library.
- **Canvas API**: For rendering particles, geometric shapes, and cursor effects.

## ⚙ Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/vinaypinagadi/AES-256-encryption.git
   ```
2. **Serve the Application**:
   - Use a local server (e.g., VS Code Live Server, `http-server`, or Python's `http.server`):
     ```bash
     python -m http.server 8000
     ```
   - Open `index.html` in a modern browser (Chrome, Firefox, Edge).
3. **Dependencies**: No installation required; CryptoJS is loaded via CDN:
   ```html
   <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
   ```

## 🚀 Usage
1. **Enter Text**: Input the text to encrypt or decrypt in the first field.
2. **Provide Secret Key**: Enter a key (minimum 8 characters) in the password field. The strength bar updates in real-time.
3. **Encrypt/Decrypt**:
   - Click **Encrypt** to generate an AES-256 encrypted string.
   - Click **Decrypt** to decode an encrypted string with the correct key.
4. **View Result**: The output appears with a smooth fade-in animation. Click the **Copy** button to copy the result.
5. **Error Handling**: Invalid inputs or keys trigger animated error messages and toasts.

## ♿ Accessibility
- **ARIA Support**:
  - `role="region" aria-live="polite"` for result output.
  - `role="alert"` for error and toast notifications.
  - Descriptive `aria-label` attributes for inputs.
- **Keyboard Navigation**: All buttons and inputs are focusable and operable via keyboard.
- **Default Cursor**: Preserved to ensure compatibility with assistive technologies, with a subtle curly trail effect for visual enhancement.

## 🎨 Visual Effects
- **Rotating 3D Hexagon**:
  - A wireframe hexagon with 2px `#FFD700` borders, rotating in 3D space over 20 seconds.
  - Semi-transparent (opacity: 0.2) and positioned behind content (z-index: -1).
- **Canvas Animations**:
  - **Geometric Shapes**: Rotating triangles and hexagons with 2px lines, spawning at 2% frequency, with sizes 15–40px and opacity 0.2–0.5.
  - **Particles**: Small (1.6px diameter) `#FFD700` dots, spawning at 5% frequency, with gentle motion (0.1–0.4px/frame) and fast fading (0.008–0.02).
  - **Curly Cursor**: A trail of 2px particles follows the mouse, with oscillating motion for a smooth, curly effect, fading over 20–40 frames.
- **Subtle Design**: All effects have low opacity (canvas: 0.2) to maintain focus on functionality.

## ⚡ Performance
- **Optimized Canvas**: Shapes and particles are removed when faded or off-screen to minimize memory usage.
- **Low Spawn Rates**: Shapes (2%) and particles (5%) spawn infrequently to ensure smooth rendering.
- **Curly Cursor**: Particles spawn only on significant mouse movement (>1px), with short lifespans to limit overhead.
- **Hardware Acceleration**: CSS transforms used for 3D hexagon and UI animations for better performance.

## 🤝 Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request with a detailed description.

Please ensure code adheres to the existing style and maintains accessibility standards.

## 📜 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

*Built with security and user experience in mind, this tool combines robust encryption with modern, accessible design.*  
For issues or suggestions, please open a ticket on the [GitHub repository](https://github.com/your-repo/secure-encryption-tool).