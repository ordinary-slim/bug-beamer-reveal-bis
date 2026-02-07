# Beamer reveal bug report:

## Instructions

```sh
# Any other compile should work. Note the .latexmkrc
# Should be reproducible without .latexmkrc, edit accordingly publish.sh
latexmk -pdf main
source publish.sh
```

## Bug

With newest version (BeamerReveal-20260205.0754), generated main.html has paths of slides as:
- data-background-image="website/main_files/media/Slides/slide-1.jpg"
, where website is the output directory.

The old version I had (20260130.1210) generated paths as:

- data-background-image="main_files/media/Slides/slide-1.jpg"

Moreover new version has:

// Loop the presentation
,

while old version had:
// Loop the presentation
loop: false,
