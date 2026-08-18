# hermes-pets

Custom pets for [Hermes Agent](https://github.com/NousResearch/hermes-agent).

A collection of custom pets. Each one lives in its own folder.

Pets are just a mascot on screen. They don't change how the agent thinks or how many tokens it uses.

## Install a pet

Each pet in this repo is one folder. Copy that whole folder into Hermes. Don't dump the files loose. The folder name is the pet's slug.

Hermes looks here:

**Mac and Linux**

```
~/.hermes/pets/
```

**Windows**

```
%LOCALAPPDATA%\hermes\pets\
```

If you use a named Hermes profile, put it under that profile instead:

```
~/.hermes/profiles/<name>/pets/
```

You want this layout (S0uthpaw as an example):

```
pets/
  s0uthpaw/
    pet.json
    spritesheet.webp
```

Then tell Hermes to use it. Swap in the folder name:

```
hermes pets select s0uthpaw
```

Or, inside a running session:

```
/pet s0uthpaw
```

Preview it in the terminal with:

```
hermes pets show s0uthpaw
```

If nothing shows up, run `hermes pets doctor`. A pet only appears after the folder is in place and you've selected it.

## What's in the folder

| File | What it is |
| --- | --- |
| `pet.json` | Name, description, and path to the spritesheet |
| `spritesheet.webp` | Animation frames (8 by 9 grid of 192 by 208 cells) |
