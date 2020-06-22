
RGB to GREY to bin to tsp

# convert ./data/Daisey.png -colorspace gray ./data/Daisey-grey.png
generate Daisey-grey.png

#binary_local_threshold.ipynb
generate data/test-bin-local-delitate.png

# ./monchrom2cities-txt data/test-bin-local-delitate.png
generate data/test.tsp

# ./columbus data/test -global_search= 10 -local_search= 30 -temp= 15000 -decay= .9985 -maxiter= 16000 &
generate data/test_trip.csv

# Watch intermediate results: tsp_result_only.ipynb
Visualize data/test_trip.csv



Credits

https://github.com/SteveBronder/tsp_gpu
