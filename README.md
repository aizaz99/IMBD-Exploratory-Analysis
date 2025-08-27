** TMDB Movie Analytics with Pandas**

Analyze the TMDB 5000 Movies + Credits datasets using pandas to answer business and creative questions like: which genres are most profitable, which directors score the highest ratings, who dominates blockbuster casts, and how film metrics evolve by decade.

Overview

What you’ll see in the notebook

Merge tmdb_5000_movies.csv and tmdb_5000_credits.csv on movie ID

Parse JSON-like columns (genres, keywords, cast, crew, companies)

Engineer features:

profit = revenue - budget

director from crew

top_cast (top 3 billed)

release_year and decade

Answer key questions with groupby and Counter

Visualize results with matplotlib

Print a KPI summary table

Datasets

/kaggle/input/movietitledataset/tmdb_5000_movies.csv

/kaggle/input/moviedataset/tmdb_5000_credits.csv

Key columns used:

Movies: id, title, budget, revenue, vote_average, genres, keywords, production_companies, release_date

Credits: movie_id, cast, crew

Note: JSON fields arrive as strings. The notebook converts them to Python objects before analysis.

Questions this project answers

Average Profit by Genre
Which genres earn the most profit on average?

Top Directors by Rating
Which directors have the highest average vote_average with at least 3 films?

Star Power
Who are the most frequent top-billed actors overall, and in the top 10% revenue “blockbusters”?

Trends by Time
How do average budget, revenue, and rating move across decades?

Budget vs Revenue
What is the correlation between budget and revenue?

Tech stack

Python 3.x

pandas

matplotlib

Jupyter Notebook

Built-ins: ast, collections.Counter




Parse JSON and feature engineering

Convert genres, keywords, production_companies, cast, crew

Extract director, top_cast, companies

Build profit, release_year, decade

Analysis

Average profit by genre (explode and groupby)

Director ratings table (min 3 films)

Actor frequency overall and in blockbusters (top 10% revenue)

Decade trends for budget, revenue, rating

Budget vs revenue correlation

Visuals

Bar: Top 10 genres by average profit

Scatter: Budget vs revenue

Line: Average rating by decade

Bar: Top 15 blockbuster actors

KPIs

Compact table with headline metrics

Example highlights from my run

Your numbers may vary, but here’s the kind of output to expect:

Genres leading by average profit included Animation, Adventure, and Fantasy.

Top directors by average rating (min 3 films) included Hayao Miyazaki, Sergio Leone, Christopher Nolan, Quentin Tarantino, Pete Docter.

Frequent top-billed actors overall included Robert De Niro, Samuel L. Jackson, Bruce Willis, Matt Damon.

Frequent top-billed actors in blockbusters included Tom Cruise, Will Smith, Tom Hanks, Johnny Depp, Ian McKellen.

Budget and revenue showed a positive correlation.

Interpreting results

Use average profit for a quick profitability view, but consider medians to reduce outlier effects.

For directors, apply a minimum film count to avoid single-movie spikes.

Actor counts are based on top 3 billed. Adjust if you want deeper casts.

Some early decades may have sparse data. Treat decade trends with care.

Extend this project

Add median and IQR to reduce outliers.

Normalize revenue to inflation-adjusted dollars.

Build a simple profit classifier using scikit-learn.

Add country or language breakdowns.

Create a dashboard in Streamlit or Power BI.

Acknowledgments

TMDB 5000 Movies and Credits datasets

Matplotlib and pandas communities
