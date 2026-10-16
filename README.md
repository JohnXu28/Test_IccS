# Test_IccS — IccS_Test (scanner engine) black-box test data

Golden raw-compare suite for `apps/IccS_Test` (ConverSion_Test, 8-bit path):

- `rainbow.icc` — input scanner profile
- `In.tif`     — 8-bit input image
- `In16.tif`   — 16-bit input image (used by ConverSion_File)
- `Target1/2/3.tif` — golden raw buffers for the three pipelines
  (sRGB_KodakPhoto / sRGB_KodakMix / sRGB_KodakText)

Run (from this directory, CWD matters):

```
IccS_Test.exe rainbow.icc In.tif out.tif
```

`ConverSion_Test` compares its converted buffers against `Target1/2/3.tif`
in memory (PASS = bit-identical); `ConverSion_File` writes `In*Out*.tif`
outputs here — those are generated and ignored by git.
