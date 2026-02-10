# Quick Setup Guide

## Getting Started and Preparing for Deployment

1. Open any modern web browser.
2. Open the **`index.html`** file to view the website locally. The website is ready to use immediately; **no build process is required.**
3. Upload all project files to your web hosting service to publish the website online.

## 🚀 Getting Started

### Static site (GitHub Pages compatible)

This is a **fully static** website. No Node.js, PHP, or database required.

- **Products** are stored in the browser's `localStorage` and managed via the admin dashboard.
- **Orders** are saved to `localStorage` when customers submit the checkout form.
- Open `admin/index.html` (or `yoursite.com/admin/` when deployed) to manage products and view orders.

**Note:** Orders and product edits are stored per-browser. When deployed to GitHub Pages, each visitor's cart and the admin's product/order data use that browser's storage. For production with shared data, consider a backend or third-party service.

### Step 1: Configure Order Submission (optional)

Orders are saved to `localStorage` and visible in the admin panel. For email notifications or external storage, you would need to integrate a service like Formspree or EmailJS (not included).

### Step 2: Test the Website

1. Open `index.html` in your browser
2. Click on a product
3. Select size, color, and quantity
4. Click "Add to Order"
5. Click the cart icon (🛒) in the header
6. Click "Proceed to Checkout"
7. Fill in the order form
8. Submit the order

### Step 3: Deploy

Upload all files to your web hosting:
- **Netlify**: Drag and drop the folder
- **Vercel**: Connect GitHub repo
- **GitHub Pages**: Push to repository
- **Any hosting**: Upload via FTP

## 📧 Testing Order Submission

1. Add products to cart and go to checkout
2. Fill in name, phone, and city
3. Submit the order — it saves to `localStorage`
4. Open the admin dashboard → الطلبات (Orders) to view the order

## 👤 Admin Dashboard (لوحة التحكم)

Manage products, orders, content, and design **without editing code**:

1. Open **`admin/index.html`** in your browser (or go to `yoursite.com/admin/` when deployed).
2. Log in with default password: **`admin123`**
3. Use the Arabic interface to:
   - **المنتجات** — Add, edit, delete products; set names, prices, descriptions, multiple images (drag to reorder), colors, sizes, and quantity per size/color; show or hide products.
   - **المخزون** — View stock levels and low-stock / out-of-stock alerts.
   - **الطلبات** — View orders, change status (Pending → Processing → Shipped → Delivered → Cancelled), view customer and item details.
   - **المحتوى** — Edit Home, About Us, and Contact page text and homepage banners.
   - **التصميم** — Change store accent color and show/hide website sections.

**Security:** To change the default password, open the browser console on the admin page, run `btoa('YourNewPassword')`, then in `assets/js/store.js` find where `passwordHash` is set and replace the value with the result (or edit the admin login check in `admin/admin.js` to use a different storage key).

All changes save to the browser's local storage and **apply immediately** on the live site when customers visit.

## 🔧 Customization

### Change Product Price
- Use the **Admin Dashboard** (المنتجات) to set regular and discount prices, or edit in store data.

### Add More Products
- Use the **Admin Dashboard** → المنتجات → إضافة منتج (Add product). No code editing needed.

### Change Colors
- Use **Admin Dashboard** → التصميم to set the accent color, or edit `:root { --accent: ... }` in `assets/css/styles.css`.

## 🌐 Language Support

The website supports English and Arabic:
- Arabic uses RTL (right-to-left) layout
- Language preference is saved in browser
- To add more languages, edit `assets/js/lang.js`

## 📱 Mobile Optimization

The website is fully responsive:
- Touch-optimized buttons
- Mobile-friendly forms
- Responsive cart modal
- Works on all screen sizes

## ❓ Troubleshooting

**Orders not appearing in admin?**
- Orders are stored in `localStorage` per browser — open admin in the same browser
- Check browser console for errors

**Cart not working?**
- Clear browser cache
- Check that `cart.js` is loaded
- Verify localStorage is enabled

**Styling issues?**
- Make sure `styles.css` and `cart.css` are loaded
- Check browser console for CSS errors

## 📞 Support

Need help? Contact:
- Email: black12tshirt@gmail.com
- Phone: +212 679 460 301
