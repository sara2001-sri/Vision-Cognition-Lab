# Vision Cognition Lab

An interactive web app with four short experiments that show how vision connects to attention,
perception, memory, and decision-making. It runs in the browser with no installation.



## Tasks and the science behind them

| Theme | Task | Measure | Classic finding |
|---|---|---|---|
| Attention | Spatial cueing (Posner) | Validity effect (RT invalid minus valid) | Cued locations are processed faster (Posner, 1980) |
| Perception | Müller-Lyer illusion, method of adjustment | Illusion size in px | Context changes perceived length |
| Memory | Change detection | Capacity K = N x (hit rate - false-alarm rate) | Capacity of about 3 to 4 items (Luck & Vogel, 1997; Cowan, 2001) |
| Decision-making | Dot comparison + confidence | Accuracy, RT, confidence by difficulty | Weaker evidence gives slower, less accurate, less confident choices (drift-diffusion models) |

## Run it
Open `index.html` in Chrome, Edge, or Firefox. Do the four tasks (about 12 minutes), then open **Results**.
Use **Download data (CSV)** to save the data.



## Data format
`module, trial, condition, level, response, correct, rt_ms, value`
- posner: condition = cue validity, level = target side
- muller: condition = fin type, level = standard length (200 px), value = adjusted length
- vwm: condition = change/same, level = set size
- dots: condition = dot difference, level = side with more dots, value = confidence (1 to 3)

## Limitations
- Stimuli are in pixels, not degrees of visual angle, and screen size and viewing distance are not controlled.
- Browser timing has roughly 10 to 20 ms of noise.
- Trial counts are small, so single-person results are noisy. Pool data from several people for stronger conclusions.

## Ideas for extension
- Add a webcam or eye-tracker gaze measure to the cueing task.
- Fit a drift-diffusion model to the dot task data .
- Add a saliency-model comparison for attention.

