# SK Tech Solutions Product Showcase

Separate animated product image gallery for the existing company website. Uses the supplied SK Tech logo and no stock imagery. Includes 15 product categories, search/filter, photo gallery, and image/document download controls.

## Free-first publishing
- Host the static site on GitHub Pages.
- Use Cloudinary Media Library as the simplest staff-managed image host to start. Staff sign in to the Cloudinary dashboard and upload company photos there; visitors only see photos whose URLs are added to the matching `photos` array in `index.html`.
- Add documents to the matching `downloads` array.
- The website deliberately has no public upload endpoint or exposed upload secret.

## Add a photo
Find the category in `index.html`, then change `photos:[]` to something like:
`photos:[{name:"Office cabin front view",url:"https://res.cloudinary.com/YOUR_CLOUD/image/upload/v123/your-image.jpg"}]`

## 1 GB storage note
Cloudinary Free has 25 monthly credits shared across managed storage, transformations, and image bandwidth; 1 credit equals 1 GB of each respective resource. 1 GB stored plus customer download traffic consumes credits, so check usage and image file limits before moving all assets. Free plan image size limits may require compressing individual large photos. See https://cloudinary.com/documentation/billing_and_plans and https://cloudinary.com/pricing.

## Publish
Upload `index.html`, `README.md`, `.nojekyll`, and `assets/sk-tech-logo.png` to a GitHub repository root, then enable Settings -> Pages -> Deploy from branch -> `main` -> `/(root)`.
