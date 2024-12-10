# MyDecisive Docs on Hugo

The `public`, `resources`, and `static` directories are associated with local publication of the website and should be ignored when using GitPages. `.hugo_build.lock` should also be ignored.

The `archetypes` directory is a sort of template for the front matter of content pages that get created. The `layouts` directory is for HTML templates to control how pages are rendered.

Hugo's union file system means you override themes via a path from the root directory, not by editing theme files. See [this page](https://mcshelby.github.io/hugo-theme-relearn/configuration/sitemanagement/structure/index.html) for a clear explanation and an example.

## Images
Images are stored in an `images` directory on the same level as the content referencing those images. Look at the directory structure to see the pattern.

### tl;dr Why Do That?
Because Hugo looks at everything as a path, the "slug" (basically the end of the URL in human-readable form) is either presented as a "directory" (default, "pretty" URL) or as a file complete with file extension. This also depends on where a page is in the directory structure, whether it's treated as a section page or not.

Unfortunately the various ways Hugo handles generating the page URLs can play havoc with getting embedded image URLs to play nice. For example, even if an image is in a directory `images` that's on the same level as the file referencing that image, the file will have to reference the image this way: `../images/that_image.png`. 

 

## Resources

- [Hugo Docs](https://gohugo.io/documentation/)
- [Hugo learning resources](https://gohugo.io/getting-started/external-learning-resources/)
- Hugo Youtube tutorials: https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3
- Hugo community: See Hugo docs
- [hugo-book theme](https://github.com/alex-shpak/hugo-book?tab=readme-ov-file): A simple docs theme for Hugo. (Not using this theme as seems it's no longer being maintained.)
- The [Relearn](https://github.com/McShelby/hugo-theme-relearn) theme seems to be a well-maintained and well-documented theme that's relatively simple to use.
- More info about the Relearn theme at [this site](https://www.tshdmtmr.com/basics/migration/).
