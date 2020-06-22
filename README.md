# Making tsp art

Convert an image to monocrom (binary) image and use all black points (=0) as cities which has to be connected. The result is an image of one line with an equal start and end point. To solve the TSP problem a cuda implementation of a simulated annealing algorithm e.g. from SteveBronder can be used (see credits).

### RGB to GREY to bin to tsp

generate Daisey-grey.png
```
convert ./data/Daisey.png -colorspace gray ./data/Daisey-grey.png
```

generate ./data/test-bin-local-delitate.png
```
binary_local_threshold.ipynb
```

generate ./data/test.tsp
```
./monchrom2cities-txt data/test-bin-local-delitate.png
```

generate data/test_trip.csv (intermediate result /tmp/test_trip.csv)
```
./columbus data/test -global_search= 10 -local_search= 30 -temp= 15000 -decay= .9985 -maxiter= 16000 &
```

Visualize (intermediate) results of ./data/test_trip.csv (or /tmp/test_trip.csv)
```
tsp_result_only.ipynb
```



Credits

https://github.com/SteveBronder/tsp_gpu
