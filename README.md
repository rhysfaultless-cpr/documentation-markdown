# Clearpath Robotics, Polaris GEM robotic platform

This repository is used to produce PDF manuals for the Clearpath Robotics, Polaris GEM robot platform.

## To produce a PDF:

1.  Make sure you have Node.js installed on your computer, by running:
    ```
    node -v
    ```
    [Download and install Node.js](https://nodejs.org/) if you do not have it yet.
2.  Clone this repository in VS Code.
3.  Open the repositiory in VS Code ( File -> Open Folder... )
4.  Open a new terminal, and run:
    ```
    npm install
    ```
    This will install all the dependencies listed in the _package.json_.
5.  Open the VS Code extensions area.
    Search or _Markdown PDF_, and install it.
    <center>
      <img src="/assets/images_readme/readme_1.png" width="800"/>
    </center>
6.  Open the file _/docs/main.md_
7.  Right click in the code window, and select _Markdown PDF: Export (pdf)_.
    <center>
      <img src="/assets/images_readme/readme_2.png" width="800"/>
    </center>
8.  The PDF _/docs/main.pdf_ will be updated.

## Making updates

1.  Follow the steps for how **To produce a PDF** to make sure you have the build tools.
2.  Create a feature branch describing your intended change.
3.  Open a terminal and run:
    ```
    npm run format
    ```
    This will run the Prettier code formatter based on the rules listed in _prettierrc.json_
4.  Make updates to:
    - _main.md_
    - Add new _.md_ files to the _/docs_ directory, then reference these new files inside _main.md_
    - Add images to the _/assets_ directory, then reference these new files inside a _.md_ file.
5.  Run the Prettier code formatter before commits, by running:
    ```
    npm run format
    ```
6.  Update the PDF, as described in the earlier section of this README.
7.  Add the changed files, commit, and push changes to the remote repository.
8.  Create a pull request and assign it to someone on the Clearpath Robotics team.

## Common elements:

1.  [Standard Markown elements](https://www.markdownguide.org/cheat-sheet/)
    - Headers with #, ##, etc
    - tables
    - bold, italics, strikethrough
    - [emojis](https://www.webfx.com/tools/emoji-cheat-sheet/)
    - unordered and ordered lists
    - horizontal rules
2.  Page breaks, by adding:
    ```html
    <div class="page" />
    ```
3.  Including other Markdown files, by adding:
    ```markdown
    :[include](file_name_to_be_included.md)
    ```
    This is a relative path, so it is best to save your markdown files in the same directory as main.md

A list of other Markdown PDF commands can be found at <https://github.com/alanshaw/markdown-pdf>
