# Histogram-Equalization
Step‑by‑step manual grayscale histogram equalization in Python with full statistical analysis.

## Histogram-Equalization
This repository demonstrates a **manual grayscale image histogram equalisation** process using Python.  
All operations — from histogram calculation and normalisation to cumulative distribution computation and equalised mapping — are performed step‑by‑step without using OpenCV’s built‑in `equalizeHist()` function.

---

##  Original Image
<img width="404" height="427" alt="download" src="https://github.com/user-attachments/assets/e0e5d54a-1937-4c90-87bd-72ea296f7aa7" />


---

##  Histogram & CDF

Below are the manually computed **normalised histogram** and its **Cumulative Distribution Function (CDF)** for the input image.
<img width="1188" height="490" alt="download (1)" src="https://github.com/user-attachments/assets/6fa96dce-0ee2-4219-ab5b-ecd5b3ce9928" />


---

##  Equalisation Result

After performing manual mapping \( s_k = (L - 1) \times T(r_k) \):

<img width="953" height="451" alt="download (2)" src="https://github.com/user-attachments/assets/3d242080-5d07-4cac-a078-d4565d98521c" />


Histogram equalisation enhances global contrast and redistributes pixel intensities across the available range.

---

##  Histogram Comparison

To verify the equalisation effect, both **original** and **equalised histograms** are compared below:

<img width="1189" height="490" alt="download (3)" src="https://github.com/user-attachments/assets/ee1fc82c-d3ce-42bb-8e3c-67ab17369310" />


---

##  Quantitative Metrics

| Metric        | Original     | Equalized    |
|---------------|--------------|--------------|
| Mean          | 83.284042    | 129.744308   |
| Variance      | 4577.720330  | 5064.168432  |
| Entropy       | 7.308640     | 7.134227     |
| MSE           | -            | 2251.839020  |
| PSNR (dB)     | -            | 14.605430    |

---

##  How to Run
```bash
git clone https://github.com/mahditaghsimi/Histogram-Equalization.git
cd Histogram-Equalization/scr
pip install -r ../requirements.txt
jupyter notebook histogram_equalization_manual.ipynb
