THREE.BloomBlendPass
=====================

Bloom blend effect for three.js.

![sample](https://raw.githubusercontent.com/mattatz/THREE.BloomBlendPass/master/Captures/after.png)

## Usage

This effect relies on THREE.EffectComposer.

```javascript

var composer = new THREE.EffectComposer();
composer.addPass(new THREE.RenderPass(scene, camera));

var bloomPass = new THREE.BloomBlendPass(
    2.0, // the amount of blur
    1.0, // interpolation(0.0 ~ 1.0) original image and bloomed image
    new THREE.Vector2(1024, 1024) // image resolution
);
bloomPass.renderToScreen = true;
composer.addPass(bloomPass);

composer.render();

```

## Example

![before](https://raw.githubusercontent.com/mattatz/THREE.BloomBlendPass/master/Captures/before.png)
![after](https://raw.githubusercontent.com/mattatz/THREE.BloomBlendPass/master/Captures/after.png)

