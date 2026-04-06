# KyvShield Web SDK — Example

Example web app demonstrating the KyvShield Web SDK for identity verification (KYC).

## Usage

Include the SDK via CDN, then call `KyvShield.initKyc()`:

```html
<script src="https://kyvshield-naruto.innolinkcloud.com/static/sdk/kyvshield.min.js"></script>

<script>
const result = await KyvShield.initKyc(
  {
    baseUrl: 'https://kyvshield-naruto.innolinkcloud.com',
    apiKey: 'YOUR_API_KEY',
    enableLog: true,
    theme: { primaryColor: '#EF8352', themeMode: 'light' },
  },
  {
    steps: ['selfie', 'recto', 'verso'],
    language: 'fr',
    showIntroPage: true,
    showInstructionPages: true,
    showResultPage: true,
    showSuccessPerStep: true,
    challengeMode: 'minimal',
    requireFaceMatch: true,
    target: selectedDocument,
  }
);

if (result.success) {
  console.log('KYC passed:', result.overallStatus);
}
</script>
```

## Running locally

Open `index.html` in a browser. The SDK requires HTTPS or localhost for camera access.

## API Documentation

Full documentation: **https://kyvshield-naruto.innolinkcloud.com/developer**

## License

BSD 3-Clause License.
