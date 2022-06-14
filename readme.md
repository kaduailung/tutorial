# Web Development related notes
## The Picture Tag

HTML `<picture>` tag is used in responsive web designing
  where we need to load the different images based on their 
  viewport, height, width, orientation, and pixel density. 
  Picture tag give a developer more flexibility in specifying image resources.

example :

```html
<picture>
  <source media="(min-width:650px)" srcset="image.jpg">
  <source media="(min-width:465px)" srcset="img_white_flower.jpg">
  <img src="img_orange_flowers.jpg" alt="Flowers" style="width:auto;">
</picture>
```
---
### notes
  - it is advisable not to use the Picture tag just for `Resolution Switching` since the same can be achieved using the updated version of the `<Img>` tag.
  - Picture tag is the best option when we need to handle both `Resolution Switching` and `Art Direction` simultaneously.
  - The following example shows a complete example of using Art Direction and Resolution Switching using a `<picture>` tag.
    
    - ```html
      <picture>
     
         <source media="(orientation: landscape)"

            srcset="land-small-car-image.jpg 200w,
                    land-medium-car-image.jpg 600w,
                    land-large-car-image.jpg 1000w"

            sizes="(min-width: 700px) 500px,
                   (min-width: 600px) 400px,
                   100vw">

         <source media="(orientation: portrait)"

            srcset="port-small-car-image.jpg 700w,
                    port-medium-car-image.jpg 1200w,
                    port-large-car-image.jpg 1600w"

            sizes="(min-width: 768px) 700px,
                   (min-width: 1024px) 600px,
                   500px">

         <img src="land-medium-car-image.jpg" alt="Car">
      </picture>
      ```

