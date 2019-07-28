# Recipe List
The idea is that it would be a web app that lets you enter the ingredient list for recipes that you know, and also the
quantities of those ingredients which you are able to buy at your local shops and whether they spoil and how much they
cost.

Then you can go to a weekly meal planning screen, and as you add recipes it will show you what quantities of what
ingredients are going to be used, and how much is going to get wasted.

Yeah that is the general idea.

## Implementation
Backend will be an API, then there will be a web app that works on desktop and mobile and that is pretty much it.
Api should be stateless pretty much so that it's easy to test.

## Data Types
Pretty much all data is going to be user specific I think, since they enter it themselves.

User <- List
List << Recipe (via RecipeUsage)
List << Ingredient (via IngredientUsage)
User <- Recipe
Recipe <- Ingredient
Ingredient <- Quantity
Ingredient <- IngredientUsage
Quantity <- IngredientUsage
