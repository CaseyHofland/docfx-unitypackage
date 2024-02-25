<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->



<div align="center">
  <!-- PROJECT LOGO -->
  <h2>DocFX Unity package</h2>

  ![docfx-unitypackage](https://github.com/CaseyHofland/docfx-unitypackage/assets/27729987/d4666aa7-6424-4b5f-9721-021402fb238e)
  
  <p>
    GitHub Action for deploying a DocFX website for Unity packages to Github Pages.
    <br/>
    <a href="https://github.com/CaseyHofland/docfx-unitypackage/issues">Report Bug</a>
    ·
    <a href="https://github.com/CaseyHofland/docfx-unitypackage/issues">Request Feature</a>
  </p>
  
  
  
  <!-- PROJECT SHIELDS -->
  [![MIT License][license-shield]][license-url]
  [![Release][release-shield]][release-url]
  [![Release Date][release-date-shield]][release-date-url]
</div>



<!-- ABOUT THE PROJECT -->
### About DocFX Unity package

DocFX Unity package is a GitHub action for deploying a DocFX website for Unity packages to GitHub Pages. These days, Unity maintains a lot of [optional packages](https://docs.unity3d.com/Manual/pack-safe.html) containing [great documentation](https://docs.unity3d.com/Packages/com.unity.cinemachine@2.9/manual/). This action's goal is to allow you to easily build documentation for Unity packages published on GitHub. It aims to mimic [Unity's documentation workflow][workflow-url] while keeping the native benefits of [DocFX][docfx-url].



<!-- Installation -->
## Installation

1. In the GitHub of your Unity package, create a branch called "gh-pages".
2. Go to the Settings tab, select "Pages" in the table on the left, then select "Deploy from a Branch" and select "gh-pages" as the branch to deploy from.
3. Go to the Actions tab, select "set up a workflow yourself", then copy and paste the following code:
```yaml
name: docfx-unitypackage

on:
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    permissions:
      contents: write

    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: true

      - name: Build
        uses: CaseyHofland/docfx-unitypackage@v1
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_branch: gh-pages
          publish_dir: _site
```

Every time you push to main, this action will run and your site will get automatically updated with any documentation or API changes.

### Prerequisites

Your repository should be a [Unity package](https://docs.unity3d.com/Manual/cus-layout.html).

Specifically, the root of your project should contain:
- `package.json`
- `CHANGELOG.md` [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
- either `LICENSE` or `LICENSE.md`
- either `README.md` or `Documentation~/index.md`



<!-- USAGE -->
## Usage

DocFX Unity package has been specifically designed to mimic the affordances and limitations of the [Package Manager DocTools@2.1][workflow-url]. In theory, you should be able to use the documentation of the version 2.1 tools and everything should work exactly the same, except for the following differences:
- DocFX Unity package is forgiving to beginners. All that is required by the [Package Manager DocTools@2.1][workflow-url] is optional, though strongly recommended.
- To add a custom logo and favicon to the generated website, add a file called `logo` and `favicon` inside the `Documentation~/images/` folder. The recommended logo height is 50px.
- When you don't have a `TableOfContents.md` in your `Documentation~`, the manual will be created without a table of contents. This may be preferrable for single-page documentation.
- [Unity's per-package metadata](https://docs.unity3d.com/Packages/com.unity.package-manager-doctools@2.1/manual/package-metadata.html), the values you can override in `projectMetadata.json`, are different from [DocFX's per-package metadata](https://dotnet.github.io/docfx/docs/template.html?tabs=modern#template-metadata).
- Currently, `config.json` does nothing and preprocessor directives are not generated.

If there are any other changes not listed here, please [open an issue][issues-url] to propose it be added to the docs.



<!-- RESOURCES -->
## Resources

### Documentation Guides

- [Package documentation guides](https://docs.unity.cn/Packages/com.unity.services.wire@1.1//manual/)
- [Documenting your package](https://docs.unity3d.com/Manual/cus-document.html)
- [Unity Style Guide](https://docs-style-guide.unity.com/)
- [Microsoft Style Guide](https://learn.microsoft.com/en-us/style-guide/welcome/)

### Examples

- [Unity Clock](https://caseyhofland.github.io/com.caseyhofland.unityclock/manual/)


<!-- ROADMAP -->
## Roadmap

**High Priority:**
- [x] Support preprocessor directives
- [ ] Unity API references
- [ ] Dependencies API references
- [ ] Versioned Documentation

**Low Priority:**
- [ ] Customization options

See the [open issues][issues-url] for a full list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are always appreciated. You may do so by forking the repo and creating a pull request, or by [opening an issue][issues-url].

1. Fork the Project
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a pull request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

### Casey Hofland

**Formal:** hofland.casey@gmail.com

**Informal:** [@CaseyHofland](https://mastodon.gamedev.place/@CaseyHofland)



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/CaseyHofland/docfx-unitypackage.svg
[license-url]: https://github.com/CaseyHofland/docfx-unitypackage/blob/master/LICENSE
[release-shield]: https://img.shields.io/github/release/CaseyHofland/docfx-unitypackage.svg
[release-url]: https://github.com/CaseyHofland/docfx-unitypackage/blob/master/releases/latest
[release-date-shield]: https://img.shields.io/github/release-date/CaseyHofland/docfx-unitypackage.svg
[release-date-url]: https://github.com/CaseyHofland/docfx-unitypackage/releases
[workflow-url]: https://docs.unity3d.com/Packages/com.unity.package-manager-doctools@2.1/manual/developer-notes.html#pmdt
[docfx-url]: https://dotnet.github.io/docfx/
[issues-url]: https://github.com/CaseyHofland/docfx-unitypackage/issues
