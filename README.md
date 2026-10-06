# Smart Classroom Lab

An interactive companion to Topic 1: The IoT Ecosystem. All readings, timing values and outcomes are illustrative simulations.

## Explore

- **Classroom:** inspect devices, change occupancy and temperature, toggle a lamp, and play a sensing-to-action story.
- **Network:** follow device messages and return commands, disconnect the internet, buffer readings and reconnect.
- **Data processing:** validate an impossible reading, sort by timestamp and aggregate a batch.
- **Edge & cloud:** compare a local stop command with a cloud response under different network conditions.
- **Five V’s:** experiment with accumulated volume, different data forms, arrival speed, placement bias and decisions that use data.
- **Check yourself:** eight questions with feedback and a score.

Use the top navigation to switch experiments. “Pause motion” pauses animation and simulated clocks. Reduced-motion preferences start the site paused. Settings and scores stay only in memory and reset when the page reloads.

## Run locally

Open `index.html` directly in a modern browser. No build, install, API key or backend is required. Alternatively, from this folder run:

```sh
python3 -m http.server 4173
```

Then visit `http://localhost:4173`.

## Publish on GitHub Pages

1. Create a GitHub repository and upload the contents of this folder at its root. Keep `assets/` alongside `index.html`, `styles.css` and `app.js`.
2. In repository **Settings → Pages**, select **Deploy from a branch**.
3. Choose the **main** branch and **/(root)**, then save.
4. Open the URL provided by GitHub after deployment completes.

The included `.nojekyll` disables Jekyll processing. All links use relative paths, so the site works under a repository URL such as `https://username.github.io/iot-classroom-lab/`.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Files

- `index.html`: page structure, classroom hotspots and network diagram.
- `styles.css`: responsive styling and animations.
- `app.js`: classroom rules, experiments, simulation clock and quiz.
- `assets/classroom.png`: original AI-generated classroom illustration.
- `assets/favicon.svg`: site icon.
- `TEACHING-GUIDE.md`: slide mapping, suggested demonstrations and assumptions.

## Scope and assumptions

No real devices are connected. No camera or microphone is accessed. No student data is collected by the application, and there are no external runtime dependencies. GitHub Pages itself may log visitor information under GitHub’s hosting policies.

The network is illustrative. Real gateway protocol support depends on hardware. Some Wi-Fi devices connect through routers directly. The smart plug’s sensing features are an example, not a claim about all products. Timing and cooling hours are teaching assumptions, not engineering specifications or energy measurements.

The classroom illustration was generated specifically for this site. The lesson structure is based on the supplied Topic 1 IoT Ecosystem teaching deck. The original PowerPoint is not included.

## Guided learning

The site now opens in guided mode. Each lesson presents one short instruction, an action button, and a result. The next step unlocks after that action. Previous steps can be revisited. Use **Explore freely** to reveal the full controls and longer explanations, then return to the guided lesson when ready.

The classroom adds entering students, a rising thermometer and animated cooling airflow. The network follows one message at a time. Data processing animates validation, record reordering and a summary. The five V’s progress through one concept at a time.

`scaffold.js` supplies the guided sequence and focused animations alongside the underlying experiments in `app.js`.
