# presenting_ivim.vim

**presenting_ivim.vim** is a vim plugin that turns your markup into presentable
slides (in ivim).

This is cloned version from 'presenting.vim' repository.
Cloned repository [presenting.vim](https://github.com/sotte/presenting.vim)

**ivim** it's vim version for ios, with some capabilities like pure python packages and lua scripting, and with really little shell.
As it's not possible to work as usual linux-flavour system, in the case of **presenting.vim** it's not possible to use __figlet__, so I have changed to use python version that could be installed through :!pip install pyfiglet.

I have also solved some issues related to some tags from the original cloned version. I have also changed some fonts when using different headers.

**Summary**
- Changed figlet by pyfiglet
- Arranged some tags with tables and header3
- Different figlet fonts for header1/header2/header3
- width adapted for my personal use in my ipad-air using mono nerd font (Anonymice 17.0)

Here you have original and cloned README.md file

------------------------


It is a clone of [present.vim][1] which is a clone of [presen.vim][2]. In
contrast to its predecessors, presenting.vim:

  [1]: https://github.com/pct/present.vim
  [2]: https://github.com/sorah/presen.vim

  * has support for common markup languages,
  * can be extended, and
  * is documented

Great, hey?

## Demonstrations
Here is what the `examples/PresentingDemo.rst` file looks like when presented.

![presenting.vim RST demo](examples/demo.gif)

Markdown files are rendered a bit more fancifully. Be sure to read the help file. Here is the `examples/PresentingDemo.markdown` being presented.

![presenting.vim Markdown demo](examples/FancyMarkdown.gif)

## Installation

Use [pathogen][3] or [vundle][4] to install presenting.vim.

  [3]: https://github.com/tpope/vim-pathogen
  [4]: https://github.com/gmarik/vundle

## Configuration

Simply write your presentation in your favorite markup language. Every slide
is separated by a markup language specific marker.

|   Filetype   | Slide Separator |
| ------------ | --------------- |
| markdown     | `# heading`     |
| rst          | `~~~~`          |
| orgmode      | `#----`         |
| GoLang slide | `* title`       |


These can be overridden or extended by setting `b:presenting_slide_separator`
for your preferred filetype in your `.vimrc`. For example, set the `.rst` slide
separator to `~~~~` via:

```viml
au FileType rst let b:presenting_slide_separator = '\v(^|\n)\~{4,}'
```

## Usage

When you want to start presenting, execute
```
:PresentingStart
```

It is possible to have multiple presentations running at the same time. Just
run the command in each source document, and each slide show will be
displayed in its own tab.

Once presenting, slide navigation is accomplished via these keys:

| Key | Action         |
| --- | -------------- |
| `n` | next slide     |
| `p` | previous slide |
| `q` | quit           |

## Examples

For examples of presenting.vim presentations, see:

  * [PresentingExample.markdown](https://github.com/sotte/presenting.vim/blob/master/examples/PresentingDemo.markdown)
  * [PresentingExample.rst](https://github.com/sotte/presenting.vim/blob/master/examples/PresentingDemo.rst)
  * [PresentingExample.org](https://github.com/sotte/presenting.vim/blob/master/examples/PresentingDemo.org)
  * [PresentingExample.slide](https://github.com/sotte/presenting.vim/blob/master/examples/PresentingDemo.slide)

Of course you can configure the slide separators.

## Contributing

The [code][5] and [issue tracker][6] are on github. Pull requests are welcome!

  [5]: https://github.com/sotte/presenting.vim
  [6]: https://github.com/sotte/presenting.vim/issues
