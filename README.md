<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<canvas id="myCanvas"></canvas>
// Create a new scene
const scene = new THREE.Scene();

// Create a new rectangular mesh
const geometry = new THREE.BoxGeometry(1, 1, 1);
const material = new THREE.MeshPhongMaterial({ color: 0xffffff });
const mesh = new THREE.Mesh(geometry, material);

// Add the mesh to the scene
scene.add(mesh);

// Create a new directional light
const light = new THREE.DirectionalLight(0xffffff, 1);

// Set the position of the light
light.position.set(0, 1, 1);

// Add the light to the scene
scene.add(light);

// Get the canvas element from the DOM
const canvas = document.getElementById("myCanvas");

// Create a new renderer
const renderer = new THREE.WebGLRenderer({ canvas });

// Set the size of the renderer to match the canvas
renderer.setSize(canvas.width, canvas.height);

// Render the scene
renderer.render(scene, camera);
