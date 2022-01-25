## V. transforming effect patterns

## [] vs {}
-- compare how [,] and {,} work:
hush

- s "[voodoo voodoo:3, arpy arpy:4 arpy:2]"

- s "{voodoo voodoo:3, arpy arpy:4 arpy:2}"

- s "[drum bd hh bd, can can:2 can:3 can:4 can:2]"

- s "{drum bd hh bd, can can:2 can:3 can:4 can:2}"

- s "[bd sn, can:2 can:3 can:1, arpy arpy:1 arpy:2 arpy:3 arpy:5]"

- s "{bd sn, can:2 can:3 can:1, arpy arpy:1 arpy:2 arpy:3 arpy:5}"

-- ** cyclic / repetitive

- n "0 1 2 3" # sound "arpy"

- n (run 4) # sound "arpy"