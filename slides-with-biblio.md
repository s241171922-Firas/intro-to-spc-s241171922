---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::
---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Math Scores
This histogram visualizes the distribution of 'Math' scores from the `bigclass` dataset.

- **X-axis**: Math Scores
- **Y-axis**: Frequency
- **Binwidth**: 50
:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_scores_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="100%"}
### Overall Conclusion on Machine Capabilities

Based on the Cpk analysis (with USL=105.0, LSL=95.0, Pressure=200, Temperature=338):

*   **Machine 1:** The process is **NOT capable** (Cpk = 1.185 < 1.33). While close to the acceptable limit, it doesn't meet the standard for capability, suggesting potential for improvement.
*   **Machine 2:** The process is **NOT capable** (Cpk = 0.272 < 1.33). This machine shows a significantly lower Cpk, indicating a process that is far from capable and requires substantial intervention.
*   **Machine 3:** The process is **NOT capable** (Cpk = 0.942 < 1.33). Similar to Machine 1, this process does not meet the capability standard and needs improvement efforts.

In summary, none of the machines are currently capable under the specified conditions. Further investigation into the causes of variation and mean shifts is necessary to improve process capability.

:::
::::

---
# Bibliography
<div id="refs"></div>
