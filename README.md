![dynamic-model_png](image.png)
# Dynamic Four-Bar Linkage Mechanism Simulator
An interactive web-based kinematic analysis and visualization tool for four-bar linkage mechanisms with real-time animation and trajectory tracking.

## 🎯 Overview

This application provides a comprehensive solution for analyzing and visualizing the kinematics of four-bar linkage mechanisms (ABCD). It calculates joint positions, link angles, and traces the trajectory of point E on the coupler link, making it ideal for mechanical engineering education and mechanism design validation.

## ✨ Features

- **Real-time Kinematic Analysis**: Calculates joint positions and link angles for any crank angle
- **Interactive Visualization**: SVG-based rendering with automatic scaling and viewport adjustment
- **Trajectory Tracking**: Records and displays the complete path of point E on the coupler link
- **Animation Control**: Play/pause mechanism rotation with adjustable crank angle
- **Parameter Configuration**: Customize all mechanism dimensions and geometric properties
- **Responsive Design**: Clean, modern interface that works across different screen sizes
- **Auto-assembly Check**: Validates mechanism configuration and reports assembly feasibility

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- npm (comes with Node.js)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd dynamic-model
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to the URL shown in the terminal (typically `http://localhost:5173`)

## 📖 Usage

### Input Parameters

The mechanism is defined by the following parameters:

- **l₁ (AB)**: Length of the crank link (m)
- **l₂ (BC)**: Length of the coupler link (m)
- **l₃ (CD)**: Length of the rocker link (m)
- **x (A → D)**: Horizontal distance from point A to point D (m)
- **y (A → D)**: Vertical distance from point A to point D (m)
- **L_BE / L_BC**: Ratio of BE to BC length
- **∠(BC, BE)**: Angle between BC and BE (degrees)
- **φ₁**: Initial crank angle (degrees)

### Controls

1. **Enter Parameters**: Fill in the mechanism dimensions in the right panel
2. **Submit**: Click "Mexanizmi göstər" to visualize the mechanism
3. **Adjust Angle**: Use the slider to manually change the crank angle
4. **Animate**: Click "Play" to automatically rotate the crank
5. **Clear Trace**: Reset the trajectory path of point E

### Output

The application displays:
- Visual representation of the four-bar linkage
- Real-time joint coordinates (A, B, C, D, E)
- Link angles (φ₁, φ₂, φ₃)
- Trajectory path of point E
- Assembly status and validation

## 🛠️ Technology Stack

- **React 19.2.0**: UI framework with hooks for state management
- **Vite 7.2.4**: Fast build tool and development server
- **SVG**: Vector graphics for mechanism visualization
- **ESLint**: Code quality and consistency
- **CSS3**: Modern styling with custom properties

## 📐 Mathematical Model

The application solves the position analysis problem for a four-bar linkage using:

1. **Vector loop closure equation**: AB + BC + CD = AD
2. **Trigonometric solution**: Solves for φ₂ and φ₃ given φ₁
3. **Discriminant validation**: Ensures mechanism can be assembled
4. **Point E calculation**: Extends from point B along BE vector

The kinematic equations are solved using the tangent half-angle substitution method for robust and accurate results.

## 📁 Project Structure

```
dynamic-model/
├── src/
│   ├── App.jsx          # Main application component
│   ├── App.css          # Styling
│   └── main.jsx         # React entry point
├── index.html           # HTML template
├── package.json         # Dependencies and scripts
├── vite.config.js       # Vite configuration
├── eslint.config.js     # ESLint configuration
└── README.md            # This file
```

## 🔧 Available Scripts

- `npm run dev`: Start development server with hot module replacement
- `npm run build`: Build production-ready optimized bundle
- `npm run preview`: Preview production build locally
- `npm run lint`: Run ESLint to check code quality

## 🧪 Example Configuration

Try these parameters for a functional four-bar linkage:

```
l₁ (AB): 0.5 m
l₂ (BC): 1.2 m
l₃ (CD): 0.8 m
x: 1.5 m
y: 0.3 m
L_BE / L_BC: 0.6
∠(BC, BE): 45°
φ₁: 0°
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## 📝 License

This project is available for educational and research purposes.

## 🙏 Acknowledgments

Developed as part of Tapşırıq 10 (Task 10) - Four-Bar Linkage Mechanism kinematic analysis project.

---

**Note**: The interface and comments are in Azerbaijani language. The mechanism follows standard mechanical engineering conventions with counterclockwise positive angles and standard Cartesian coordinates.
