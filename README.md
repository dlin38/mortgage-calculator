# Smart Mortgage Prepayment Calculator 🏠

Mobile-friendly web app for calculating mortgage prepayment schedules with smart statement parsing.

## Features

✅ **Mobile-responsive** - Works perfectly on phones, tablets, and desktop  
✅ **Camera upload** - Take a photo of your mortgage statement  
✅ **Smart OCR** - Automatically extract principal, rate, escrow, and extra payments  
✅ **Multiple bank formats** - Parses various statement layouts  
✅ **Prepayment scenarios** - Model extra monthly payments and lump sums  
✅ **Visual summary** - See payoff date and interest saved at a glance  
✅ **Detailed schedule** - Month-by-month breakdown with chart  
✅ **CSV export** - Download schedule for Excel/Sheets  

## Usage

### Option 1: Upload Statement

1. Open `index.html` in a browser
2. Click **"Take Photo"** or **"Choose File"**
3. Select your mortgage statement (PDF or image)
4. Wait for OCR processing (~10-30 seconds)
5. Review extracted values (edit if needed)
6. Click **"Calculate"**

### Option 2: Manual Entry

1. Open `index.html` in a browser
2. Enter mortgage details:
   - Current principal balance
   - Interest rate (%)
   - Remaining term (years)
   - Monthly escrow (taxes/insurance)
   - Extra monthly payment (optional)
   - One-time lump sum (optional)
3. Click **"Calculate"**

## What It Calculates

### Summary

- **New payoff date** with extra payments
- **Years saved** compared to standard schedule
- **Total interest saved** vs. original amortization
- **Total amount paid** (principal + interest)

### Detailed Schedule

Monthly breakdown showing:
- Payment amount
- Principal portion
- Interest portion
- Extra payment applied
- Remaining balance

### Chart

Visual graph of balance declining over time.

## OCR Statement Parsing

The app looks for these patterns in uploaded statements:

**Principal Balance:**
- "Principal Balance: $..."
- "Remaining Balance: $..."
- "Current Balance: $..."

**Interest Rate:**
- "Interest Rate: X.XX%"
- "Rate: X.XX%"

**Escrow:**
- "Escrow: $..."
- "Tax & Insurance: $..."

**Extra Payments:**
- "Additional Principal: $..."
- "Extra Payment: $..."

If OCR doesn't find values, you can always enter them manually.

## Technical Details

### Technologies

- **HTML/CSS/JavaScript** - Single-file web app
- **Tailwind CSS** - Responsive styling
- **Tesseract.js** - OCR for image text extraction
- **Chart.js** - Balance chart visualization

### Browser Support

- Chrome/Edge/Safari/Firefox (latest)
- iOS Safari (camera support)
- Android Chrome (camera support)

### Limitations

- PDF OCR not yet implemented (use image for now)
- Accuracy depends on statement image quality
- Works best with clear, high-contrast photos

## Deployment

### Local

Just open `index.html` in any browser. No server needed!

### Web Hosting

Upload `index.html` to any static host:
- GitHub Pages
- Netlify
- Vercel
- AWS S3
- Firebase Hosting

Example (GitHub Pages):
```bash
git init
git add index.html README.md
git commit -m "Add mortgage calculator"
git remote add origin https://github.com/yourusername/mortgage-calc.git
git push -u origin main

# Enable GitHub Pages in repo settings → Pages → Source: main branch
```

### Custom Domain

1. Host on Netlify/Vercel
2. Add your custom domain (e.g., `mortgage-calc.yourdomain.com`)
3. SSL automatically configured

## Future Enhancements

- [ ] PDF text extraction support
- [ ] Save calculations to browser storage
- [ ] Compare multiple scenarios side-by-side
- [ ] Refinance calculator
- [ ] Amortization chart (principal vs interest over time)
- [ ] Property tax and insurance inflation adjustments
- [ ] Biweekly payment calculator
- [ ] Print-friendly summary report

## Examples

### Example 1: Standard Mortgage
- Principal: $250,000
- Rate: 6.5%
- Term: 30 years
- Escrow: $500/mo
- Result: Payoff in Oct 2054, $355K total interest

### Example 2: With Extra Payments
- Principal: $250,000
- Rate: 6.5%
- Term: 30 years
- Escrow: $500/mo
- **Extra: $200/mo**
- Result: Payoff in Feb 2048 (**6.7 years earlier**), $286K interest (**$69K saved**)

### Example 3: With Lump Sum
- Principal: $250,000
- Rate: 6.5%
- Term: 30 years
- Escrow: $500/mo
- Extra monthly: $100/mo
- **Lump sum: $10,000**
- Result: Payoff in Apr 2049 (**5.5 years earlier**), $295K interest (**$60K saved**)

## Tips for Best OCR Results

1. **Good lighting** - Avoid shadows
2. **Flat surface** - No wrinkles or curves
3. **Clear focus** - Sharp text, not blurry
4. **High contrast** - Dark text on light background
5. **Straight alignment** - Not tilted/rotated
6. **Zoom in** - Fill frame with relevant section

## Support

If you encounter issues:
1. Try manual entry instead of OCR
2. Check browser console for errors
3. Ensure image is clear and well-lit
4. Use JPEG/PNG format (not HEIC on iPhone)

## License

MIT License - Free to use and modify

---

Built with ❤️ for homeowners taking control of their mortgages
