# Complete Guide: Using Spectacle Section as iFrame in Elementor

## 🎯 Benefits of iFrame Approach
- ✅ No WordPress/Elementor CSS conflicts
- ✅ Works independently
- ✅ Can scroll parent page even with mouse on iframe
- ✅ Links work perfectly
- ✅ Easy to update (just update GitHub file)

---

## 📋 Step 1: Enable GitHub Pages

1. Go to your GitHub repo: https://github.com/imadonb9/edjss
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select **main** branch
5. Click **Save**
6. Wait 1-2 minutes for deployment
7. Your page will be available at: `https://imadonb9.github.io/edjss/`

---

## 📋 Step 2: Get the iFrame URL

Once GitHub Pages is enabled, your spectacle section will be accessible at:

```
https://imadonb9.github.io/edjss/elementor-spectacle-FINAL.html
```

---

## 📋 Step 3: Add to Elementor

### Option A: Smart Scroll-Through iFrame (Recommended)

Copy this code into an **Elementor HTML Widget**:

```html
<style>
.spectacle-iframe-wrapper {
  position: relative;
  width: 100%;
  min-height: 700px;
  overflow: visible;
}

.spectacle-iframe {
  width: 100%;
  height: 700px;
  border: none;
  display: block;
  transition: opacity 0.2s ease;
}

/* Allow page scroll by default */
.spectacle-iframe-wrapper .spectacle-iframe {
  pointer-events: none;
}

/* Enable interactions on hover */
.spectacle-iframe-wrapper:hover .spectacle-iframe {
  pointer-events: auto;
}
</style>

<div class="spectacle-iframe-wrapper">
  <iframe 
    class="spectacle-iframe"
    src="https://imadonb9.github.io/edjss/elementor-spectacle-FINAL.html"
    scrolling="no"
    frameborder="0"
    allow="autoplay">
  </iframe>
</div>
```

### Option B: Simple iFrame (Alternative)

If Option A doesn't work well, use this simpler version:

```html
<iframe 
  src="https://imadonb9.github.io/edjss/elementor-spectacle-FINAL.html"
  width="100%" 
  height="700" 
  frameborder="0"
  scrolling="no"
  style="border: none; display: block;">
</iframe>
```

---

## 🔧 Adjusting Height

If you need to change the height:

**Option A**: Change `700px` to your desired height
**Option B**: Use `height="800"` or whatever height you need

---

## 🎨 Customization

To update the spectacle section:

1. Edit `elementor-spectacle-FINAL.html` in your repo
2. Commit and push changes
3. Wait 1-2 minutes for GitHub Pages to update
4. Refresh your WordPress page - changes appear automatically!

---

## 🐛 Troubleshooting

### iFrame not showing?
- Make sure GitHub Pages is enabled
- Check the URL is correct
- Wait 2-3 minutes after enabling GitHub Pages

### Can't scroll the page?
- Use **Option A** (Smart Scroll-Through)
- Move mouse away from iframe to scroll page
- Hover over iframe to interact with carousel

### Links not working?
- Hover over the iframe first
- Click the link
- Links open in new tabs automatically

### Height not right?
- Adjust the `height` value in the code
- Try `700px`, `800px`, or `auto`

---

## 📱 Mobile Optimization

The iframe is fully responsive and will adjust automatically on mobile devices.

---

## 🚀 Quick Test

After setting up, test these:
1. ✅ Can you scroll your WordPress page with mouse over iframe?
2. ✅ When you hover, can you click carousel arrows?
3. ✅ Do spectacle links open in new tabs?
4. ✅ Does carousel auto-play?

If all ✅, you're done! 🎉

---

## 📞 Need Help?

Check that:
- GitHub Pages is enabled
- URL is correct: `https://imadonb9.github.io/edjss/elementor-spectacle-FINAL.html`
- Code is pasted in Elementor HTML Widget
- Page is published/updated
