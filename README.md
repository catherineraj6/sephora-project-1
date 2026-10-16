# Beauty at Every Price
### An Analysis of Sephora’s Product Listings

Exploring price differences across beauty categories and brands with Python.

## Project Overview

This portfolio project examines beauty product pricing using a dataset of Sephora product listings. It demonstrates data quality assessment, exploratory data analysis, visualization, and business interpretation.

The project is inspired by an interest in beauty retail analytics. Its findings describe the supplied Sephora dataset and should not be generalized to Ulta Beauty or the entire beauty market.

## Business Question

**How do beauty product prices vary across categories and brands, and what insights could help a beauty retailer investigate its pricing and product assortment strategy?**

## Dataset

The analysis uses `product_info.csv`, associated with the publicly available [Sephora Products and Skincare Reviews dataset on Kaggle](https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews).

The supplied file contains:

- **8,494 product listings**
- **304 brands**
- **9 primary categories**
- **27 columns**

Key fields include product name, brand, category, listed price in USD, rating, review count, and product size.

The collection date and source license should be confirmed on the dataset page before redistributing the raw file. The dataset is not assumed to reflect current prices or availability.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

## Analytical Approach

### Data Quality Assessment

- Inspect dataset dimensions, column types, and missing values.
- Check for duplicate rows and repeated product identifiers.
- Validate that prices are numeric, finite, and positive.
- Inspect expensive listings before considering any exclusions.
- Preserve missing ratings rather than replacing them with zero.

### Exploratory Analysis

- Calculate mean, median, minimum, maximum, and standard deviation.
- Compare listed prices across categories.
- Compare brands with at least 10 product listings.
- Examine price distributions and potential outliers using the interquartile range.
- Explore associations between price and customer ratings.
- Group products into clearly defined price tiers.

### Price Tier Definitions

| Tier | Listed price |
|---|---|
| Affordable | Under $25 |
| Mid-range | $25 to under $60 |
| Premium | $60 or more |

These thresholds are descriptive choices for this project, not official Sephora classifications.

## Verified Initial Findings

The initial inspection found:

- No duplicate complete rows or repeated product IDs.
- No missing, unreadable, zero, or negative values in the main price field.
- A mean listed price of **$51.66** and a median of **$35.00**.
- Listed prices ranging from **$3 to $1,900**.
- Skincare and Makeup had the most listings, with **2,420** and **2,369**, respectively.
- The Gifts category contained only **4 listings**, limiting the strength of comparisons involving that category.
- The five highest-priced listings appeared to be beauty devices or device bundles categorized as Skincare.

The difference between the mean and median suggests that expensive listings pull the average upward. High prices alone do not establish data errors.

Further category, brand, price-tier, and rating findings will be documented after reviewing the completed analysis.

## Visualizations

The notebook includes code to generate four charts:

1. **Average listed price by category** — compares category means and displays sample sizes.
2. **Product price distribution** — shows the full price range alongside a closer view up to the 99th percentile.
3. **Price variation by category** — compares distributions using boxplots on a logarithmic price axis.
4. **Products across price tiers** — displays listing counts and percentages within the defined tiers.

Charts are saved in the `visuals/` directory when their cells are executed.

## Business Applications

The analysis can support questions for further retail research, including:

- Does the listed assortment provide options across multiple price points?
- Are category averages influenced by expensive devices, bundles, or other product formats?
- Which brands warrant closer investigation for affordable or premium positioning?
- Which categories require more detailed, like-for-like comparisons?

These are potential applications, not demonstrated improvements in sales or profitability. Final recommendations will be developed after interpreting the analytical results.

## Limitations

- The dataset contains product listings, not transactions. It cannot establish demand, revenue, profitability, or market share.
- The data describes a historical snapshot rather than verified current prices.
- Product sizes, formats, devices, and bundles limit direct price comparisons.
- Categories are not all equivalent: some describe product types, while others describe formats or customer segments.
- Brand price differences may reflect differences in category mix.
- Small samples can make category and brand comparisons unstable.
- Ratings are missing for some products and are supported by different numbers of reviews.
- Correlation between price and rating does not establish causation.
- Findings describe this dataset and do not represent Ulta Beauty.

