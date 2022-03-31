<template>
  <div>
    <div v-for="image in images" :key="image.id" class="fl w-50 w-25-l pa1 overflow-hidden">
      <cld-image :public-id="image.publicId" class="grow" sign-url="true">
        <cld-transformation height="750" width="750" crop="crop" />
        <cld-transformation :overlay="image.overlay" />
        <cld-transformation effect="style_transfer" flags="layer_apply" />
      </cld-image>
    </div>
  </div>
</template>

<script>
import images from "~/utils/images.json";

export default {
  data() {
    return {
      images
    }
  }
}
</script>