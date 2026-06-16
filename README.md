## Zomato Bangalore Restaurant Analysis

Bangalore has over 50,000 restaurants listed on Zomato — and buried inside that data 
are some genuinely surprising patterns. This project digs into what actually makes a 
restaurant successful in Bangalore: is it the location? The cuisine? The price? Whether 
you can book a table in advance?

I explored all of that using Python, and this is what I found.

---

## What I was trying to answer

I started with 5 business questions that I'd actually want answered if I were opening 
a restaurant in Bangalore (or just trying to pick a good one for dinner):

1. **Which areas have the most restaurants — and do those areas actually have better food?**
2. **Does spending more money mean better ratings?**
3. **Which cuisines are most popular, and which ones are actually rated highest?**
4. **Does offering online ordering or table booking make a difference to ratings?**
5. **Which restaurant formats (casual dining, quick bites, cafes etc.) perform best?**

---

## What I found

**Location matters, but not how you'd expect.**
BTM Layout has the highest number of restaurants in the city (~3,500+), but it ranks 
near the bottom for average ratings. Koramangala 5th Block has far fewer restaurants 
but consistently tops the ratings chart. Being in a premium locality matters more than 
being in the busiest one.

**Price is a weak quality signal.**
There's only a 0.38 correlation between cost and rating. A ₹300 restaurant can easily 
outrate a ₹1,500 one. Expensive doesn't mean good — it just means expensive.

**The most popular cuisines aren't the best-rated ones.**
North Indian cuisine dominates the city (~21,000 restaurants) but sits near the bottom 
on average ratings. Continental and Italian — far less common — consistently top the 
ratings chart. High volume appears to dilute quality.

**Table booking is the strongest quality signal we found.**
Restaurants that accept table bookings average a 4.14 rating vs 3.62 for those that 
don't — a gap of 0.52 points. It's a proxy for experience-driven, sit-down restaurants 
that tend to take quality seriously. Online ordering, by contrast, barely moves the 
needle (0.07 correlation with rating).

**Quick Bites dominate in count, but Casual Dining + Bar leads in quality.**
With ~19,000 outlets, Quick Bites is the most common format — but it ranks 9th out of 
10 on average ratings. Casual Dining with a Bar tops the ratings at 4.08, followed by 
Dessert Parlors and Cafes.

---

## Tools used

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **Dataset** — [Zomato Bangalore Restaurants](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants) (~51,000 restaurants)
- **Environment** — Jupyter Notebook

---

## Project structure

zomato-bangalore-eda/

│

├── zomato_eda.ipynb        # Main analysis notebook

└── zomato_cleaned.ipynb    # Cleaned dataset (output of cleaning pipeline)

---

## How to run this

1. Clone the repo
2. Install dependencies: `pip install pandas numpy matplotlib seaborn kagglehub`
3. Open `zomato_eda.ipynb` in Jupyter and run all cells top to bottom

The notebook downloads the raw dataset automatically via `kagglehub` — no manual 
downloading needed.

---

