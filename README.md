# Archipelago Adventures Website

A static website for boat trip services in the Turku archipelago, Finland.

## Services

- **Fishing Trips**: Exclusive fishing expeditions for special groups in the pristine waters of the Turku archipelago
- **Seal Photography Tours**: Specialized tours for nature photographers to capture seals in their natural habitat

## Deployment to Google Cloud Storage

To deploy this static website to Google Cloud Storage:

1. Create a Google Cloud Storage bucket:
```bash
gsutil mb gs://your-bucket-name
```

2. Make the bucket publicly readable:
```bash
gsutil iam ch allUsers:objectViewer gs://your-bucket-name
```

3. Configure the bucket for website hosting:
```bash
gsutil web set -m index.html -e index.html gs://your-bucket-name
```

4. Upload the files:
```bash
gsutil -m cp -r index.html styles.css gs://your-bucket-name
```

5. Access your website at:
```
http://your-bucket-name.storage.googleapis.com
```

## Local Development

To test locally:
```bash
python3 -m http.server 8080
```

Then open http://localhost:8080 in your browser.

## Features

- Fully responsive design (mobile-friendly)
- Pure HTML/CSS (no JavaScript required)
- Optimized for static hosting
- Professional design with ocean theme
- Contact information included