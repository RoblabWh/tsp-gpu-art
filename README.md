
RGB to GREY to bin to tsp

1. convert .data/Daisey.png -colorspace gray data/Daisey-grey.png

2. binary_local_threshold.ipynb

3. ./monchrom2cities-txt data/test-bin-local-delitate.png

4 ./columbus data/test -global_search= 10 -local_search= 30 -temp= 15000 -decay= .9985 -maxiter= 16000 &

5. Watch intermediate results: tsp_result_only.ipynb



Credits

https://github.com/SteveBronder/tsp_gpu
