# SpeedyChef Legal Pages

This directory contains the legal documentation web pages for the SpeedyChef mobile application.

## Files

- `index.html` - Complete legal center with Terms & Conditions and Privacy Policy
- `README.md` - This documentation file

## Features

### Mobile-Friendly Design
- Responsive layout that works on all screen sizes
- Touch-friendly navigation buttons
- Optimized typography for mobile reading
- Smooth scrolling and transitions

### Content Sections
1. **Home** - Overview of SpeedyChef and legal documents
2. **Terms & Conditions** - Complete terms of service
3. **Privacy Policy** - Comprehensive privacy policy

### Key Legal Coverage

#### Terms & Conditions
- Service description and features
- Device and Apple ID responsibility
- Premium subscription (SpeedyChef Pro) details
- Acceptable use policies
- AI-generated content disclaimers
- Intellectual property rights
- Liability limitations
- Termination policies

#### Privacy Policy
- Data collection practices
- Information usage and sharing
- Third-party services (AI, Analytics, Ads)
- Data security measures
- User rights and choices
- Children's privacy protection
- International data transfers

## Contact

- **Developer:** Nenad Biocanin
- **Email:** llama.solutions@icloud.com

## Deployment

This is a static HTML page that can be hosted on any web server:

1. **GitHub Pages** - Upload to a GitHub repository and enable Pages
2. **Netlify** - Drag and drop the folder to Netlify
3. **Vercel** - Deploy directly from this folder
4. **Traditional Web Hosting** - Upload files via FTP/SFTP

## Mobile Optimization

The page includes several mobile-friendly features:

- Viewport meta tag for proper mobile scaling
- Flexible CSS Grid and Flexbox layouts
- Touch-friendly button sizes (minimum 44px)
- Readable font sizes on small screens
- Optimized spacing and padding for mobile
- Smooth scrolling and transitions
- Backdrop blur effects for modern mobile browsers

## Legal Compliance

This template covers common legal requirements for mobile apps:

- GDPR compliance considerations
- CCPA privacy requirements
- App Store legal requirements
- Subscription billing disclosures
- AI service usage disclaimers
- Advertising and analytics disclosures

## Usage in App

You can link to these pages from your iOS app using:

```swift
// Open legal pages in Safari
if let url = URL(string: "https://speedychef.llama.solutions/") {
    UIApplication.shared.open(url)
}
```

Or embed in a WKWebView for in-app viewing.
