# Hugo Portfolio Template

*Modified version of the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) template.*

Website generated using this template: https://megh-khaire.github.io/

## Steps for using this template:

1. Install [Hugo](https://gohugo.io/installation/) on your machine.
2. Fork this repository.
3. Clone the fork locally:
    ```
    git clone https://github.com/<username>/hugo-portfolio-template.git
    ```
4. Setup the [PaperMod theme](portfolio/themes/README.md).
5. Create another github repository and with name: `<username>.github.io` .
   1. Example: https://github.com/megh-khaire/megh-khaire.github.io
   2. This new repository will contain all the static files that will be generated from the hugo template.
   3. We will use this repo as a submodule in the `hugo-portfolio-template` repository that we have previously setup.
6. To setup the submodule locally fire the following command from the `portfolio` directory in `hugo-portfolio-template` project:
    ```
    git submodule add -b main https://github.com/<username>/<username>.github.io.git public
    ```
    > Note if you get an error saying that the directory already exists please delete the `public` directory and retry the same command again.
7. Make the required changes to the template and set the `baseUrl` in config.toml file. *In the baseUrl just replace john-doe with your github username.*
8. Now that your submodule is setup use the following command to generate the static files:
    ```
    hugo -t hugo-PaperMod
    ```
9. From the `public` directory push the generated static files to the `<username>.github.io` repository and github will automatically deploy the HTML files to your [github website](https://pages.github.com/).
10. Whenever you add a new post or make changes to the template use `hugo -t hugo-PaperMod` to regenerate the static files.

## References:
All the steps mentioned above are illustrated in [this amazing video](https://youtu.be/LIFvgrRxdt4) by Ryan Schachte.