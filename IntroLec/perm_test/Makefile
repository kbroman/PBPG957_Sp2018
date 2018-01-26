all: lod_random.js data_random.json

data_random.json: grab_data_random.R
	R CMD BATCH grab_data_random.R

lod_random.js: lod_random.coffee
	coffee -bc lod_random.coffee
