# Email UI Extension Pack

## Introduction

This extension pack is a collection of VS Code settings and extensions that have been put together specifically to get you up and coding as an Email UI Developer as quickly as possible.

While nothing in here is mandatory, I guarantee that these will improve your efficiency in coding and help reduce errors.

---
## Installation

1. Clone this repo to your computer and name it `vscode-email-resources`.
2. Open the Extensions panel in VS Code by clicking the 4-block icon in the sidebar menu.
3. Click the `...` at the top of the Extensions panel to access more options.
4. Select the `Open from VSIX...` option.
5. Navigate to the `extension-pack` folder in the `vscode-email-resources` repo, open the release folder and choose the latest release version. 

---
## Recommended Settings
You may choose to adhoc the below settings if you wish. However, if you'd like to add these as well as a few settings to enhance the editor, then drop these [settings](https://github.com/chrismith77/vscode-email-resources/blob/main/user-settings/settings.json) into your user settings.json in VS Code. Some settings can be changed to match your preferences so look through all the settings before adding them to yours.

If you add the font family setting then be sure you download and install the [Cascadia Code](https://github.com/microsoft/cascadia-code/releases) font.


#### Code Spell Checker
Update which languages the Code Spell Checker extension will check and add in some default words to the user library. User words are ignored by the spell checker. You can add more words to this list as needed.

```json
{
  "cSpell.enabledLanguageIds": [
    "asciidoc", "astro",
    "c", "cpp", "csharp", "css",
    "erb",
    "git-commit", "go", "graphql",
    "handlebars", "haskell", "html",
    "jade", "java", "javascript", "javascriptreact", "json", "jsonc", "jupyter",
    "latex", "less",
    "markdown",
    "php", "plaintext", "python", "pug",
    "restructuredtext", "ruby", "rust",
    "scala", "scss",
    "text", "typescript", "typescriptreact",
    "yaml", "yml",
    "xml"
  ],
  "cSpell.userWords": [
    "ampscript", "apothic", "arcsize", "arial", "astro",
    "bgcolor", "bspace", "busname",
    "cellpadding", "cellspacing", "codesnippetblock", "concat",
    "degdigital",
    "eacute", "emailaddr", "euml", "extracss",
    "gmail", "grizz", "grizzlemail", "gsub", "gulpfile",
    "helvetica",
    "itemprop", "itemscope", "itemtype",
    "lspace",
    "monospace", "mso", "museo",
    "nbsp", "nowrap",
    "oneasics", "OOTB", "opencounter",
    "pardot", "pcss", "pinterest", "precss", "preheader",
    "roboto", "roundrect", "rspace", "runat",
    "samsungfix", "sfmc", "smsb", "strokecolor", "strokeweight", "stylelint", "stylesheet", "stylesheets",
    "templating", "textbox", "tspace",
    "unsub",
    "valign", "vawp",
    "webmail", "websafe", "wordmark",
    "xmlns",
    "youtube",
    "zwnj"
  ],
}
```

#### Colorize
Update which languages the Colorize extension will work with.

```json
{
  "colorize.languages": [
    "ampscript",
    "astro",
    "css",
    "erb",
    "handlebars", "html",
    "javascript", "json",
    "less",
    "nunjucks",
    "postcss",
    "ruby",
    "sass", "scss", "sss", "svg",
    "typescript",
    "xml",
    "yaml"
  ],
}
```

#### HTMLHint
Disables the warning that the file is missing a doctype. Since our email content block files don't have a doctype this is a setting you don't want to overlook.

```json
{
  "htmlhint.options": {
    "doctype-first": false
  },
}
```

#### Live Server
Set a default browser for Live Server to open in and disable info pop-ups. Feel free to change the browser to your favorite.

```json
{
  "liveServer.settings.CustomBrowser": "firefox",
  "liveServer.settings.donotShowInfoMsg": true,
  "liveServer.settings.donotVerifyTags": true,
}
```

#### Prettier
The build tool has it's own set of Prettier options set when you build files. These will help ensure that the repo code stays consistent between developers.

```json
"prettier.documentSelectors": ["**/*.astro"],
"prettier.printWidth": 110,
"prettier.singleAttributePerLine": false,
"prettier.singleQuote": true,
"[astro]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.language.brackets": [
    ["%%[", "]%%"],
    ["<%", "%>"]
  ],
  "editor.language.colorizedBracketPairs": [
    ["%%[", "]%%"],
    ["<%", "%>"]
  ]
},
```

#### Project Manager
Tell the Project Manager extension where you keep your project repos at. You can add multiple folder locations and Project Manager will compile all the repos into one list. The locations are dependent on where you are saving your repos. Here are a few example locations (notice how you need to escape the backslash with another backslash).

```json
{
  "projectManager.any.baseFolders": [
    "~\\AppData\\Roaming\\Code\\User",
    "c:\\\\repos",
    "$home\\repos",
    "$home\\Library\\Application Support\\Code\\User",
    "e:\\\\repos",
    "~\\dev"
  ],
}
```

---
## Included Extensions
While all of these extensions are installed with this extensions pack, there are certain ones that are more of a personal preference. Feel free to uninstall the ones you don't want. Should you want to lighten your extension library, I've broken them up into catagories: [Keep](#markdown-header-keep) | [Consider Keeping](#markdown-header-consider-keeping) | [Meh](#markdown-header-meh) | [Themes](#markdown-header-themes)

### Keep
Unless you just enjoy making things harder on yourself.

#### [Astro](https://marketplace.visualstudio.com/items?itemName=astro-build.astro-vscode)
This extension provides all kinds of support for .astro files ... I wouldn't run Astro without it, trust me.

[![Astro (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/astro-build.astro-vscode.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=astro-build.astro-vscode)

---
#### [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
Misspelled words are bad um'k.

[![Code Spell Checker (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/streetsidesoftware.code-spell-checker.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

---
#### [HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)
Adds CSS Intellisense for HTML. Hate Intellisense? Then you're probably not a fan of VS Code anyway.

[![HTML CSS Support (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/ecmel.vscode-html-css.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)

---
#### [HTMLHint](https://marketplace.visualstudio.com/items?itemName=htmlhint.vscode-htmlhint)
An HTML code linter. We write HTML, nuff said.

[![HTMLHint (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/htmlhint.vscode-htmlhint.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=htmlhint.vscode-htmlhint)

---
#### [GitLab Workflow](https://marketplace.visualstudio.com/items?itemName=gitlab.gitlab-workflow)
Adds GitLab support to VS Code. I'm sure it will come in useful one day. 

[![GitLab Workflow (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/gitlab.gitlab-workflow.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=gitlab.gitlab-workflow)

---
#### [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
Provides you a visual representation of the branch tree. It's also pretty handy at easily allowing you to revert, cherry pick, rebase, and a whole bunch more. 

[![GIT Lens (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/mhutchie.git-graph.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)

---
#### [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
Adds feature rich functionality to the built-in Git capabilities of VS Code. Quickly glimpse into whom, why, and when a line of code was changed.

[![GIT Lens (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/eamodio.gitlens.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

---
#### [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
What's better than clean code? Consistently formatted code. Prettier is opinionated so you can't control everything that it does ... just embrace it and it will set you free.

[![Prettier (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/esbenp.prettier-vscode.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)


---
#### [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)
Easily access project repo folders from VS Code. Yeah, no more navigating through directories or dealing with Open Folder commands. Just click on the project folder, select a repo and profit ... you're welcome.

[![Project Manager (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/alefragnani.project-manager.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

---
#### [Red Hat Commons](https://marketplace.visualstudio.com/items?itemName=chrisvltn.redhat.vscode-commons)
A base utility for Red Hat extensions. This is installed with the YAML extension. Gotta have it if you want to have the [YAML](#markdown-header-yaml) extension.

[![Red Hat Commons (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/chrisvltn.redhat.vscode-commons.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=chrisvltn.redhat.vscode-commons)

---
#### [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
Adds comprehensive YAML language support. Let's face it, even with a new build tool we will likely still deal with YAML files. So you're gonna want this one.

[![YAML (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/redhat.vscode-yaml.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

---
### Consider keeping
These extensions will make your day-to-day coding a lot more enjoyable. Would you miss them if you never used them, probably not ... but I would encourage you to try them out before uninstalling. 

#### [Advanced New File](https://marketplace.visualstudio.com/items?itemName=patbenatar.advanced-new-file)
Allows you to create files anywhere in your workspace. Takes a bit to get used to using, but once you get the hang of it you'll realize the potential. This one's great for stretching your VS Code Command Pallet muscles.

[![Advanced New File (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/patbenatar.advanced-new-file.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=patbenatar.advanced-new-file)

---
#### [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
Automatically rename paired HTML/XML tags. Like, when you updated your `<h1>` to an `<h2>` and forget to rename the closing tag. Avoid that embarrassment forever.

[![Auto Rename Tag (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/formulahendry.auto-rename-tag.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)

---
#### [Character Count](https://marketplace.visualstudio.com/items?itemName=stevensona.character-count)
Adds a character count of your selected text/code in the VS Code status bar. Want to know how many characters that giant block of CSS is? Then wonder no more.

[![Colorize (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/stevensona.character-count.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=stevensona.character-count)

---
#### [Colorize](https://marketplace.visualstudio.com/items?itemName=kamikillerto.vscode-colorize)
Color values are given a background color of the same value. Gives you a visual of what the color is and helps you quickly identify where colors are set in your code. 

[![Colorize (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/kamikillerto.vscode-colorize.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=kamikillerto.vscode-colorize)

---
#### [CSS Peek](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek)
View and edit CSS within your HTML/ERB files. If your 🤯 , then you're not doing it right.

[![CSS Peek (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/pranaygp.vscode-css-peek.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek)

---
#### [Duplicate](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-duplicate)
Easily duplicate files and directories using the Explorer right-click menu. Similar to [Advanced New File](#markdown-header-advanced-new-file) but not handled in the VS Code Command Pallet.

[![Duplicate (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/mrmlnc.vscode-duplicate.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-duplicate)

---
#### [Filesize](https://marketplace.visualstudio.com/items?itemName=mkxml.vscode-filesize)
Displays the size of focused file within the status bar. No more navigating to a file in the Windows Explorer or Finder to see what the size of your file is.

[![Filesize (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/mkxml.vscode-filesize.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=mkxml.vscode-filesize)

---
#### [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)
A convenient way of creating, moving, renaming, and deleting files or directories using the VS Code Command Pallet.

[![File Utils (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/sleistner.vscode-fileutils.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)

---
#### [HTML End Tag Labels](https://marketplace.visualstudio.com/items?itemName=anteprimorac.html-end-tag-labels)
Labels the HTML end tag with the class or ID used on the opening tag. Probably not the end of the world if you don't like this one. But it sure does come in handy for those bigger blocks of code.

[![HTML End Tag Labels (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/anteprimorac.html-end-tag-labels.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=anteprimorac.html-end-tag-labels)

---
#### [Indented Block Highlighting](https://marketplace.visualstudio.com/items?itemName=byi8220.indented-block-highlighting)
Highlights the entire block of indented code that you are editing. True, this only benefits you if you indent your code ... which begs the question, are you indenting your code?

[![Indented Block Highlighting (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/byi8220.indented-block-highlighting.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=byi8220.indented-block-highlighting)

---
#### [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
Preview markdown files in VS Code. I know, not everyone is affectionate towards markdown. However, if you find yourself wanting or needing to write some markdown, then this extension gives you a real-time preview of what it might look like.

[![Markdown Preview Enhanced (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/shd101wyy.markdown-preview-enhanced.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)

---
#### [Open In Browser](https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser)
Adds an "Open in browser" feature to the Explorer right-click menu. Cause sometimes you gotta check stuff out in a browser, amirite?

[![Open In Browser (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/techer.open-in-browser.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser)

---
### Meh
The following extensions are a little more situational depending on your coding style/preferences and what type of coding language you are dealing with. These offer minor conveniences that would likely not be missed by most. 

#### [AMPscript Language](https://marketplace.visualstudio.com/items?itemName=xnerd.ampscript-language)
Syntax Highlighting for AMPscript language. Would probably be better if we were dealing with HTML files in our build tool, ERB doesn't play so nice. Handy for straight AMPscript files though.

[![AMPscript Language (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/xnerd.ampscript-language.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=xnerd.ampscript-language)

---
#### [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
Gives you the ability to add bookmarks in your code, allowing you to move within or between files quicker. It takes a bit of getting used to, but once you do you quickly jump around in your project.

[![Bookmarks (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/alefragnani.Bookmarks.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)

---
#### [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
Launch a local dev server with live reload. Our build tool takes care of local server testing, but sometimes you're working outside of the build tool. This extension makes it so that you can fire off a local server to test out the one-off HTML pages.

[![Live Server (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/ritwickdey.LiveServer.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

---
#### [Semicolon Insertion Shortcut](https://marketplace.visualstudio.com/items?itemName=chrisvltn.vs-code-semicolon-insertion)
Adds a shortcut to insert a semicolon at the end of a line. Doesn't sound like a big deal, until you start writing a bunch of Javascript and realize why this extension was created.

[![Semicolon Insertion Shortcut (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/chrisvltn.vs-code-semicolon-insertion.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=chrisvltn.vs-code-semicolon-insertion)


---
### Themes
The settings in this extension pack will use the Moonlight theme and Material Icon Theme. However, themes are definitely a personal preference, so I won't take it personally if you don't like these options.

Why even include them you ask? Because picking themes can be overwhelming, so I thought I'd throw out a couple of my favorites. 

Don't underestimate a good theme, it will vastly improve your coding experience. Visit [vscodethemes](https://vscodethemes.com/) to find the theme that speaks to you.

#### [Moonlight Theme](https://marketplace.visualstudio.com/items?itemName=atomiks.moonlight)
A dark color theme with bubblegum colors.

[![Moonlight Theme (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/atomiks.moonlight.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=atomiks.moonlight)

---
#### [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
Adds easily identifiable icons to folders. They'er a love'em or hate'em kind of thing ... you decided which camp you're in.

[![Material Icon Theme (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/PKief.material-icon-theme.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)

---
#### [Noctis Theme](https://marketplace.visualstudio.com/items?itemName=itemName=liviuschera.noctis)
A collection of light and dark themes with a good balance of warm and cold colors.

[![Noctis (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/itemName=liviuschera.noctis.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=itemName=liviuschera.noctis)