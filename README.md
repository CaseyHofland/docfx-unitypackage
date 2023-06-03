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
  <h2>DocFX Unity Package Action</h2>

  <a href="https://github.com/CaseyHofland/docfx-unitypackage">
    <img src="https://github.com/CaseyHofland/docfx-unitypackage/assets/27729987/26e90342-31a0-4e6d-a119-b6c7e385d321" alt="Logo" width="400">
  </a>
  
  <p>
    GitHub Action for deploying to GitHub Pages with DocFX for Unity packages
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
### About DocFX Unity Package Action

This is a gitHub action for deploying a DocFX website for Unity packages to Github Pages. These days, Unity maintains a lot of [optional packages](https://docs.unity3d.com/Manual/pack-safe.html) containing [great documentation](https://docs.unity3d.com/Packages/com.unity.cinemachine@2.9/manual/). This action's goal is to allow you to easily build documentation for Unity packages published on github. It aims to mimic [Unity's documentation workflow][workflow-url] while keeping the native benefits of [DocFX][docfx-url].



<!-- Installation -->
## Installation

1. In the github of your unity package, create a branch called "gh-pages" (the naming matters!).
2. Go to the Settings tab, select "Pages" in the table on the left, then select "Deploy from a Branch" and select "gh-pages" as the branch to deploy from.
3. Go to the Actions tab, then select "set up a workflow yourself" and find "docfx-unitypackage" in the marketplace.

Every time you push to main, this action will run and your site will get automatically updated with any documentation or api changes!

### Prerequisites

Your repository should be a [Unity Package](https://docs.unity3d.com/Manual/cus-layout.html).

Specifically, the root of your project should contain:
- `package.json`
- `CHANGELOG.md` [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
- either `LICENSE` or `LICENSE.md`
- either `README.md` or `Documentation~/index.md`



<!-- USAGE -->
## Usage

The DocFX Unity Package Action has been specifically designed to mimic the affordances and limitations of the [Package Manager DocTools@2.1][workflow-url]. In theory, you should be able to use the documentation of the version 2.1 tools and everything should work exactly the same, except for the following differences:
- DocFX Unity Package Action is forgiving to beginners. All that is required by the [Package Manager DocTools@2.1][workflow-url] is recommended, but optional.
- To add a custom logo and favicon to the generated website, add a file called `logo` and `favicon` inside the `Documentation~/images/` folder. The recommended logo height is 50px.
- When you don't have a `TableOfContents.md` in your `Documentation~`, the manual will be created without a table of contents. This may be preferrable for single-page documentation.
- [Unity's per-package metadata](https://docs.unity3d.com/Packages/com.unity.package-manager-doctools@2.1/manual/package-metadata.html), the values you can override in `projectMetadata.json`, are different from [DocFX's per-package metadata](https://dotnet.github.io/docfx/docs/template.html?tabs=modern#template-metadata).

If there are any other changes not listed here, please [open an issue](https://github.com/CaseyHofland/docfx-unitypackage/issues) to propose it be added to the docs.



<!-- RESOURCES -->
## Resources

### Documentation Guides

- [Package documentation guides](https://docs.unity.cn/Packages/com.unity.services.wire@1.1//manual/)
- [Documenting your package](https://docs.unity3d.com/Manual/cus-document.html)
- [Unity Style Guide](https://docs-style-guide.unity.com/)
- [Microsoft Style Guide](https://learn.microsoft.com/en-us/style-guide/welcome/)

### Examples

- [Unity Clock](https://github.com/CaseyHofland/com.caseyhofland.unityclock)


<!-- ROADMAP -->
## Roadmap

**High Priority:**
- [ ] Unity API references
- [ ] Dependencies API references
- [ ] Versioned Documentation

**Low Priority:**
- [ ] Add customization options

See the [open issues](https://github.com/CaseyHofland/docfx-unitypackage/issues) for a full list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



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
