# CITY TRACE: HEATLINE

A compact, browser-playable Three.js urban action prototype. The project is designed for touch-first play and includes a procedural Ahmedabad-inspired district, three drivable vehicle types, patrol/search/pursuit police states, mission progression, two ending choices, local saves, a minimap, and graphics profiles.

## Run locally

Requirements: Node.js 20+ and npm.

```bash
npm install
npm run dev
```

Open the Vite URL printed in the terminal. For a phone on the same Wi-Fi network, open the URL using the host computer's LAN IP and Vite's displayed port. Allow local network access if prompted. The development server must be reachable from the phone.

Build a production bundle:

```bash
npm run build
npm run preview
```

## Controls

- Mobile: left virtual stick moves on foot; drag the right side of the scene to rotate the camera. RUN and JUMP are contextual. ACT enters/exits a nearby vehicle or advances an interaction objective.
- Driving: use steering, GAS, BRAKE, and HB buttons. ACT exits the vehicle.
- Desktop fallback: WASD / arrow keys, Shift to sprint, Space to jump, E or F to interact, Escape to pause. Mouse drag on the right side rotates the camera.
- The campaign begins at the safehouse. Follow the objective card and cyan marker on the minimap.

## Included systems

- Five mission definitions with step triggers, rewards, evidence records, restart support, and two final choices.
- Versioned localStorage saves with basic validation and a fresh-save fallback.
- Procedural roads, buildings, market/police/garage/industrial/relay landmarks, road clutter, trees, and an overpass.
- Compact car, motorcycle, auto-rickshaw, and pooled ambient traffic.
- Police patrol, investigate, pursue, and search states; local line-of-sight checks; remembered last-seen position and repeated-route counters.
- On-foot collision, jump, sprint, driving acceleration/steering/braking, vehicle condition, speed display, minimap, health, cash, and heat display.
- LOW / MEDIUM / HIGH render profiles.

## Assets and licenses

No third-party art or audio files are bundled. Visible models are procedural Three.js geometry and materials. Three.js is distributed under the MIT License and is installed through npm. The simple engine tone is generated through Web Audio API. There are no essential remote asset URLs.

## Known limitations

This is a playable compact prototype, not a production-grade commercial game. Buildings and vehicles use procedural geometry rather than bespoke GLB models; traffic and pedestrian simulation are intentionally limited; pedestrian crowds, full dialogue trees, a real encrypted-evidence puzzle, deep upgrade shop UI, rain/wet-road rendering, first-person driving camera, and a professional soundscape are not implemented. Police and vehicle collision behavior is arcade-like. Route memory is stored and contributes to suspicion/search heuristics but is not a city-wide predictive simulation. LocalStorage saves are browser/device-local and are not cloud-synced. The requested 30 FPS target and long-session memory behavior have not been verified on physical mobile hardware.

## Verification

Run `npm test` for lightweight mission/save logic checks. Run `npm run build` to verify production bundling. Actual Android/iOS hardware profiling is still required before making performance claims.
