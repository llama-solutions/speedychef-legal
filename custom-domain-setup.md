# Custom Domain Setup for SpeedyChef Legal Pages

## Domain Options

### Option 1: Subdomain (Recommended)
- `legal.speedychef.com`
- `terms.speedychef.com` 
- `privacy.speedychef.com`

### Option 2: Separate Domain
- `speedychef-legal.com`
- `speedychef-terms.com`

### Option 3: Path on Existing Domain
- `yourcompany.com/legal` (requires different setup)

## Step-by-Step Setup

### Step 1: ✅ CNAME File Created
File: `/CNAME`
Content: `legal.speedychef.com` (replace with your domain)

### Step 2: DNS Configuration

#### For Subdomain (legal.speedychef.com):
```
Type: CNAME
Name: legal
Value: yourusername.github.io
TTL: 3600 (or Auto)
```

#### For Root Domain (speedychef-legal.com):
```
Type: A
Name: @ (or root)
Value: 185.199.108.153
Value: 185.199.109.153  
Value: 185.199.110.153
Value: 185.199.111.153
TTL: 3600 (or Auto)

Type: AAAA (IPv6, optional)
Name: @ (or root)
Value: 2606:50c0:8000::153
Value: 2606:50c0:8001::153
Value: 2606:50c0:8002::153
Value: 2606:50c0:8003::153
```

### Step 3: GitHub Pages Configuration
1. Go to your repository on GitHub
2. Settings → Pages
3. Custom domain: Enter your domain
4. Check "Enforce HTTPS" (after DNS propagates)
5. Save

### Step 4: Commit and Push CNAME File
```bash
cd /Users/nele/llama/SpeedyChef-Legal
git add CNAME
git commit -m "Add custom domain configuration"
git push origin main
```

## DNS Provider Examples

### Cloudflare
1. Dashboard → DNS → Records
2. Add CNAME record:
   - Type: CNAME
   - Name: legal
   - Target: yourusername.github.io
   - Proxy status: DNS only (gray cloud)

### GoDaddy
1. Domain Manager → DNS
2. Add Record:
   - Type: CNAME
   - Host: legal
   - Points to: yourusername.github.io
   - TTL: 1 Hour

### Namecheap
1. Domain List → Manage → Advanced DNS
2. Add New Record:
   - Type: CNAME Record
   - Host: legal
   - Value: yourusername.github.io
   - TTL: Automatic

### Google Domains
1. DNS → Custom resource records
2. Add:
   - Name: legal
   - Type: CNAME
   - TTL: 1H
   - Data: yourusername.github.io

## Verification Steps

### 1. DNS Propagation Check
```bash
# Check if DNS is working
dig legal.speedychef.com
nslookup legal.speedychef.com
```

### 2. Online Tools
- https://www.whatsmydns.net/
- https://dnschecker.org/

### 3. GitHub Pages Status
- Repository → Settings → Pages
- Should show "Your site is published at https://legal.speedychef.com"

## Troubleshooting

### Common Issues:
1. **DNS not propagated**: Wait 24-48 hours
2. **HTTPS not working**: Enable "Enforce HTTPS" after DNS works
3. **404 errors**: Check CNAME file content and GitHub Pages settings
4. **Certificate errors**: GitHub needs time to provision SSL (up to 24 hours)

### DNS Propagation Time:
- **Cloudflare**: 2-5 minutes
- **GoDaddy**: 1-24 hours  
- **Namecheap**: 30 minutes - 24 hours
- **Google Domains**: 10-15 minutes

## Security & Performance

### Enable HTTPS
- ✅ Automatic with GitHub Pages
- ✅ Free SSL certificate
- ✅ Force HTTPS redirect

### Performance Tips
- Use Cloudflare for CDN (optional)
- Enable browser caching
- Optimize images (already done)

## Final URL
After setup, your legal pages will be available at:
- https://legal.speedychef.com/
- Mobile-optimized ✅
- HTTPS secured ✅
- Fast loading ✅
