<template>
  <div>
    <md-card md-with-hover>
      <md-ripple>
        <md-card-content>
          <md-list>
            <div class="md-title">Please select an object:</div>
            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Cube"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Cube</span>
            </md-list-item>

             <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Cone"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Cone</span>
            </md-list-item>

             <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Cylinder"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Cylinder</span>
            </md-list-item>

            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Sphere"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Sphere</span>
            </md-list-item>

            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Square"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Square</span>
            </md-list-item>

            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Circle"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Circle</span>
            </md-list-item>

            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Ring"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Ring</span>
            </md-list-item>

            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="Octahedron"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">Octahedron</span>
            </md-list-item>

            <md-list-item>
              <md-radio
                v-model="threeGeometry"
                value="TorusKnot"
                @change="changeGeometry"
                class="md-primary"
              />
              <span class="md-list-item-text">TorusKnot</span>
            </md-list-item>

          </md-list>
        </md-card-content>
      </md-ripple>
    </md-card>
  </div>
</template>

<script>
export default {
  name: "configurator",
  data: () => ({
    threeGeometry: ""
  }),
  methods: {
    changeGeometry() {
      this.$emit("geometryChanged", this.threeGeometry);
    }
  }
};
</script>

<style scoped>
.md-card {
  position: relative;
  width: 99.9%;
  box-sizing: border-box;
  margin: 4px;
  display: block;
  vertical-align: top;
}
.md-card-content {
  width: inherit;
}
.md-card-header {
  text-align: left;
}
.md-title {
  font-size: 14px !important;
}
.md-list {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  width: inherit;
}
</style>
