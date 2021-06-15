# Bookends-Obsidian Alfred Workflow

This is an Alfred workflow to generate a note in Obsidian from a Bookends reference. It is still in its early stages of design but is otherwise fully functional. 

![Example](https://raw.githubusercontent.com/oashour/bookends-obsidian-alfred/master/example.gif)

## Usage

1. Go to your bookends settings -> BiBTeX -> Enable BiBTeX
2. Generate a cite key for the references you want to create a note for in Obsidian (default shortcut: ⌘⇧K). This will be the title of the note.
3. Add the workflow to Alfred by downloading the .workflow file and double clicking it.
4. With the Workflow selected, click the [χ] icon on the right to set your environment variables.
  - `paperFolder` is the name of the folder where you want the notes stored inside your vault. This is just a folder name, not a path, e.g., `Papers`
  - `vaultName` is the name of your vault, e.g., `Notes`
  - `vaultPath` is the path to your vault, e.g., `/Users/ash/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes`
5. Open Bookends and select a reference. Activate Alfred and type beo. A note will be created with the name ${citekey} in the ${papersFolder} inside the vault ${vaultName}
  - If ${citeKey} is not set up, you will get an error notification and no note is created
  - If the note already exists, it will open in Obsidian (i.e. no duplicates are created as long as you don't rename the note or change the citekey).
  - If this is the first time creating a note, an obsidian:// link to the note will be placed in the notes section of the reference in Bookends.

## Issues and Contribution

This is a very early development workflow. I developed it for my own usage and this will be very opinionated. Feel free to fork it and modify it to suit your own needs. Alternatively, if you'd like to improve the workflow, I more than welcome pull requests (although presumably they're a little difficult with these .workflow files). If you have any problems or find any bugs, have feature suggestions, etc., please open an issue.
