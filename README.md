# Fuzzy-Pokedex
Very simple fzf based pokedex I built for my son to enjoy

![Screenshot](https://github.com/ericlay/fuzzy-pokedex/blob/main/screenshot.png?raw=true)

Requires BeautifulSoup4, fzf, parallel, espeak-ng, pokemon-colorscipts and, any nerd font; all else should be there

Credits to the great projects below in which do most the heavy lifting: \
https://gitlab.com/phoneybadger/pokemon-colorscripts \
https://github.com/rmccorm4/Pokefetch 
 
## To-do

* [ ] Rewrite arg parsing loop
* [ ] Drop `echo`, use `printf` instead
* [ ] Rewrite to use `PokeAPI` as data source
* [ ] Refactor to allow user to choose local data source or from web
* [ ] Get sprites from `PokeAPI` if possible
* [ ] Work on TTS to read entries
* [ ] Add `ripgrep` to filter on various attributes
