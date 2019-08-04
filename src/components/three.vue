<template>
    <div>
        <Config v-on:geometryChanged="changeGeo" />
        <div id="webGL"></div>
        </div>
</template>

<script>
import Config from "./configurator";
import * as THREE from "three";


export default {
  name: "three",
  components: {
    Config
  },
  data() {
    return {
      renderer: null,
      scene: null,
      camera: null,
      mesh: null,
      container: null,
      threeGeometry: "Sphere",
      geometryVariable: {
        Cube: new THREE.BoxGeometry(1, 1, 1),
        Sphere: new THREE.SphereGeometry(1, 32, 32),
        Square: new THREE.PlaneGeometry(2, 2, 32),
        Circle: new THREE.CircleGeometry(1, 32)
      }
    };
  },
  methods: {
    init() {
      this.container = document.getElementById("webGL");
      this.scene = new THREE.Scene();
      this.camera = new THREE.PerspectiveCamera(
        75,
        this.container.clientWidth / this.container.clientHeight,
        0.1,
        1000
      );
      this.renderer = new THREE.WebGLRenderer();
      this.renderer.setSize(
        this.container.clientWidth,
        this.container.clientHeight
      );
      this.container.appendChild(this.renderer.domElement);

      this.camera.position.set(0, 0, 5);

      this.animate();
    },
    animate() {
      requestAnimationFrame(this.animate);
    if(this.mesh) {
      this.mesh.rotation.x += 0.01;
      this.mesh.rotation.y += 0.01;
    }
      

      this.renderer.render(this.scene, this.camera);
    },

    removeShape() {
      this.scene.remove(this.mesh);
      this.mesh.geometry.dispose();
      this.mesh.material.dispose();
      this.mesh = undefined;
   
    },
    changeGeo(e){
      if(this.mesh) this.removeShape();
      this.threeGeometry = e;
      let geometry = this.geometryVariable[e];
      let material = new THREE.MeshNormalMaterial();
      this.mesh = new THREE.Mesh(geometry, material);
      this.scene.add(this.mesh)
      }
  },
  mounted() {
    this.init();
  }
};
</script>

<style>
#webGL {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}

</style>
