# Have2Run Privacy Policy

This directory contains the privacy policy pages for Have2Run, designed to be hosted on GitHub Pages.

## Structure

```
privacy-policy/
├── index.html          # Korean privacy policy (default)
├── en/
│   └── index.html      # English privacy policy
├── css/
│   └── style.css       # Shared responsive styles
└── README.md           # This file
```

## Deployment to GitHub Pages

### Step 1: Create GitHub Repository

1. Create a new **public** repository on GitHub (required for GitHub Pages)
2. Recommended name: `have2run-privacy`

### Step 2: Push Files

```bash
# Navigate to this directory
cd privacy-policy

# Initialize git (if not already done)
git init

# Add all files
git add index.html en/index.html css/style.css README.md

# Commit
git commit -m "Initial privacy policy pages"

# Add remote (replace with your GitHub username)
git remote add origin https://github.com/[username]/have2run-privacy.git

# Push to main branch
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to repository Settings
2. Navigate to "Pages" section (left sidebar)
3. Under "Source", select branch: `main` and folder: `/ (root)`
4. Click "Save"
5. GitHub will build and deploy the site (takes 1-2 minutes)

### Step 4: Verify Deployment

After deployment, the privacy policy will be accessible at:

- **Korean (default):** `https://[username].github.io/have2run-privacy/`
- **English:** `https://[username].github.io/have2run-privacy/en/`

**Replace `[username]` with your actual GitHub username (e.g., `junddao`).**

### Expected URLs for Have2Run

If deployed to `junddao` account:

- Korean: `https://junddao.github.io/have2run-privacy/`
- English: `https://junddao.github.io/have2run-privacy/en/`

## Integration with App

### 1. Update Flavor Configuration

In `app/lib/core/config/flavors.dart`, update the `privatePolicyUrl`:

```dart
static String get privatePolicyUrl {
  return 'https://junddao.github.io/have2run-privacy/';
}
```

### 2. App Store / Play Store Submission

Use the **English version** URL for store submission forms:

- **Apple App Store Connect:** Privacy Policy URL field
- **Google Play Console:** Privacy Policy URL field

URL to submit: `https://junddao.github.io/have2run-privacy/en/`

### 3. In-App WebView

The privacy policy will be displayed in the app via `PrivacyPolicyPage` (implemented in Plan 76-02).

## Features

- **Bilingual:** Korean (default) and English versions
- **Mobile-responsive:** Optimized for mobile screens (used in Health Connect permission flow on Android)
- **Print-friendly:** Clean print styles for users who want to save a copy
- **No tracking:** No analytics or tracking scripts (respects user privacy)
- **Accessible:** Semantic HTML with proper heading hierarchy
- **Language switcher:** Easy navigation between Korean and English versions

## Updating the Policy

To update the privacy policy:

1. Edit `index.html` (Korean) and/or `en/index.html` (English)
2. Update the "Last Updated" date in both files
3. Commit and push changes to GitHub
4. GitHub Pages will automatically rebuild and deploy the updated version

## Compliance

This privacy policy covers:

- ✅ Korea PIPA (Personal Information Protection Act)
- ✅ Apple App Store privacy requirements
- ✅ Google Play Store privacy requirements
- ✅ Health Connect privacy policy requirements (Android 14+)

## Support

For privacy-related questions: [privacy@have2run.com](mailto:privacy@have2run.com)
