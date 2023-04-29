# Fuzzy-Pokédex 
### The Pokédex for your terminal
Simple fzf based Pokédex I built for my son to enjoy.

Parses results from [PokeAPI](pokeapi.co/) and feeds combined results from `pokemon-colorscripts` to `fzf`

![Screenshot](https://github.com/ericlay/fuzzy-pokedex/blob/main/screenshot.png?raw=true)

A very wonky preview:
[![asciicast](https://asciinema.org/a/581487.svg)](https://asciinema.org/a/581487)

## Install

Requires fzf, parallel, jq, espeak-ng, pokemon-colorscipts and, any nerd font; all else should be there

### Arch (and arch based)
```
$ git clone https://github.com/ericlay/fuzzy-pokedex.git
$ cd fuzzy-pokedex
$ makepkg -si
```
## Usage

```
Use fzf to search Pokemon stats 
Can optionally search by name

EXAMPLE
	pokedex [pokemon name]

OPTIONS
	-q, --quick [pokemon]
		Prints single Pokédex entry to terminal
	-u, --update [N/+N/-N/N%]
		Scrape web for updated Pokémon stats
		WARNING: update function is resource heavy
		See Parallel job control (-j) for options
		Default is 200%
	-h, --help
		Print this help screen

KEYBINDS
	space	Reads the Pokedex entry
	ctrl-space	Stops reading the Pokédex entry
	ctrl-n	Shows small sprite version
	ctrl-b	Shows large sprite version
	ctrl-s	Shows shiny sprite version
	ctrl-h	Shows this help screen in preview window
```

Credits to the great projects below: \
https://gitlab.com/phoneybadger/pokemon-colorscripts \
https://github.com/rmccorm4/Pokefetch 
 
## To-do
* [ ] Better arg parsing
* [ ] Refactor to allow user to choose local data source or from web
* [ ] Get sprites from `PokeAPI` if possible {PR WELCOME!}
* [ ] Work on TTS to read entries
* [ ] Add ability to filter on various attributes
