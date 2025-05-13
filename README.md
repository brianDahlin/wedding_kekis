# 🎉 Di & Art Wedding Website

**Invitation website for Artemiy & Diana's Wedding**

🌐 Domain: [diandart.xyz](https://diandart.xyz)

---

## 📖 Overview

This is a lightweight, single-page invitation website built with Vue 3 and Tailwind CSS. It showcases custom fonts, responsive layouts, and smooth animations. The site is hosted on AWS S3 and accelerated by Cloudflare.

## 🚀 Live Preview

Visit the live site at: [https://diandart.xyz](https://diandart.xyz)

## ✨ Features

* **Minimalist Design**: Emphasis on typography and color palette.
* **Responsive Layout**: Optimized for mobile, tablet, and desktop.
* **Vue 3**: Declarative components and reactive data binding.
* **Tailwind CSS**: Utility-first styling with custom font integration.
* **Swiper.js**: Continuous looping galleries and sliders.
* **Static Hosting**: Deployed on AWS S3 with Cloudflare DNS and HTTPS.

## 🛠 Tech Stack

* **Vue 3** (`vue@3.x`)
* **Tailwind CSS** (`tailwindcss@^3.x`)
* **Swiper.js** (`swiper@11`)
* **AWS S3** (Static Website Hosting)
* **Cloudflare** (DNS, CNAME flattening, SSL)

## 📦 Installation & Development

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/diandart-wedding.git
   cd diandart-wedding
   ```
2. Install dependencies:

   ```bash
   npm install
   ```
3. Run the development server:

   ```bash
   npm run dev
   ```
4. Open the site in your browser:

   ```
   http://localhost:3000
   ```

## 🏗️ Build

Generate a production-ready build:

```bash
npm run build
```

The compiled files will be placed in the `dist/` directory by default.

## ☁️ Deployment to AWS S3

1. Ensure AWS CLI is configured (`aws configure`).
2. Sync the build folder to your S3 bucket:

   ```bash
   aws s3 sync ./dist s3://diandart.xyz --delete
   ```
3. Enable **Static website hosting** on the S3 bucket (set `index.html` as the index document).
4. Configure DNS in Cloudflare:

   * Add a CNAME record for `@` pointing to `diandart.xyz.s3-website.<region>.amazonaws.com` (set to DNS only).
5. (Optional) Enable **Flexible SSL** and switch the CNAME to Proxied (orange cloud) for HTTPS support.

## 🔧 Configuration

* **fonts/**: Custom font files (RyukExtra, Inter).
* **public/images/**: Static image assets.
* **tailwind.config.js**: Tailwind theme customization.
* **.env**: Environment variables (if needed).

## 🤝 Contributing

We welcome contributions! Follow the workflow:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/my-feature`.
3. Commit your changes: `git commit -m 'Add new feature'`.
4. Push to your fork: `git push origin feature/my-feature`.
5. Open a Pull Request.

## 👤 Authors

* **Artemiy**

## 🏷 License

MIT License
