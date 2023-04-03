## Hello! I am Shadly Salahuddin. 

[![Website Website](https://img.shields.io/badge/%20-Website-black?color=222244&labelColor=000000&logo=github&logoColor=f5f7fe)](https://shadlyd15.github.io/)
[![Blog Blog](https://img.shields.io/badge/%20-Blog-black?color=222244&labelColor=000000&logo=jekyll&logoColor=f5f7fe)](https://shadlyd15.github.io/blog/)
[![LinkedIn LinkedIn](https://img.shields.io/badge/%20-LinkedIn-black?color=222244&labelColor=000000&logo=LinkedIn&logoColor=f5f7fe)](https://www.linkedin.com/in/shadlyd15/)
[![Gmail](https://img.shields.io/badge/%20-Send%20Mail-black?color=222244&labelColor=000000&logo=gmail&logoColor=f5f7fe)](mailto:shadlyd15@gmail.com?subject=From%20GitHub&&body=Hi,%20there.%20Found%20you%20on%20GitHub!%20Let's%20talk%20about...)



<!--
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=shadlyd15&layout=compact)](https://github.com/shadlyd15)
-->


# Rotating Cube with Color Change - Three.js

Here's an example of a rotating cube using Three.js, where the cube changes its color while rotating.
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Rotating Cube - Three.js</title>
    <style>
      body {
        margin: 0;
      }
      canvas {
        display: block;
      }
    </style>
  </head>
  <body>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
      // Set up the scene, camera, and renderer
      const scene = new THREE.Scene();
      const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
      const renderer = new THREE.WebGLRenderer();
      renderer.setSize(window.innerWidth, window.innerHeight);
      document.body.appendChild(renderer.domElement);

      // Create the cube geometry and material, then combine them to form a mesh
      const geometry = new THREE.BoxGeometry();
      const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
      const cube = new THREE.Mesh(geometry, material);
      scene.add(cube);

      // Position the camera
      camera.position.z = 5;

      // Create an animation loop to rotate the cube
      const animate = function () {
        requestAnimationFrame(animate);

        // Rotate the cube
        cube.rotation.x += 0.01;
        cube.rotation.y += 0.01;

        // Render the scene
        renderer.render(scene, camera);
      };

      // Start the animation loop
      animate();
    </script>
  </body>
</html>
