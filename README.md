
## 1. How would you return all the recipes in your database?

Recipe.all

## 2. How would you return all the comments in your database?

'Comment.all'

## 3. How would you return the most recent recipe posted in your database?

Recipe.last

4. How would you return all the comments of the most recent recipe in your database?

recipe = Recipe.last
Comment.where(recipe: recipe)

5. How would you return the most recent comment of all your comments?

Comment.last

6. How would you return the recipe associated with the most recent comment in your database?

Recipe.where(id: Comment.last.recipe)

7. How would you return all comments that include the string brussels in them?

Comment.where('body LIKE?', '%brussels%').all
