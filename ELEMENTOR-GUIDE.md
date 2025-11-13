# How to Add Spectacle Section to WordPress Elementor

## Quick Start Guide

### Step 1: Add Required CSS Libraries

Add these in **WordPress Admin → Appearance → Customize → Additional CSS** or use a Header/Footer plugin:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css">
```

### Step 2: Add JavaScript Libraries

Add these before `</body>` tag using a Header/Footer plugin like **Insert Headers and Footers**:

```html
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
  var swiper = new Swiper('.edjs-swiper-carousel', {
    slidesPerView: 1,
    spaceBetween: 30,
    loop: true,
    autoplay: {
      delay: 3000,
      disableOnInteraction: false,
    },
    navigation: {
      nextEl: '#swiper-button-next',
      prevEl: '#swiper-button-prev',
    },
    breakpoints: {
      640: { slidesPerView: 1 },
      768: { slidesPerView: 2 },
      1024: { slidesPerView: 3 },
      1280: { slidesPerView: 4 },
    }
  });
});
</script>
```

### Step 3: Add HTML in Elementor

1. Open your page in **Elementor**
2. Add an **HTML Widget**
3. Paste the entire HTML section from `elementor-spectacle-section.html`
4. Update and publish!

## Alternative: All-in-One Code Block

If you prefer, you can copy everything from `elementor-spectacle-section.html` and paste it directly into an Elementor HTML widget. Make sure to:

1. Include the CSS `<style>` tags
2. Include the HTML section
3. Include the JavaScript `<script>` tags at the bottom

## Image URLs

All images are hosted on GitHub:
- Background: `https://raw.githubusercontent.com/imadonb9/edjss/main/assets/img/Asset%209%404x.png`
- Overlay: `https://raw.githubusercontent.com/imadonb9/edjss/main/assets/img/suii%203%404x.png`
- Spectacle images: In the same repository under `/assets/img/spectacles/`

## Customization

### Change Colors
Find `#BDCF00` in the CSS and replace with your brand color.

### Add More Spectacles
Copy a `<div class="swiper-slide">...</div>` block and modify:
- Image URL
- Spectacle name
- Date
- Link URL

### Adjust Carousel Speed
Change `delay: 3000` (3 seconds) to your preferred milliseconds.

## Troubleshooting

**Carousel not working?**
- Make sure Swiper JS is loaded
- Check browser console for errors
- Verify all closing tags are present

**Styles not applying?**
- Clear WordPress cache
- Clear Elementor cache
- Check if CSS is in correct location

**Links not opening?**
- Verify `target="_blank"` is present on `<a>` tags
- Check URLs are correct

## Support

For issues or customization help, check the full file: `elementor-spectacle-section.html`
