# gitfiti

 _noun_ : Carefully crafted graffiti in a github commit history calendar.  

![screenshot of gitfiti](https://raw.github.com/gelstudios/gitfiti/master/gitfiti-screenshot.png "screenshot")

`gitfiti.py` is a tool to decorate your github account's commit history calendar by (blatantly) abusing git's ability to accept commits _in the past_.

How? `gitfiti.py` generates a script (powershell or bash) that makes commits with the `GIT_AUTHOR_DATE` and `GIT_COMMITTER_DATE` environment variables set for each targeted pixel.

Since this is likely to clobber repo's history, it is highly recommend that you create a _new_ github repo when using gitfiti.

## Pixel Art

![pixel art examples](https://raw.github.com/gelstudios/gitfiti/master/pixels-large.png "pixel art")  
Included "art" from left to right: kitty, oneup, oneup2, hackerschool, octocat, octocat2

## Usage

1. Create a new github repo to store your handiwork.
2. Run `gitfiti.py` and follow the prompts for username, art selection, offset, and repo name.
3. Run the generated `gitfiti.sh` or `gitfiti.ps1` from your home directory (or any non-git tracked dir) and watch it go to work.
4. Wait... Seriously, you'll probably need to wait a day or two for the gitfiti to show in your commit graph.

## User Templates

The file format for personal templates is the following:

1. Each template starts off with a ":" and then a name (eg. ":foo")
2. Each line after that is part of a json-recognizable array.
3. The array contain values 0-4, 0 being blank and 4 being dark green.
4. To add multiple templates, just add another name tag as described in 1.

For example:

```python
:center-blank
[[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,0,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1]]
```

This would output a 7 x 7 light green square with a single blank center square.

Once you have a file with templates, enter its name when prompted and the templates will be added to the list of options.

## Removal

Fortunately if you regret your gitfiti in the morning, removing it is fairly easy: delete the repo you created for your gitfiti (and wait).

## License

gitfiti is released under [The MIT license (MIT)](http://opensource.org/licenses/MIT)

## Notable derivatives or mentions

- [Vincent Van Git](https://github.com/jh3y/vincent-van-git) Vincent, which offers a [very slick web ui](https://vincent-van-git.netlify.app/) to generate a gitfiti script
- [github-calendar-customerizer](https://github.com/ZachSaucier/github-calendar-customizer) from ZachSaucier, another very [nice web GUI](https://codepen.io/ZachSaucier/full/PzVRBy) for generating gitfiti templates
- [git-art](https://github.com/jamesjarvis/git-art) from jamesjarvis, a work-alike web based [editor GUI](https://jamesjarvis.github.io/git-art/) that generates the script too
- [Pikesley's](https://github.com/pikesley) Pokrovsky, which offers Github History Vandalism [as a Service!](http://pokrovsky.herokuapp.com/)
- [PSVandalism](https://github.com/DenisBalan/PSVandalism) Wrapper around Pokrovsky, which makes possible vandalising Github History from Powershell
- [github-board](https://github.com/bayandin/github-board) commits gitfiti from easy templates
- [ghdecoy](https://github.com/tickelton/ghdecoy) fills the contribution graph with random data (sneaky!)
- [Gitfiti Painter](http://codepen.io/cbas/pen/vOXeKV) visual drawing tool for artists to easily create templates
- [git-draw](https://github.com/ben174/git-draw) a Chrome extension which will allow you to freely draw on your commit map(!)
- [github-jack](https://github.com/tardypad/github-jack) a pure bash version with space invaders and shining creepypasta
- [github-graffiti](https://github.com/mavrk/github-graffiti) a GUI editor with a bash script to allow custom designs on your commit map
- [Paint GitHub](https://paintgithub.com/) is the most convenient way to paint your GitHub contribution graph!
- [contribution-pixel-messages](https://github.com/abulvenz/contribution-pixel-messages) generates a date plan from an editable GUI
- Seen something else? Submit a pull request or open an issue!
