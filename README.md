
RGB to GREY to bin to tsp

#generate Daisey-grey.png
1. convert ./data/Daisey.png -colorspace gray ./data/Daisey-grey.png

# generate data/test-bin-local-delitate.png
2. binary_local_threshold.ipynb

# generate data/test.tsp
3. ./monchrom2cities-txt data/test-bin-local-delitate.png

#generate data/test_trip.csv
4 ./columbus data/test -global_search= 10 -local_search= 30 -temp= 15000 -decay= .9985 -maxiter= 16000 &

# Visualize data/test_trip.csv
5. Watch intermediate results: tsp_result_only.ipynb



Credits

https://github.com/SteveBronder/tsp_gpu
