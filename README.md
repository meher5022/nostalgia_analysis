
[README.md](https://github.com/user-attachments/files/27767517/README.md)

# 🎥🎞️ Nostalgic Aesthetics as Responses to Modern Online Life
### An Exploratory Data Analysis Project

---

## The Hypothesis

> **As modern digital environments become more algorithmic, fast-paced, and overstimulating, users increasingly seek nostalgic and analog experiences that feel more authentic, emotionally comforting, and human.**

We are living through a paradox. The more seamlessly the internet integrates into daily life, the more people appear to be turning *away* from it.
Instant photography. Film cameras. Vintage clothing. Y2K. 2000s nostalgia. These aren't random revivals. This project asks: **what if they are symptoms?**

---

##  Project Structure

```
 project/
│
├── sales_analysis.py          # Instax / analog camera sales trends
├── insta_analysis.py          # Instagram sentiment & digital fatigue NLP
├── google_trends_analysis.py  # Google Trends: nostalgia vs. digital fatigue
│
├──  visuals /
│   ├── monthly_quantity_sold.png
│   ├── monthly_revenue_trend.png
│   ├── yearly_quantity_sold.png
│   ├── camera_vs_film_trend.png
│   ├── top_selling_products.png
│   ├── revenue_by_sales_channel.png
│   ├── film_vs_camera_share.png
│   ├── sentiment_distribution.png
│   ├── theme_distribution.png
│   ├── wordcloud_discussions.png
│   ├── google_trends_over_time.png
│   ├── fatigue_vs_nostalgia.png
│   ├── lag_correlation.png
│   ├── correlation_heatmap.png
│   ├── doomscrolling_vs_vintage.png
│   └── yearly_cultural_trend_change.png
```

---

## The Story in Three Acts

### Act I — The Market Speaks: Instax Sales Analysis

*In a world of infinite digital photos, why are people returning to physical photography?*

The first dataset examines **Fujifilm Instax sales transactions** — a product line built entirely on the charm of imperfection: overexposed edges, slightly washed-out colours If the nostalgia trend were purely aesthetic — a filter on Instagram, a mood board on Pinterest — you wouldn't expect it to move physical units. But the traces of this shift appear in purchasing patterns .

**What the data reveals:**

- **Monthly & Yearly Quantity Trends** examine whether Instax demand is increasing steadily, stabilizing, or responding to broader cultural shifts. Growth in these trends reflects more than consumer spending, it indicates a growing preference for tangible experiences. 

![monthly quantity sold](visuals/monthly_quantity_sold.png)

- **Camera vs. Film Sales Ratio** is the most telling KPI of all. A high film-to-camera ratio means people who already *own* the camera keep *using* it. They aren't just buying a novelty object and letting it collect dust — they're committing to analog photography.

![Camera vs Film](visuals/film_vs_camera_share.png)

A high film-to-camera ratio means people who already own the camera keep using it.

> **Hypothesis Link:** Rising Instax sales, especially repeat film purchases, suggest consumers are actively investing in analog experiences — not just fantasising about them.

---

### Act II — The Algorithm Knows You're Tired: Instagram Sentiment Analysis

*"The place where people go to escape boredom has itself become a source of exhaustion."*

The second dataset turns inward — to the words people use on Reddit when they talk about Instagram. Using **NLP, TF-IDF analysis, and theme-based classification**, this analysis maps the emotional texture of online discourse around social media addiction and digital fatigue.

**What the data reveals:**

- **Sentiment Distribution** answers a blunt question: when people talk about Instagram and addiction in the same breath, are they mostly positive, negative, or neutral? A skew toward negativity here anchors the emotional backdrop against which nostalgia must be understood.

- **Theme Frequency Analysis** tracks five core themes across posts:
  - `Addiction` — dopamine, compulsive behaviour, inability to stop
  - `Overstimulation` — burnout, anxiety, overwhelm
  - `Attention Problems` — shortened focus, inability to concentrate
  - `Short-Form Content` — reels, scrolling, algorithmic feeds
  - `Digital Detox` — the desire to quit, delete, go offline

- **Top Words by Sentiment** and the **Word Cloud** strip away structure and let the raw vocabulary speak. When "dopamine," "algorithm," "anxiety," and "attention" dominate the language of negative posts, the picture becomes clear: people aren't just bored. They feel *manipulated*.

> **Hypothesis Link:** The emotional exhaustion surfacing in online discourse creates the psychological conditions for nostalgia — a retreat toward simpler, slower, more controllable experiences.

---

### Act III — The Search Bar Reveals : Google Trends Analysis

*Purchases can be influenced. Search behavior is often instinctive.*

The third and most macro-level dataset uses **Google Trends data** to plot search interest over time across two competing cultural forces: **Digital Fatigue** (Brain Rot, AI Slop, Doomscrolling) and **Nostalgia** (Film Camera, Vintage, Retro Style, Y2K Aesthetic, 2000s).

This is where the hypothesis becomes testable at scale.

**What the data reveals:**

- **Google Trends Over Time** plots all search terms against three cultural fault lines:
  - **March 2020** — Pandemic lockdowns. The world went online, all at once.
  - **January 2021** — The TikTok Boom. Short-form video rewired attention spans globally.
  - **January 2023** — The AI Boom. Suddenly, even *content creation* felt automated.

  Each of these events represents an escalation in digital saturation. Watch what the nostalgia lines do in response.

- **Digital Fatigue vs. Nostalgia Composite Scores** condense the complexity into two clean trend lines. The key question: do they move *together*? Does one *lead* the other?

- **Correlation Heatmap** reveals the full relationship matrix between all tracked terms. Does "Brain Rot" correlate with "Film Camera"? Does "Doomscrolling" move with "Vintage"?

- **Doomscrolling vs. Vintage Regression** isolates this specific relationship — two terms that could not sound more different, plotted against each other to see if they share a hidden rhythm.

- **Yearly Cultural Trend Change** shows the *acceleration* of each category, not just their levels — identifying which force is growing fastest and whether the gap between fatigue and nostalgia is narrowing or widening.

> **Hypothesis Link:** If nostalgia search interest demonstrably rises in the months following spikes in digital fatigue, the hypothesis moves from compelling to evidenced.

---

##  Key KPIs at a Glance

| KPI | Source | What It Tests |
|-----|--------|---------------|
| Film-to-Camera Sales Ratio | `sales_analysis.py` | Depth of analog commitment, not just novelty |
| Yearly Instax Sales Growth | `sales_analysis.py` | Whether analog interest is sustained over time |
| Sentiment Score Distribution | `insta_analysis.py` | Emotional tone of digital fatigue discourse |
| Digital Detox Theme Frequency | `insta_analysis.py` | Scale of desire to disconnect |
| Lag Correlation (Fatigue → Nostalgia) | `google_trends_analysis.py` | Causal direction of the fatigue-nostalgia link |
| Fastest Growing Search Term | `google_trends_analysis.py` | Which side of the tension is accelerating |
| Doomscrolling ↔ Vintage Correlation | `google_trends_analysis.py` | Direct link between fatigue behaviour and retro search |

---

##  Tech Stack

```python
pandas          # Data manipulation & time-series analysis
matplotlib      # Trend visualisation & chart generation
seaborn         # Correlation heatmaps & regression plots
scikit-learn    # TF-IDF vectorisation for NLP
wordcloud       # Visual keyword analysis
collections     # Keyword frequency counting
numpy           # Composite score calculation
re              # Text cleaning & tokenisation
```

---

##  Datasets Used

| Dataset | Description |
|---------|-------------|
| `instax_sales_transaction_data.csv` | Fujifilm Instax product sales records with date, product, category, channel, quantity, and revenue |
| `insta_sentiment_data.csv` | Reddit posts discussing Instagram addiction, labelled with sentiment scores |
| `nostalgia.csv` | Google Trends export tracking search interest in nostalgia and digital fatigue terms over time |

---

##  Conclusions & Interpretation

This project does not claim that everyone buying a disposable camera is having an existential crisis about TikTok. But the convergence of three independent datasets — consumer spending, online emotional discourse, and mass search behaviour — points toward something more than coincidence.

**The pattern that emerges:**

1. Digital fatigue is real, measurable, and growing — visible in both the language people use online and the search terms they reach for when overwhelmed.
2. Analog and retro consumption is rising — not as a passing aesthetic phase, but as a sustained purchasing and searching behaviour.
3. The timing is suggestive — cultural accelerators like the pandemic, the TikTok boom, and the AI wave each appear to precede upticks in nostalgia-oriented searches and purchases.

---

##  How to Run

```bash
# Clone the repository
git clone https://github.com/yourusername/digital-nostalgia-eda.git
cd digital-nostalgia-eda

# Install dependencies
pip install pandas matplotlib seaborn scikit-learn wordcloud numpy

# Place datasets in the project root, then run each script
python sales_analysis.py
python insta_analysis.py
python google_trends_analysis.py
```

Charts will be saved as `.png` files in the project root.

---

## Author

**Meher Vaswani**
Data & Research | Exploring the cultural intersections of technology, emotion, and consumer behaviour.

---

