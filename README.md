# Vision Cognition Lab

An interactive web app with four short experiments that show how vision connects to attention,
perception, memory, and decision-making. It runs in the browser with no installation.

**Live demo:** _add your GitHub Pages link here after publishing_

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

## Publish it (so a professor can click and try it)
1. Create a GitHub repository and upload these files.
2. Go to Settings > Pages, choose the `main` branch and the root folder, and save.
3. Paste the resulting link in this README and in your email.

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
- Fit a drift-diffusion model to the dot task data (for example with PyDDM).
- Add a saliency-model comparison for attention.

## References
- Posner, M. I. (1980). Orienting of attention. *Quarterly Journal of Experimental Psychology, 32*(1), 3-25.
- Luck, S. J., & Vogel, E. K. (1997). The capacity of visual working memory for features and conjunctions. *Nature, 390*, 279-281.
- Cowan, N. (2001). The magical number 4 in short-term memory. *Behavioral and Brain Sciences, 24*(1), 87-114.
- Ratcliff, R., & McKoon, G. (2008). The diffusion decision model. *Neural Computation, 20*(4), 873-922.
