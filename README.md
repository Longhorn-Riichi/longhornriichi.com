## longhornriichi.com

Longhorn Riichi's website built with Jekyll!

Custom domain: [longhornriichi.com](https://longhornriichi.com/)

CloudFlare production hostname: [longhornriichi.pages.dev](https://longhornriichi.pages.dev/)

CloudFlare preview hostname: [dev.longhornriichi.pages.dev](http://dev.longhornriichi.pages.dev/)

## Testing Locally
Get [all the requirements for Jekyll](https://jekyllrb.com/docs/). Then:
```
bundle install
bundle exec jekyll serve
```
Useful options: `--livereload` `--host=0.0.0.0`.

## Repository Structure:
Developers should be most interested in the following:
- `/_data/`: content that is better stored as lists of values (`.json`) or a dictionary of key-value pairs (`.yml`) (as opposed to a `.md` article).
- `/_include/`: `.html` components that may be reused across different layouts.
- `/_layouts/`: the [Jekyll layouts](https://jekyllrb.com/docs/step-by-step/04-layouts/).
- `/_sass/components/`: the style sheets for various components.
- `/assets/css/style.scss`: the style sheet entry point that defines some thematic variables and imports the above `components` style sheets.

## Notes

- The optimal width of the images in the content is `700px` (see [`page.html`](/_layouts/page.html)).

## Credits
- Theme template: [Jekyll Serif Theme](https://github.com/zerostaticthemes/jekyll-serif-theme)
- Illustrations: [いらすとや](https://www.irasutoya.com/)
