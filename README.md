# solar-flow-heatmap

The heat-map payload for the Solar Flow app, served at
**https://solarflow.brilliantworker.com/heatmap.json**.

To publish, replace `heatmap.json` on `main` and push. The server checks this repo every minute. If the new
file is valid JSON and no larger than 64 KB, it goes live; otherwise the previous file stays up. No build
step, and nothing else in this repo is served.

- `date` is the **solar date** the payload applies to, at the Keeper's location. A future date is rejected
  by the app.
- The contract (schema v1) is owned by the Heat-map Author and defined in the Solar Flow project.
