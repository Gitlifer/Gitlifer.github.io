# `html-midi-player` website

FYP Demo Page

---
Evaluation metrics:

| Model             | Pitch Range | N-Pitches Used | Polyphony | Scale Consistency | Pitch Entropy | Empty Beat Rate | Groove Consistency |
|-------------------|-------------|----------------|-----------|-------------------|---------------|-----------------|--------------------|
| CP-LSTM           | 60.98       | 40.380         | 4.901     | 0.958             | 4.447         | 0.091           | 0.993              |
| CP-linear (baseline) | 48.50    | 31.980         | 3.292     | 0.967             | 4.210         | 0.030           | 0.995              |
| CP-Comp           | 64.08       | 42.060         | **5.125**     | 0.966         | 4.382         | 0.045           | 0.994              |
| CP-XL             | **64.62**  | **44.36**      | 5.112     | **0.977**        | **4.548**      | **0.021**       | 0.992              |

### Pitch-Related Metrics
- **Pitch Range**: The range of pitches.
- **N-Pitches Used**: The number of unique pitches used.
- **Polyphony**: The average number of pitches being played concurrently.
- **Scale Consistency**: The largest pitch-in-scale rate over all major and minor scales. The pitch-in-scale rate is defined as the ratio of the number of notes in a certain scale to the total number of notes.
- **Pitch Entropy**: The entropy of the normalized note pitch histogram.

### Rhythm-Related Metrics
- **Empty Beat Rate**: The ratio of the number of empty beats (where no note is played) to the total number of beats.
- **Groove Consistency**: The mean Hamming distance of the neighboring measures.

---
Compound Word (CP)
Token types including:
- 3 note-related types: {duration}, {pitch}, {velocity}
- 3 metric-related types {tempo}, {position/bar}, {chord}
- {EOS}

---

Original source code is from https://cifkao.github.io/html-midi-player/. It is given here as an example of including `html-midi-player` in a website built using tools like the [Parcel](https://parceljs.org/) bundler and the [Jekyll](https://jekyllrb.com/) static site generator.

To use it, install all the dependencies:
- `bundle install` for the Ruby dependencies (you may need to install Bundler 2.3.12 first)
- `yarn install` for the Node.js dependencies (you may need to install Yarn first)

Then run `yarn dev` for live development or `yarn build` to build the website ready for deployment.
