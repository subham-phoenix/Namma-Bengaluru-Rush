# Namma Bengaluru Rush

A tiny open-world Bengaluru that runs in the browser. Drive an auto-rickshaw, race the Purple Line, play gully cricket in Cubbon Park, chase a phone thief through KR Market, run a pub quiz on Church Street, make the airport run and deliver a hot masala dosa. Eight missions, traffic that obeys signals, pedestrians with faces and opinions, and the occasional cow.

**Play:** replace this line with your GitHub Pages link, for example `https://YOUR-USERNAME.github.io/namma-bengaluru-rush/`

Needs a desktop browser (Chrome, Edge or Firefox) with WebGL, a keyboard and a mouse. It is not designed for phones or tablets. If it runs slowly, open the pause screen (press Esc) and turn Shadows off.

## Your progress is saved

Cash, completed missions, achievements, photos and your last on-foot position are saved automatically in your own browser (localStorage). Nothing is sent to a server. Use **Continue** on the start screen to pick up where you left off, or **New game** to erase it. Clearing the site's browser data also clears the save.

## Controls

| Key | Action |
| --- | --- |
| W A S D | Walk or drive |
| Mouse | Look around (click the game once to capture the mouse) |
| Shift | Sprint |
| Space | Jump on foot, handbrake in a vehicle |
| E | Talk, get in or out of vehicles, pet a dog, ride the metro |
| H | Honk in a vehicle, say hello on foot |
| C | Raise the photo camera |
| M / J | Map / journal and achievements |
| 1 to 6 | Pick a dialogue choice |
| Arrow keys | Turn the camera if mouse capture is unavailable |

## Missions

Look for the gold light beams and the gold marker above people's heads.

1. **Auto Anna's Favour:** drive a passenger from Cunningham Road to Koramangala.
2. **Hot Dosa Delivery:** fetch a masala dosa from Vidyarthi Bhavan and get it to the stadium while it is hot.
3. **Gully Cricket:** score 18 runs in 6 balls. Swing when the marker reaches the green zone.
4. **Photo Walk:** photograph Vidhana Soudha, Bangalore Palace, Chinnaswamy Stadium and the Lalbagh Glass House.
5. **Snatch Back:** catch a thief and return the phone.
6. **Beat the Metro:** race the Purple Line express from Majestic to Indiranagar.
7. **Brewery Trail:** collect quiz sheets from two taprooms (Indiranagar and Koramangala) and host the pub quiz on Church Street. Non-alcoholic and designed so nobody drinks and drives.
8. **Flight to Catch:** take Rohan from Koramangala to Departures at the airport, then bring Meera home from Arrivals.

## How the map relates to real Bengaluru

The map is a stylised grid, not a street-accurate copy of Google Maps. Google Maps imagery cannot be reused in a game, so landmark positions are instead anchored to their real coordinates: one block is about 1.5 km and the centre of the map is MG Road near Church Street. That keeps the relative layout right: Majestic far to the west, Vidhana Soudha and Cubbon Park in the middle, Chinnaswamy Stadium and MG Road to the east of the park, Indiranagar further east, Bangalore Palace to the north, Lalbagh to the south-west, Basavanagudi further south-west, Koramangala to the south-east and the airport to the north-east.

Known simplifications:

- Street layouts inside each district are generated, not traced from real maps.
- The real Kempegowda International Airport is about 35 km north of the city centre (via Bellary Road and NH 44). It is pulled in to the north-east corner so you can drive there.
- In real life the Purple Line runs underground between Cubbon Park and the City Railway Station, including Majestic. In the game the viaduct is elevated end to end so the race is readable.
- Buildings, shops and pubs are generic. Pub names in the game are fictional.

If you want a street-accurate version later, export road data from OpenStreetMap (free to use with attribution under the ODbL) and replace the grid generator.

## Publish on GitHub Pages

1. Create a new **public** repository on GitHub, for example `namma-bengaluru-rush`.
2. Add `index.html` and `README.md`. In the web UI: **Add file > Upload files**, drag both in, then **Commit changes**.
3. Open **Settings > Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose branch `main` and folder `/ (root)`, then **Save**.
4. Wait a minute or two and refresh the Pages settings. The live link appears at the top.

The file must be named `index.html`. GitHub Pages is free for public repositories.

### Optional: bundle Three.js for offline resilience

The game loads Three.js r128 from cdnjs. To keep it working when that CDN is blocked, download `https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js`, save it as `three.min.js` next to `index.html`, and commit it. The page falls back to that local copy automatically.

## Credits

- 3D engine: [three.js](https://threejs.org) r128 (MIT licence), loaded from cdnjs.
- Fonts: Bungee, Rubik and Noto Sans Kannada from Google Fonts (SIL Open Font Licence).
- All models, faces, textures and sounds are generated in code. No external assets.
- Characters and businesses are fictional, except real landmarks and places used as setting.
