

src stays for source dist stays for distribution

When installing a package that will be bundled into your production bundle, you should use npm install --save. If you're installing a package for development purposes (e.g. a linter, testing libraries, etc.) then you should use npm install --save-dev. More information can be found in the npm documentation.

GENERAL SETUP Our "original script" is inside the source directory. It has a dependency on the loadsh library, so it gets imported in the script using "import". Using webpack we will then bundle the original script with its dependencies, and the yield will be exported to the distribution directory with the name of main.js: for this reason, in the html file we will add the "<-script>" that points to main.js

With that said, let's run npx webpack, which will take our script at src/index.js as the entry point, and will generate dist/main.js as the output.
