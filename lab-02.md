Lab 02 - Plastic waste
================
Votre nom
La date

## Chargement des packages et des données

``` r
library(tidyverse) 
```

``` r
plastic_waste <- read_csv("data/plastic-waste.csv")
```

Commençons par filtrer les données pour retirer le point représenté par
Trinité et Tobago (TTO) qui est un outlier.

``` r
plastic_waste <- plastic_waste %>%
  filter(plastic_waste_per_cap < 3.5)
```

## Exercices

``` r
plastic_waste %>%
  filter(plastic_waste_per_cap > 3.5)
```

    ## # A tibble: 0 × 10
    ## # ℹ 10 variables: code <chr>, entity <chr>, continent <chr>, year <dbl>,
    ## #   gdp_per_cap <dbl>, plastic_waste_per_cap <dbl>,
    ## #   mismanaged_plastic_waste_per_cap <dbl>, mismanaged_plastic_waste <dbl>,
    ## #   coastal_pop <dbl>, total_pop <dbl>

``` r
  ggplot(data = plastic_waste, aes(x = plastic_waste_per_cap)) +
  geom_histogram(binwidth = 0.2, fill = "steelblue", color = "white") +
  labs(
    title = "Distribution des déchets plastiques par habitant (2010)",
    x = "Déchets plastiques par habitant (kg/jour ou tonne/an ?)",
    y = "Nombre de pays") +
  theme_minimal()
```

![](lab-02_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

### Exercise 1

``` r
# insert code here
```

### Exercise 2

``` r
# insert code here
```

Réponse à la question…

### Exercise 3

Boxplot:

``` r
# insert code here
```

Violin plot:

``` r
# insert code here
```

Réponse à la question…

### Exercise 4

``` r
# insert code here
```

Réponse à la question…

### Exercise 5

``` r
# insert code here
```

``` r
# insert code here
```

Réponse à la question…

## Conclusion

Recréez la visualisation:

``` r
# insert code here
```
