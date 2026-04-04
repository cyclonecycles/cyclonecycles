# Photos

Drop shop photos into this folder, then update the Gallery section in `index.html`.

## Good shots to get
- The shop floor / front entrance (with the new address visible if possible)
- Bikes currently in inventory (used bikes sell fast with photos)
- Sunday crawfish boil / BBQ gatherings
- Mark working on a bike
- Close-ups of cool parts or builds

## How to add photos to the page

In `index.html`, find the `#gallery` section and replace the placeholder `<div class="gallery-placeholder">` block with something like:

```html
<div class="gallery-grid">
  <img src="photos/shop-front.jpg" alt="Cyclone Cycles storefront on Bellaire Blvd" />
  <img src="photos/sunday-bbq.jpg" alt="Sunday BBQ at the shop" />
  <!-- add more as needed -->
</div>
```

And add this CSS in the `<style>` block:

```css
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}
.gallery-grid img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
```

## File naming tips
- Use lowercase, no spaces: `shop-front.jpg`, `sunday-crawfish.jpg`
- JPEGs are fine; aim for under 500KB per image for fast loading
- Netlify serves these directly — no special config needed
