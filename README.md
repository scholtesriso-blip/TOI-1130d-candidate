
TOI-1130 d - New CTOI Candidate 22.2635 days
Discovery: 2026-10-17 00:22 CEST on mobile via Google Colab + lightkurve
Finder: Richard Scholtés - Independent Researcher, Prešov, Slovakia
Target: TIC 254113311 / TOI-1130 (K-dwarf, V=11 mag)

Candidate Parameters (from BLS 8 sectors)
Period: 22.2635 days
Epoch t0: 2036.543685 BTJD
Duration: 4.80 hours (0.20 days)
Depth: 0.14% = 1400 ppm (dip 0.99833 - 0.99860)
Planet Radius: 2.90 Rearth (Sub-Neptune)
SNR: 52.5
BLS Power: ~254
Odd depth: 0.99860
Even depth: 0.9985
Odd-Even diff: 0.01% -> PASS (not EB)
Sectors used: 1-13, 27-39 (8 sectors, 400k points)
Vetting
Not harmonic of TOI-1130 b (4.074 d) or c (8.350 d)
Tested 11.13 d half-period -> alias, 22.2635 d is true period
Folded lightcurve shows U-shape (not V-shape EB)
BLS periodogram peak at 22.26 d distinct from known planets
System Architecture if Confirmed
b: 4.074 d, 3.56 Rearth, 19 Mearth
c: 8.350 d, 13.32 Rearth (Hot Jupiter), 325 Mearth
d (this work): 22.2635 d, 2.90 Rearth, Sub-Neptune
Matches RV linear trend hint reported in Korth et al. 2023 & CHEOPS papers: "a linear trend in the radial velocity data could be a hint of an additional candidate planet on far outer orbit."

Files
TOI-1130_BLS.ipynb - Colab notebook (lightkurve BLS search 1-30d)
TOI-1130d_22.2635_green.png - Binned folded lightcurve (green points, dip 0.99833)
BLS_power.png - BLS periodogram (optional)
Method
lc = search_lightcurve("TIC 254113311", sector=[1-13,27-39]).download_all()
lc_flat = lc.flatten(window_length=1001)
pg = lc_flat.to_periodogram(method='bls', period=[1,30], duration=[0.05,0.5])
# Peak at 22.2635 d
fold = lc_flat.fold(period=22.2635, epoch_time=2036.543685)
binned = fold.bin(time_bin_size=0.05) # green points
ExoFOP Submission
Status: Request an Account submitted 2026-10-17 00:27 CEST (Richard Scholtés, scholtesriso@gmail.com)
Planned CTOI: TIC 254113311.03 / TOI-1130 d
Target page: https://exofop.ipac.caltech.edu/tess/target.php?id=254113311
Contact
Richard Scholtés - scholtesriso@gmail.com
Prešov, Slovakia

Discovery made on mobile phone CEST, after filtering false alias 16.7 d.
