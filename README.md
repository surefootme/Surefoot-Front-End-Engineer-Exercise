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

**Target URL:** _All_ product pages (e.g. ﻿[oxo.com/oxo-professional-5pc-starter-set.html](https://www.oxo.com/oxo-professional-5pc-starter-set.html), [oxo.com/oxo-professional-5pc-starter-set.html](https://www.oxo.com/oxo-professional-5pc-starter-set.html)﻿)

*   Add a **small, well-styled message** below the “Add to Cart” button:
    > “OXO products are used in over 10 million kitchens. You’re in good company!”
*   Style the message so it fits seamlessly with the page.
*   Ensure the implementation can be executed **within browser devtools**, using JavaScript and CSS (not by modifying the site’s actual code).
*   Bonus (not required): Add a subtle fade-in effect when the message appears.

### Variation B: The Easter Egg Surprise

**Target URL:** _Exactly_ [https://www.oxo.com/compact-cold-brew.html](https://www.oxo.com/compact-cold-brew.html)

*   When a user **hovers over the “Add to Cart” button five times**, a hidden GIF should appear below the button.
*   Use this GIF: https://www.oxo.com/media/magefan_blog/2018/10/ezgif.com-resize.gif
*   The GIF insertion should feel smooth and non-intrusive.
*   The GIF should **disappear** when the user clicks on it. **Reset the experience** so the GIF is shown again after the user hovers over the "Add to Cart" button 5 more times.
*   Use JavaScript and CSS to manage the logic.
*   Ensure the implementation can be executed **within browser devtools**, using JavaScript and CSS (not by modifying the site’s actual code).
    
### Variation C: Recommended Products

**Target URL:** _Exactly_ [https://www.oxo.com/oxo-good-grips-12-piece-smart-seal-glass-container-set.html](https://www.oxo.com/oxo-good-grips-12-piece-smart-seal-glass-container-set.html)

*   Below the Add to Cart button, add a related product recommendation.
*   The new section should include a title of "You might also like" and display the **product image, name, price, and link to view full details**.
*   Style the section so it fits seamlessly with the page.
*   Ensure the implementation can be executed **within browser devtools**, using JavaScript and CSS (not by modifying the site’s actual code).
*   Use the following API request to get products in the same category, and display the first result that is returned:
    ```sh
    curl --location 'https://mvfvxhvmmt-dsn.algolia.net/1/indexes/*/recommendations' \
        --header 'Content-Type: application/json' \
        --header 'X-Algolia-API-Key: ab2c55cb9b5c14cc40a50f16dde51a90' \
        --header 'X-Algolia-Application-ID: MVFVXHVMMT' \
        --data '{
            "requests": [{
                "indexName": "magento2_prod_oxooxo_products",
                "objectID": "5632",
                "model": "related-products",
                "maxRecommendations": 3,
                "threshold": 0
            }]
        }'
    ```
*   Bonus (not required): Add a carousel (with one slide visible at a time) and let the user navigate between three different products returned from the API above.
