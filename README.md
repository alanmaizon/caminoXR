# 3D First-Person Simulator

This project is a first-person 3D simulation where a user can walk around a virtual bedroom using keyboard and mouse controls. The scene is rendered using **Three.js** with the ability to jump, crouch, and look around. Smooth transitions are implemented for actions like jumping and crouching to create a more natural feel.

## Features
- First-person movement with smooth transitions.
- Mouse look for rotating the view horizontally and vertically.
- Jumping using the `Spacebar` with a smooth return to standing height.
- Crouching using `Ctrl` for smooth crouch and stand actions.
- Boundaries set to prevent movement outside of the room.
- A simple toggle between two heights (dog view and human view).
- The scene includes lighting and a 3D bedroom model loaded from a `.glb` file.

## Usage

### Movement Controls
- **W** or **↑**: Move forward
- **S** or **↓**: Move backward
- **A** or **←**: Move left
- **D** or **→**: Move right
- **Mouse**: Look around (horizontal and vertical movements)
- **Spacebar**: Jump with a smooth return to standing height.
- **Ctrl**: Crouch down with a smooth transition.

### Mouse Controls
- **Left-click**: Hold and move the mouse to look up, down, left, and right.
- **Movement**: Use the mouse to rotate the view horizontally, which also updates the movement direction.

## Project Structure

- **app.py**: Flask server handling static file serving and routing.
- **static/**:
  - **3D/**: Contains the 3D model files (e.g., `room.glb`).
  - **scripts/**: Contains `controls.js`, which manages the camera and movement logic.
- **templates/**:
  - **index.html**: The main HTML file displaying the 3D scene and including the necessary scripts.
  
## How It Works

- The project uses **Three.js** to render a 3D scene and simulate first-person navigation within a confined space.
- Movement is controlled using `velocity` and `direction` vectors, with boundaries in place to limit the movement to the room's perimeter.
- The **camera**'s position is dynamically updated based on the user's input, including smooth transitions for jumping and crouching.
- The 3D bedroom model is loaded using the **GLTFLoader** from Three.js, with lighting and camera settings adjusted to enhance the realism of the scene.

## Contributions

Feel free to fork this repository, submit pull requests, or open issues for suggestions or bug reports.
