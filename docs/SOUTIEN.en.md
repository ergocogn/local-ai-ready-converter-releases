# Support and ads in the app

[Lire en français](SOUTIEN.md) · [Home](../README.md)

Local AI-Ready Converter can display a **Support the project** area on the main screen. Giving the repository a GitHub star is **free** and is not a payment. The [Support via Stripe](https://buy.stripe.com/8x214pgIZ7ho3vUftg1oI00) button opens the payment provider in your browser; the app never processes a payment itself. It does not infer an amount: only an explicitly labelled button pointing to a matching payment page should suggest one.

If a real ad is configured in a future build, it replaces this card in the same space and is labelled **Advertisement**. The ad is an image bundled with that installed version and an HTTPS link. The app does not fetch an ad-network script or remote image on every display. Clicking opens the link in your browser. Changing the image or destination requires a new app version.

![The area with a fictional ad](assets/annonce-demo.png)

*Illustration only: a generated demo image, with no real advertiser or campaign.*

The first-run walkthrough and Settings let you hide the entire area. The choice is saved locally. Conversion works with or without it. See [privacy and network use](CONFIDENTIALITE.en.md).

**What about a GitHub Sponsor button?** GitHub documents a `.github/FUNDING.yml` file that can point to a custom support URL, including Stripe. However, [GitHub's documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository) presents it for open-source projects. Because this product's code is proprietary, we will not enable that repository button before clarifying eligibility with GitHub. The Stripe links in the README and app do not depend on it.
