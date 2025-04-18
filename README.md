# Howdy, job seeker!

Below are 3 scenarios that will allow us to get a sense for your coding chops and give you exposure to the type of work you'd be doing on a regular basis to ensure you enjoy it. This is isn’t your standard front-end dev gig, as you’ll be writing code that is inserted into websites via 3rd party testing tools like [Convert](https://www.convert.com/), [Monetate](https://www.monetate.com/), and [Visually.io](https://www.visually.io/). The below scenarios are designed to reflect that.  

## Submission

1. Create a **Github Gist** including your final JavaScript and CSS
1. Name your gist `"[yourName]-surefoot-application.md"`
1. Include a short explanation (1-2 paragraphs) describing your approach for each variation.
1. When complete, add the gist URL to your application and :shipit:

## Requirements

*   Use whatever IDE you'd like for writing the code, but **ensure the code can be executed within the browser's devtools for testing and validating functionality**—do not manually modify the site’s code.
*   **JavaScript & CSS only** (please no jQuery).
*   Your code for each variation should exceute independently (i.e. each variation does not require code from another variation in order to run successfully).
*   Ensure the test works **responsively** on both desktop and mobile.
*   Write **clean, well-commented** code.
*   Send your completed code as a public GitHub gist and share a link.
*   You may use **AI for assistance**, but please write your own code for the final implementation - we'll know!
    
## What We're Evaluating

✅ **Technical Skills**: Your ability to write clean, functional JavaScript and CSS and leverage existing APIs to display information asynchronously.

✅ **Attention to Detail**: Ensuring changes blend seamlessly with OXO’s site.

✅ **Creativity & Fun**: How well you implement the requirements without disrupting the user experience.

✅ **Problem-Solving**: Does your solution handle edge cases like excessive user interaction or API errors? Is your code bug free and does not cause any problems with the existing site when executed?

## Objective

Write code *to be executed in the browser's devtools* to modify an existing product page on [**OXO.com**](http://OXO.com). (Normally, this code would be copied to a 3rd party testing tool (see intro above), but for the purposes of evaluating your code, we'll be executing the code from the browser's devtools instead). These test variations will:

1.  Add a **subtle yet effective UX change** that could improve conversions.
2.  Include a **fun Easter egg**—a hidden GIF that appears based on user interaction.
3.  Fetch product details **from an API** and display them on the page.
4.  Follow clean, modular, and well-documented coding practices.

## Scenario

You’re working with **Surefoot** to optimize OXO’s product pages. The team wants to test whether adding **messaging near the “Add to Cart” button** can increase conversions or Average Order Value.

Additionally, because CRO should be fun, you’ll add a **hidden surprise GIF** when users interact with the page in a specific way.

## Your Task

### Variation A: Confidence Booster Message

**Target URL:** _All_ product pages (e.g. ﻿[Oxooxo.com/oxo-professional-5pc-starter-set.html](https://www.oxo.com/oxo-professional-5pc-starter-set.html)[Oxooxo.com/oxo-professional-5pc-starter-set.html](https://www.oxo.com/oxo-professional-5pc-starter-set.html)﻿)

*   Add a **small, well-styled message** below the “Add to Cart” button:
    > “OXO products are used in over 10 million kitchens. You’re in good company!”
*   Style the message so it fits seamlessly with the page.
*   Ensure the implementation can be executed **within browser devtools**, using JavaScript and CSS (not by modifying the site’s actual code).
*   Bonus (not required): Add a subtle fade-in effect when the message appears.

### **Variation B: The Easter Egg Surprise**

**Target URL:** _All_ product pages (e.g. ﻿[Oxooxo.com/oxo-pop-20-piece-pop-container-set.html](https://www.oxo.com/oxo-pop-20-piece-pop-container-set.html)[Oxooxo.com/oxo-pop-20-piece-pop-container-set.html](https://www.oxo.com/oxo-pop-20-piece-pop-container-set.html)﻿)

*   When a user **hovers over the “Add to Cart” button five times**, a hidden **funny cooking-related GIF** should appear below the button.
*   The animation should feel smooth and non-intrusive.
*   Use JavaScript and CSS to manage the logic.
*   Ensure the implementation can be executed **within browser devtools**, using JavaScript and CSS (not by modifying the site’s actual code).
*   Bonus (not required): Make the GIF disappear when the user clicks on it.
    
### Variation C: Recommended Products

**Target URL:** _Exactly_ [https://www.oxo.com/oxo-good-grips-12-piece-smart-seal-glass-container-set.html](https://www.oxo.com/oxo-good-grips-12-piece-smart-seal-glass-container-set.html)

*   Below the Add to Cart button, add a related product recommendation.
*   The new section should include a title of "You might also like" and display the **product image, name, price, and link to view full details**.
*   Style the section so it fits seamlessly with the page.
*   Ensure the implementation can be executed **within browser devtools**, using JavaScript and CSS (not by modifying the site’s actual code).
*   Use the following API request to get products in the same category, and display the first result that is returned:
    ```sh
    curl --location 'https://mvfvxhvmmt-dsn.algolia.net/1/indexes/*/queries?X-Algolia-Api-Key=OTVkZTk2YTY1YTBiNGM0MTlmYmQ5MmE4YWRmYWUxZWI0MDJiODc5YTExNGQ0MjM3OTBjODQ4NDczNTRmZWUzNmZpbHRlcnM9Y2F0YWxvZ19wZXJtaXNzaW9ucy5jdXN0b21lcl9ncm91cF8wJTIwJTIxJTNEJTIwMCZ0YWdGaWx0ZXJzPSZ2YWxpZFVudGlsPTE3NDQ5MDAwMjE%3D&X-Algolia-Application-Id=MVFVXHVMMT' \
    --header 'Content-Type: application/json' \
    --data '{
        "requests": [
            {
                "indexName": "magento2_prod_oxooxo_products",
                "params": "clickAnalytics=true&facetFilters=%5B%5B%22categories.level3%3AShop%20%2F%2F%2F%20Kitchenware%20%2F%2F%2F%20Food%20Containers%20%2F%2F%2F%20Smart%20Seal%22%5D%5D&facets=%5B%22brand%22%2C%22categories.level0%22%2C%22categories.level1%22%2C%22categories.level2%22%2C%22categories.level3%22%2C%22categories.level4%22%2C%22oxo_color%22%2C%22price.USD.group_0%22%5D&filters=categoryPageId%3A%22Shop%20%2F%2F%2F%20Kitchenware%20%2F%2F%2F%20Food%20Containers%20%2F%2F%2F%20Smart%20Seal%22&highlightPostTag=__%2Fais-highlight__&highlightPreTag=__ais-highlight__&hitsPerPage=48&maxValuesPerFacet=10&numericFilters=%5B%22visibility_catalog%3D1%22%2C%22status%3D1%22%5D&page=0&ruleContexts=%5B%22magento_filters%22%2C%22magento-category-25%22%5D&tagFilters="
            }
        ]
    }'
    ```
*   Bonus (not required): Add a carousel (with one slide visible at a time) and let the user navigate between three different products returned from the API above.
