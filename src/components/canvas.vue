<script setup>
import * as THREE from "three";

// get the canvas element
const canvas = document.querySelector("canvas.webgl");

// To see something we need 4 elements
/**
 * Scene
 * Object
 * Camera
 * Renderer
 */

// Scene
const scene = new THREE.Scene();

// Object
/**
 * A visible object in three is called a mesh
 * Mesh is a combination of Geometry and Materials
 */
const geometry = new THREE.BoxGeometry(1, 1, 1);
const material = new THREE.MeshBasicMaterial({ color: 0xff0000 });
const mesh = new THREE.Mesh(geometry, material);

// add it to the scene
scene.add(mesh);

// for aspect ratio
const sizes = { height: 800, width: 800 };

// Camera
const camera = new THREE.PerspectiveCamera(75, sizes.height / sizes.width);

// add to scene
scene.add(camera);

// renderer
const renderer = new THREE.WebGLRenderer({ canvas });
</script>

<template>
  <div>
    <canvas class="webgl"></canvas>
  </div>
</template>
