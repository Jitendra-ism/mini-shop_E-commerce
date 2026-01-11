# How to Add New Products to Your eCommerce Website

## 🎯 Quick Method: Edit the Products File

### Step 1: Open the Products File
Navigate to `src/data/products.ts` - this file contains all your products.

### Step 2: Add Your New Product
Copy this template and add it to the `products` array:

```typescript
{
  id: 'p10', // Make this unique (p10, p11, etc.)
  name: 'Your Product Name',
  price: 99.99,
  originalPrice: 129.99, // Optional - shows "Sale" badge
  image: 'https://images.pexels.com/photos/your-image-url',
  description: 'Write a compelling product description here',
  category: 'clothes', // Must be: clothes, shoes, or accessories
  subcategory: 'your-subcategory',
  rating: 4.5,
  reviews: 100,
  inStock: true,
  features: ['Feature 1', 'Feature 2'], // Optional
  colors: ['Red', 'Blue'], // Optional
  sizes: ['S', 'M', 'L'] // Optional
}
```

### Step 3: Save and See Changes
The website will automatically update when you save the file!

## 📸 Finding Product Images

### Free Stock Photos (Recommended):
- **Pexels**: https://www.pexels.com/
- **Unsplash**: https://unsplash.com/
- **Pixabay**: https://pixabay.com/

### How to Get Image URLs:
1. Find your product image on Pexels
2. Right-click the image
3. Select "Copy image address"
4. Paste the URL in the `image` field

## 🛍️ Product Examples

### Adding a New T-Shirt:
```typescript
{
  id: 'c4',
  name: 'Vintage Band T-Shirt',
  price: 24.99,
  originalPrice: 34.99,
  image: 'https://images.pexels.com/photos/8532616/pexels-photo-8532616.jpeg',
  description: 'Retro-style band t-shirt with vintage graphics. Soft cotton blend for ultimate comfort.',
  category: 'clothes',
  subcategory: 't-shirts',
  rating: 4.3,
  reviews: 87,
  inStock: true,
  features: ['Vintage Design', 'Soft Cotton Blend', 'Comfortable Fit'],
  colors: ['Black', 'White', 'Gray'],
  sizes: ['XS', 'S', 'M', 'L', 'XL', 'XXL']
}
```

### Adding New Sneakers:
```typescript
{
  id: 's4',
  name: 'High-Top Canvas Sneakers',
  price: 89.99,
  image: 'https://images.pexels.com/photos/1598508/pexels-photo-1598508.jpeg',
  description: 'Classic high-top sneakers with canvas upper and rubber sole. Perfect for casual wear.',
  category: 'shoes',
  subcategory: 'sneakers',
  rating: 4.4,
  reviews: 156,
  inStock: true,
  features: ['Canvas Upper', 'Rubber Sole', 'Lace-Up Closure', 'Padded Collar'],
  colors: ['White', 'Black', 'Red', 'Navy'],
  sizes: ['6', '7', '8', '9', '10', '11', '12']
}
```

### Adding a New Accessory:
```typescript
{
  id: 'a4',
  name: 'Wireless Bluetooth Headphones',
  price: 149.99,
  originalPrice: 199.99,
  image: 'https://images.pexels.com/photos/3394650/pexels-photo-3394650.jpeg',
  description: 'Premium wireless headphones with noise cancellation and 30-hour battery life.',
  category: 'accessories',
  subcategory: 'electronics',
  rating: 4.7,
  reviews: 312,
  inStock: true,
  features: ['Noise Cancellation', '30-Hour Battery', 'Wireless Bluetooth', 'Premium Sound'],
  colors: ['Black', 'White', 'Silver'],
  sizes: ['One Size']
}
```

## 🎨 Advanced Product Features

### Multiple Images:
```typescript
images: [
  'https://images.pexels.com/photos/image1.jpg',
  'https://images.pexels.com/photos/image2.jpg',
  'https://images.pexels.com/photos/image3.jpg'
]
```

### Sale Items:
```typescript
price: 79.99,
originalPrice: 99.99, // Shows "Sale" badge and crossed-out price
```

### Out of Stock:
```typescript
inStock: false, // Shows "Out of Stock" overlay
```

## 🔄 Adding New Categories

### Step 1: Add to Categories Array
In the same file, find the `categories` array and add:

```typescript
{
  id: 'electronics',
  name: 'Electronics',
  image: 'https://images.pexels.com/photos/your-category-image.jpg',
  subcategories: ['headphones', 'phones', 'tablets']
}
```

### Step 2: Update Navigation
Edit `src/components/Header.tsx` to add the new category button:

```typescript
<button
  onClick={() => onNavigate({ currentPage: 'products', selectedCategory: 'electronics' })}
  className="text-sm font-medium transition-colors text-slate-600 hover:text-slate-800"
>
  Electronics
</button>
```

## ✅ Checklist for Adding Products

- [ ] Unique ID (no duplicates)
- [ ] Clear, descriptive name
- [ ] Competitive pricing
- [ ] High-quality image URL
- [ ] Compelling description
- [ ] Correct category
- [ ] Realistic rating (1-5)
- [ ] Review count
- [ ] Stock status
- [ ] Optional: Colors, sizes, features

## 🚀 Pro Tips

1. **Consistent Naming**: Use clear, searchable product names
2. **Good Images**: High-quality, well-lit product photos work best
3. **Detailed Descriptions**: Help customers understand what they're buying
4. **Realistic Ratings**: Keep ratings between 3.5-5.0 for credibility
5. **Stock Management**: Set `inStock: false` for unavailable items
6. **Categories**: Stick to existing categories or add new ones properly

## 🔧 Testing Your New Products

After adding products:
1. Save the file
2. Check the homepage for featured products
3. Navigate to the category page
4. Click on your new product
5. Test adding to cart
6. Verify all details display correctly

Your new products will appear immediately on the website!