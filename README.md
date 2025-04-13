## To run the inference process with 2 threads

```bash
pycbc_inference --verbose --config-files model.ini data.ini prior.ini sampler.ini --output-file inference-masses.hdf --seed 3214897 --nprocesses 2 --force
```

## To plot the posterior of the inferred parameters (eg. eta, mchirp)

### Corner Scatter plot
```bash
pycbc_inference_plot_posterior --verbose --input-file inference-masses.hdf --output-file posterior.png --plot-scatter --plot-marginal --z-arg snr --parameters mchirp eta
```
### 2D density plot
```bash
pycbc_inference_plot_posterior --verbose --input-file inference-masses.hdf --output-file posterior.png --plot-density --plot-contours --plot-marginal --parameters mchirp eta
```

## To run the autocorrelation function of each parameter chain

```bash
pycbc_inference_plot_acf --input-file inference-masses.hdf --output-file plotacf.png --parameters mchirp eta --verbose
```