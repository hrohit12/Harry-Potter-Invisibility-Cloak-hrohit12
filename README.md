Real-Time Invisibility Cloak-hrohit12
This project is a fun, web-based implementation of a "Harry Potter"-style invisibility cloak using JavaScript, HTML5 Canvas, and your webcam. It detects a specific color (red by default) in the live video feed and replaces it with a pre-captured background image, creating the illusion of invisibility.

🚀 Live Demo
Try it out yourself! [Link to your live demo here] (e.g., hosted on GitHub Pages, Netlify, or Vercel)

✨ Features
Real-Time Video Processing: Manipulates your webcam feed live in the browser.

Color Detection: Uses an HSV color model to accurately detect a specific color, even in varied lighting.

Static Background Replacement: Captures a background image and uses it to create the invisibility effect.

Simple User Interface: An easy-to-use interface to start the effect with a single click.

No Backend Needed: Runs entirely on the client-side in your web browser.

🛠️ Technologies Used
This project is built with modern web technologies and requires no external libraries (besides Tailwind for styling).

HTML5: For the basic structure and the <video> and <canvas> elements.

CSS3 & Tailwind CSS: For creating a clean, modern, and responsive user interface.

JavaScript (ES6+): The core engine that drives all the logic.

WebRTC API (navigator.mediaDevices.getUserMedia): To securely access the live webcam feed.

HTML Canvas API: To read video frames, process pixels in real-time, and render the final effect.

⚙️ How to Use
To run this project on your local machine, follow these simple steps:

Clone the repository:

git clone https://github.com/hrohit12/Real-Time-Invisibility-Cloak-hrohit12

Navigate to the project directory:

cd your-repository-name

Open the index.html file:

Since this project has no dependencies, you can simply open the index.html file directly in a modern web browser like Chrome, Firefox, or Edge.

For the best experience (to avoid any potential CORS issues with local files), it's recommended to use a lightweight local server. If you have VS Code, the "Live Server" extension is a great option.

Grant camera permission when your browser asks for it.

Follow the on-screen instructions to make the magic happen!

🔬 How It Works
The magic behind the cloak is a sequence of steps handled by JavaScript:

Camera Access: The WebRTC API is used to get access to the user's webcam feed, which is then streamed to a hidden <video> element.

Background Capture: When the user starts the process, the application captures a single frame from the video stream. This frame is stored as the static "background."

Real-Time Processing Loop: The application then starts a loop using requestAnimationFrame for smooth, continuous processing. In each frame:

The current video frame is drawn onto an HTML <canvas>.

The pixel data for the entire canvas is read into a JavaScript array.

The code iterates through every pixel, converting its color from the RGB model to the HSV (Hue, Saturation, Value) model. HSV is used because it's much more reliable for detecting a specific color across different lighting conditions and shades.

If a pixel's HSV value falls within the defined range for "red," it is replaced with the corresponding pixel from the stored background image.

The modified pixel data is then drawn back onto the canvas, creating the final image that the user sees.
