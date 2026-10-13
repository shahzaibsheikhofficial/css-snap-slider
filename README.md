# CSS Snap Slider Edit

A **CSS-only** responsive slider. On desktop your row stays exactly as it is. On tablet and mobile the same row turns into a smooth, swipeable slider that snaps **one item at a time**, like the product sliders on modern stores.

**No JavaScript. No libraries. One small CSS file.**

### 👉 [Live Demo](https://shahzaibsheikhofficial.github.io/css-snap-slider/)

---

## Features

- Pure CSS, with zero JavaScript, so it is lightweight and fast
- Desktop layout stays untouched
- Smooth swipe with one-item-at-a-time snapping on tablet and mobile
- Hidden scrollbar for a clean look
- Works with any row of items: products, posts, reviews, team cards and more
- Easy to use in WordPress, Elementor, WooCommerce or any plain HTML site

## How it works

The slider uses the CSS **scroll snap** feature. The row becomes a horizontal scroll container (`overflow-x: auto`), and every item is told where to snap (`scroll-snap-align: start`). The CSS only applies at tablet and mobile breakpoints, so desktop is not affected.

## Usage

### 1. Add the wrapper class

Add the class `snap-slider` to the section that wraps your row.

```html
<div class="snap-slider">
  <div class="slider-track">
    <div class="slider-item">Item 1</div>
    <div class="slider-item">Item 2</div>
    <div class="slider-item">Item 3</div>
  </div>
</div>
```

| Class | What it is |
|---|---|
| `.snap-slider` | The wrapper around your row |
| `.slider-track` | The row that holds all the items |
| `.slider-item` | Each single item inside the row |

### 2. Use your own class names

Replace `.slider-track` and `.slider-item` in the CSS with the classes of your own row and items. For example, in WordPress you would use the row class and item class that your theme or builder already gives you.

### 3. Add the CSS inside the tablet and mobile breakpoints

Copy the code from [`snap-slider.css`](snap-slider.css) and paste it **inside your tablet and mobile breakpoints only**:

```css
@media (max-width: 1024px) {
  /* paste the CSS from snap-slider.css here */
}
```

Desktop keeps your normal row. That's it.

### Adjusting item width

In `.slider-item`, change `min-width`:

- `75%` shows one item with a peek of the next (good for mobile)
- `45%` shows about two items (good for tablet)

## Using it in WordPress

1. Open the page in **Elementor** and select the section that wraps your row.
2. Go to **Advanced → CSS Classes** and add `snap-slider`.
3. Paste the CSS (with your class names) into **Appearance → Customize → Additional CSS**, or into Elementor's **Custom CSS**, inside the tablet and mobile breakpoints.

## Browser support

Works in all modern browsers: Chrome, Edge, Safari, Firefox and mobile browsers. The scrollbar-hiding rules use both `scrollbar-width` and `::-webkit-scrollbar` to cover all of them.

## Notes

- Mouse dragging is not possible with CSS alone. The slider is designed for **touch swiping** on tablets and phones. On a desktop browser, use a trackpad or touch screen.
- `!important` on `justify-content` is only there to beat theme styles. Remove it if you don't need it.

## Project files

| File | Purpose |
|---|---|
| `snap-slider.css` | The slider CSS |
| `index.html` | Live demo page |
| `README.md` | This file |

## License

Released under the [MIT License](LICENSE). Free to use in personal and client projects. Please keep the license notice.

## Author

**Shahzaib Sheikh**, Web Developer

🌐 [Portfolio](https://shahzaibsheikhofficial.github.io) · ✉️ itengineer3258786@gmail.com
