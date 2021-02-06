# Box Office Predictions (base on TMDB)

## Problem:

In this competition, you're presented with metadata on over 7,000 past films from The Movie Database to try and predict their overall worldwide box office revenue. Data points provided include cast, crew, plot keywords, budget, posters, release dates, languages, production companies, and countries. You can collect other publicly available data to use in your model predictions, but in the spirit of this competition, use only data that would have been available before a movie's release.

## Work process:

### Notebooks

1. data_analysis.ipynb
   
2. feature_engineering.ipynb

### Baseline
* drop:
```
belongs_to_collection
genres
homepage
imdb_id
original_title
overview
poster_path
production_companies
production_countries
spoken_languages
status
tagline
title
Keywords
cast
crew
```

* parse ```release_date``` for a month, day and year


### Sketch ideas

#### log transform

* ```revenue```

* ```budget```
  
* ```popularity```

#### outliers handling

* ```runtime```

* ```revenue```

* ```budget```
  
* ```popularity```

#### scaling

* ```budget```

* ```revenue```

#### one-hot encoding

* ```genres```

* ```spoken_languages```

* ```production_companies```

* ```belongs_to_collection```

* ```production_countries```

* ```Keywords```

* ```cast``` (actor name)

* ```crew``` (department + name)

#### group_by statistics

* ```cast``` (actor name)

* ```genres```

* ```crew``` (department + name)

* ```spoken_languages```

* ```production_companies```

* ```belongs_to_collection```

* ```production_countries```

* ```Keywords```

#### NLP (vectorize the most popular words)

* ```tagline```

* ```title```

* ```overview```

#### Other

* is not null ```homepage```

* parse ```homepage``` for domain, https...

### Feed

1. (2.972, 83%) baseline
2. (2.329, 58%) log transformed revenue
3. (2.329, 58%) log transformed budget, popularity
4. (2.325, 58%) clear outliers for popularity