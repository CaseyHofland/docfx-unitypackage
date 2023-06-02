<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
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

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/CaseyHofland/docfx-unitypackage">
    <img src="images/logo.png" alt="Logo" width="400">
  </a>

<h3 align="center">DocFX Unity Package Action</h3>
  <p align="center">
    GitHub Action for deploying to GitHub Pages with DocFX for Unity packages
    <br/>
    <a href="https://github.com/CaseyHofland/docfx-unitypackage/issues">Report Bug</a>
    ·
    <a href="https://github.com/CaseyHofland/docfx-unitypackage/issues">Request Feature</a>
  </p>
</div>



<!-- PROJECT SHIELDS -->
[![MIT License][license-shield]][license-url]
[![Release][release-shield]][release-url]
[![Release Date][release-date-shield]][release-date-url]



<!-- ABOUT THE PROJECT -->
### About DocFX Unity Package Action

This is a gitHub action for deploying a DocFX website for Unity packages to Github Pages. These days, Unity maintains a lot of [optional packages](https://docs.unity3d.com/Manual/pack-safe.html) containing [great documentation](https://docs.unity3d.com/Packages/com.unity.cinemachine@2.9/manual/). This action aims to allow you to easily build documentation for Unity packages!

If your repository is already a Unity package, all you need to do follow the [installation guide](#installation)!

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

This section lays out how to get started with DocFX Unity Package Action.

### Prerequisites

Your repository should be a [Unity Package](https://docs.unity3d.com/Manual/cus-layout.html).

Specifically, the root of your project should contain:
- `package.json`
- `Changelog.md`
- `License.md`
-  either `README.md` or `Documentation~/index.md`

### Installation

1. In the github of your unity package, create a branch called "gh-pages" (the naming matters!).
2. Go to the Settings tab, select "Pages" in the table on the left, then select "Deploy from a Branch" and select "gh-pages" as the branch to deploy from.
3. Go to the Actions tab, then select "set up a workflow yourself" and find "docfx-unitypackage" in the marketplace.

![Build and Deployment](https://github.com/CaseyHofland/docfx-unitypackage/assets/27729987/52f5cded-f449-4238-9e52-50a52d6d30b6)

*Example of the correct settings for step 2*

Every time you push to main, this action will run and your site will get automatically updated with any documentation or api changes!

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Documentation~

The DocFX Unity Package Action has been specifically designed to mimic the affordances and limitations of the [Package Manager DocTools@2.1](https://docs.unity3d.com/Packages/com.unity.package-manager-doctools@2.1/manual/developer-notes.html#pmdt).

Logo and favicon

No toc

Auto docs

DocFX Freedom

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Unity API references
- [ ] Dependencies API references
- [ ] Versioned Documentation

See the [open issues](https://github.com/CaseyHofland/docfx-unitypackage/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



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

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Casey Hofland - [@CaseyHofland](https://mastodon.gamedev.place/@CaseyHofland) - hofland.casey@gmail.com

Project Link: [https://github.com/CaseyHofland/docfx-unitypackage](https://github.com/CaseyHofland/docfx-unitypackage)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/CaseyHofland/docfx-unitypackage.svg?style=for-the-badge
[license-url]: https://github.com/CaseyHofland/docfx-unitypackage/blob/master/LICENSE
[release-shield]: https://img.shields.io/github/release/CaseyHofland/docfx-unitypackage.svg?style=for-the-badge
[release-url]: https://github.com/CaseyHofland/docfx-unitypackage/blob/master/releases/latest
[release-date-shield]: https://img.shields.io/github/release-date/CaseyHofland/docfx-unitypackage.svg?style=for-the-badge
[release-date-url]: https://github.com/CaseyHofland/docfx-unitypackage/releases
