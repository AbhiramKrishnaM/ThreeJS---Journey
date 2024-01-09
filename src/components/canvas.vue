<script setup>
import * as THREE from "three";

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
screen.add(mesh);

// Camera
const camera = new THREE.PerspectiveCamera();
</script>

<template>
  <div>This is canvas</div>
</template>
