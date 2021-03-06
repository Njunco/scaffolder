# scaffolder

Based on `browser-template`

A template for starting front-end projects. Webpack for `require` system, build
pipeline, and development server. Boostrap and Handlebars.js included. No
front-end frameworks included.

## Installation

1.  [Download](../../archive/master.zip) this template. **Do not clone.** We will be modifying the template files before creating a repository.
1.  Unzip and rename the template directory with a suitable project name. Use hyphens to separate words in the project name; e.g., `playlist-editor`.
1.  Empty [`README.md`](README.md) and fill with your own content.
1.  Replace all instances of `scaffolder` with the name of your project.
1.  Move into the new project's directory and `git init`. _Note:_ This command converts the directory into a Git repository.
1.  Add all of the files in your project with the command `git add -A`
  -   *Note:* THIS IS THE ONLY TIME YOU SHOULD RUN THIS COMMAND WITH THE -A SWITCH
1.  Commit all of your files with the command `git commit`
  -   Your commit title should read `Initial commit`
1.  Install dependencies with `npm install`.

## Structure

Developers should store JavaScript files in [`assets/scripts`](assets/scripts).
The "manifest" or entry-point is
[`assets/scripts/index.js`](assets/scripts/index.js). In general, only
application initialization goes in this file. It's normal for developers to
start putting all code in this file, but encourage them to break out different
responsibilities and use the `require` syntax put references where they're
needed.

Developers should set `config.apiOrigins.production` (and `config.apiOrigins.development` if it differs from the default).  With `apiOrigins` set, developers may rely on `config.apiOrigin` as the base for API URLs.

Developers should store styles in [`assets/styles`](assets/styles) and load them from [`assets/styles/index.scss`](assets/styles/index.scss).

Developers should use [getFormFields](forms.md) to retrieve form data to send to an API.

To deploy a browser-template based SPA, run `grunt deploy`.

## Tasks

Developers should run these often!

-   `grunt nag` or just `grunt`: runs code quality analysis tools on your code
    and complains
-   `grunt make-standard`: reformats all your code in the JavaScript Standard Style
-   `grunt <server|serve|s>`: generates bundles, watches, and livereloads
-   `grunt test`: runs any automated tests, depends on `grunt build`
-   `grunt build`: place bundled styles and scripts where `index.html` can find
    them

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
