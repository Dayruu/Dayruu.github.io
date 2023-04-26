<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<canvas id="myCanvas"></canvas>
const scene = new THREE.Scene();

const geometry = new THREE.BoxGeometry(1, 1, 1);
const material = new THREE.MeshPhongMaterial({ color: 0xffffff });
const mesh = new THREE.Mesh(geometry, material);

scene.add(mesh);

const light = new THREE.DirectionalLight(0xffffff, 1);

light.position.set(0, 1, 1);

scene.add(light);

const canvas = document.getElementById("myCanvas");

const renderer = new THREE.WebGLRenderer({ canvas });

renderer.setSize(canvas.width, canvas.height);

renderer.render(scene, camera);
