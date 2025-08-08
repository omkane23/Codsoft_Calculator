# 📱 iPhone Calculator

A pixel-perfect recreation of the iOS Calculator app built with HTML, CSS, and JavaScript. This project features authentic iPhone design elements, smooth animations, and all the functionality of the native iOS calculator.

![iPhone Calculator Preview](https://img.shields.io/badge/Status-Complete-brightgreen) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)


## ✨ Features

### 🎨 Authentic iPhone Design
- **iPhone Frame**: Realistic device bezels with rounded corners and shadows
- **Dynamic Island**: Modern iPhone 14+ style notch area
- **Status Bar**: Live time display with battery indicator
- **Home Indicator**: Bottom swipe bar for modern iOS feel
- **iOS Typography**: Apple's system font stack (-apple-system)

### 🧮 Calculator Functionality
- **Basic Operations**: Addition (+), Subtraction (−), Multiplication (×), Division (÷)
- **Advanced Functions**:
  - AC (All Clear) - Reset calculator
  - ± (Sign Toggle) - Switch between positive/negative
  - % (Percentage) - Convert to percentage
- **Number Formatting**: Automatic comma separation for thousands (1,234)
- **Decimal Support**: Full decimal point calculations
- **Error Handling**: Division by zero protection
- **Chain Calculations**: Continuous operations support

### 🎭 Interactive Elements
- **Haptic Feedback**: Visual shake animation on button press
- **Ripple Effects**: Material design-style touch feedback
- **Operator Highlighting**: Orange buttons glow when active
- **Smooth Animations**: Cubic-bezier transitions throughout
- **Auto Text Sizing**: Numbers automatically resize when display gets full
- **Responsive Design**: Adapts to different screen sizes

### ⌨️ Input Methods
- **Touch/Click**: Full mouse and touch support
- **Keyboard Support**: 
  - Numbers (0-9)
  - Operators (+, -, *, /)
  - Decimal point (.)
  - Enter/= for calculation
  - Escape/C for clear
  - % for percentage

## 🛠️ Technical Implementation

### Technologies Used
- **HTML5**: Semantic markup and structure
- **CSS3**: Advanced styling with Grid, Flexbox, animations
- **JavaScript ES6+**: Modern JavaScript with classes and modules

### Key CSS Features
- **CSS Grid**: 4-column button layout
- **Flexbox**: Display area alignment
- **Custom Properties**: Consistent color scheme
- **Keyframe Animations**: Smooth transitions and effects
- **Backdrop Filter**: iOS-style glassmorphism
- **Media Queries**: Responsive design
- **Pseudo Elements**: Button hover effects

### JavaScript Architecture
```javascript
class iPhoneCalculator {
    constructor()           // Initialize calculator state
    updateDisplay()         // Update visual display
    formatNumber()          // Format numbers with commas
    inputNumber()           // Handle number input
    setOperation()          // Handle operator selection
    calculate()             // Perform calculations
    performCalculation()    // Core math operations
    createRipple()          // Visual feedback effects
    addHapticFeedback()     // Haptic simulation
}
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required

### Installation
1. Clone or download the project files
2. Open `New Calculator.html` in your web browser
3. Start calculating! 

```bash
# If using a local server
npx serve .
# or
python -m http.server 8000
```

### File Structure
```
project/
│
├── New Calculator.html     # Main HTML file with embedded CSS and JS
└── README.md              # This documentation file
```

## 🎯 Usage Examples

### Basic Calculations
- **Addition**: `7 + 3 = 10`
- **Subtraction**: `10 - 4 = 6`
- **Multiplication**: `8 × 9 = 72`
- **Division**: `15 ÷ 3 = 5`

### Advanced Functions
- **Percentage**: `50 % = 0.5`
- **Sign Toggle**: `42 ± = -42`
- **Chain Operations**: `5 + 3 × 2 = 16`

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `0-9` | Number input |
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `.` | Decimal point |
| `Enter` or `=` | Calculate |
| `Escape` or `C` | Clear |
| `%` | Percentage |

## 🎨 Design Specifications

### Colors
- **Background**: Linear gradient from #000000 to #1a1a1a
- **iPhone Frame**: #000000 with #1a1a1a and #333 borders
- **Number Buttons**: rgba(50, 50, 50, 0.8)
- **Operator Buttons**: Linear gradient #ff9f0a to #ff8c00
- **Function Buttons**: rgba(165, 165, 165, 0.9)

### Dimensions
- **iPhone Frame**: 375px × 812px (iPhone 12/13/14 size)
- **Button Height**: 75px
- **Button Border Radius**: 50% (perfect circles)
- **Display Font Size**: 70px (auto-resizing)
- **Gap Between Buttons**: 12px

### Typography
- **Font Family**: -apple-system, BlinkMacSystemFont, 'Segoe UI'
- **Display Weight**: 200 (Ultra Light)
- **Button Weight**: 400 (Regular)
- **Function Weight**: 500 (Medium)

## 📱 Responsive Behavior

The calculator adapts to different screen sizes:

- **Desktop**: Full iPhone frame with realistic bezels
- **Tablet**: Scaled iPhone frame maintaining aspect ratio
- **Mobile**: Optimized layout with smaller buttons and fonts

```css
@media (max-width: 400px) {
    .iphone-frame { width: 95vw; height: 95vh; }
    .display-result { font-size: 60px; }
    button { height: 65px; font-size: 28px; }
}
```

## 🔧 Customization

### Changing Colors
Edit the CSS custom properties to modify the color scheme:

```css
:root {
    --primary-bg: #000000;
    --operator-color: #ff9f0a;
    --number-bg: rgba(50, 50, 50, 0.8);
    --function-bg: rgba(165, 165, 165, 0.9);
}
```

### Adding New Functions
Extend the `iPhoneCalculator` class:

```javascript
class ExtendedCalculator extends iPhoneCalculator {
    sqrt() {
        const current = parseFloat(this.currentInput.replace(/,/g, ''));
        this.currentInput = Math.sqrt(current).toString();
        this.updateDisplay();
    }
}
```

## 🐛 Known Issues & Limitations

- **Precision**: JavaScript floating-point arithmetic limitations
- **Display**: Numbers longer than 9 digits are auto-resized
- **History**: No calculation history (matches iOS behavior)
- **Scientific**: No scientific notation support (basic calculator only)

## 🤝 Contributing

Contributions are welcome! Please feel free to:

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Maintain iOS design consistency
- Add comments for complex functions
- Test on multiple browsers
- Keep animations smooth (60fps)
- Follow existing code style

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Apple Inc.** - Original iOS Calculator design inspiration
- **CSS Tricks** - Grid and Flexbox techniques
- **MDN Web Docs** - JavaScript ES6+ features
- **Can I Use** - Browser compatibility reference

## 📞 Contact & Support

- **Issues**: Open a GitHub issue for bug reports
- **Features**: Submit feature requests via GitHub issues
- **Questions**: Check existing issues or create a new one

---

**Made with ❤️ for learning purposes**

*This project is not affiliated with Apple Inc. iPhone and iOS are trademarks of Apple Inc.*
