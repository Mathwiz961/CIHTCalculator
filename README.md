# ERAU Confidence Interval & Hypothesis Test Calculator

A single-file, ERAU-branded HTML web application that computes:

- **Confidence Intervals (CI)**
- **Hypothesis Tests (HT)**

Designed for:

- GitHub Pages deployment  
- Canvas LMS embedding (iframe)  
- Introductory and intermediate statistics courses  

---

## Features

### Modes

- **Confidence Interval**
- **Hypothesis Test**
  - Two-sided (≠)
  - Left-tailed (<)
  - Right-tailed (>)

---

## Statistical Procedures Included

### Means

#### One Mean (μ)

- σ known → **z distribution**
- σ unknown → **t distribution**
  - Degrees of freedom: `df = n − 1`

#### Two Means (μ₁ − μ₂), Independent Samples

- σ’s known → **z distribution**
- σ’s unknown → **Welch’s t distribution**
  - Unequal variances
  - Welch–Satterthwaite approximation for degrees of freedom

#### Matched Pairs (μd)

- t distribution on differences
- `df = n − 1`

---

### Proportions

#### One Proportion (p)

- z distribution (normal approximation)

#### Two Proportions (p₁ − p₂)

- z distribution  
- Hypothesis tests use **pooled p̂**  
- Confidence intervals use **unpooled standard error**

---

## Output Includes

Each calculation reports:

- Distribution used (z or t)
- Degrees of freedom (when applicable)
- Standard Error (SE)
- SE formula used
- Critical value(s)
- Test statistic (z or t)
- p-value
- Confidence interval endpoints (CI mode)
- Decision (Reject H₀ / Fail to reject H₀) for hypothesis tests

---

## Project Structure
/ (repository root)

├── index.html

└── README.md

- All UI and statistical logic are contained in `index.html`.
- No external libraries.
- No build steps.
- No dependencies.

---

## Run Locally

1. Download or clone the repository.
2. Open `index.html` in any modern web browser.

---

## Deploy on GitHub Pages

1. Push `index.html` to the repository root.
2. Navigate to:

   **Settings → Pages**

3. Under **Build and Deployment**:
   - Source: **Deploy from a branch**
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`

4. Save.

Your application will be available at: https://<your-username>.github.io/<repo-name>/


---

## Embed in Canvas (iframe)

After deploying to GitHub Pages, embed using:

```html
<iframe
  src="https://<your-username>.github.io/<repo-name>/"
  width="100%"
  height="900"
  style="border:0;"
  loading="lazy"
  allowfullscreen>
</iframe>
```
## Important

Do NOT use a raw GitHub URL such as:

github.com/.../blob/...

Canvas will block that URL.

Always use your GitHub Pages URL.

---

## Mathematical Implementation Notes

Normal CDF and inverse normal computed via numerical approximation (Acklam method).
- Student’s t CDF computed using the incomplete beta function.
- Inverse t computed using numerical root-finding.
- Two-mean unknown σ defaults to Welch’s t.
- Two-proportion hypothesis tests use pooled p̂ for SE₀.

---

## Academic Disclaimer

**This tool assumes standard statistical conditions:**

- Independent observations

- Approximate normality or CLT conditions for mean procedures

- Adequate success/failure counts for proportion procedures

- Users should verify assumptions before interpreting results.

---

## License
**MIT License**

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
