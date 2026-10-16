# Wire Cut Study

A drawing made only by cutting. Drag a wire across the plate, the pieces come loose and
slowly drift away.

## Running it

Open `index.html` in a browser. That is the whole thing.

For local work with correct font loading, serve it rather than opening the file directly:

    python3 -m http.server 8000

Then visit http://localhost:8000

## Controls

| Action | Mouse or touch | Key |
| --- | --- | --- |
| Cut | Drag from bare ground | |
| Move a piece | Drag the piece | |
| Nudge loose pieces | Tap bare ground | |
| Cut tool | | C |
| Hold tool, no cutting | | H |
| Drift, Fall, Still | | 1, 2, 3 |
| Random colours | | X |
| Gather the pieces | | G |
| New plate | | N |
| Close the panel | | Escape |

## Deploying

Static hosting, single file.
