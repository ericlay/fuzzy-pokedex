# Fuzzy-Pokedex
Very simple fzf based pokedex I built for my son to enjoy

![Screenshot](https://github.com/ericlay/fuzzy-pokedex/blob/main/screenshot.png?raw=true)

Requires fzf, parallel, jq, espeak-ng, pokemon-colorscipts and, any nerd font; all else should be there

```
Use fzf to search Pokemon stats 
Can optionally search by name

EXAMPLE
	pokedex [pokemon name]

OPTIONS
	-q, --quick [pokemon]
		Prints single pokedex entry to terminal
	-u, --update [N/+N/-N/N%]
		Scrape web for updated Pokemon stats
		WARNING: update function is resource heavy
		See Parallel job control (-j) for options
		Default is 200%
	-h, --help
		Print this help screen

KEYBINDS
	space	Reads the Pokedex entry
	ctrl-space	Stops reading the Pokedex entry
	ctrl-n	Shows small sprite version
	ctrl-b	Shows large sprite version
	ctrl-s	Shows shiny sprite version
	ctrl-h	Shows this help screen in preview window
```

Credits to the great projects below in which do most the heavy lifting: \
https://gitlab.com/phoneybadger/pokemon-colorscripts \
https://github.com/rmccorm4/Pokefetch 
 
## To-do
* [ ] Better arg parsing
* [ ] Rewrite to use `PokeAPI` as data source {Dev Branch 60%}
* [ ] Refactor to allow user to choose local data source or from web
* [ ] Get sprites from `PokeAPI` if possible {PR WELCOME!}
* [ ] Work on TTS to read entries
* [ ] Add ability to filter on various attributes
