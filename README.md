# Meal Planner

A phone app for your recipes: keep them in one place, plan breakfast, lunch, dinner and a snack for each day, and get a shopping list for the week. Works in English and Russian.

**Use it as a phone app:** open the GitHub Pages address in Chrome on Android, then tap ⋮ → **Install app** (or **Add to Home screen**). It opens full screen with its own icon and works offline.

## Files

- `meal-planner.html` is the page itself. The same file can be published as a Claude artifact.
- `build.py` wraps it into `index.html` with the app manifest and offline support. Run `python3 build.py` after editing `meal-planner.html`, and bump the cache name in `sw.js` so installed phones pick up the change.
- `manifest.webmanifest`, `sw.js` and `icons/` make it installable and work offline.

## Features

- **Today:** today's four meals as cards, with tomorrow's menu beside them. Tap a meal to swap it, keep it, change servings or open the recipe.
- **Week:** seven day cards with a slot for breakfast, lunch, dinner and snack. **Plan my week** fills the empty slots from today on, picking recipes you haven't had for a while and avoiding repeats in the same week and on the same day. **Reshuffle** swaps every meal you haven't kept; **Clear** empties them.
- **Recipes:** name, which meals it's good for, servings, time, ingredients, method and notes. Search and filter by meal, and see when each recipe was last planned or is planned next.
- **Coffee:** a separate Coffee section in Recipes, apart from the meals, so coffee is never planned into the week. A coffee recipe's **Add to shopping list** puts its ingredients under Also buy. Pasted recipes that mention coffee, espresso or latte land here.
- **Recipe ideas:** a built-in set of meal and coffee ideas, marked Idea: no lactose, no mushrooms, onion, broccoli, baked peppers or sour cream, no soups, and every ingredient easy to buy in Serbia. New ideas are added once; deleted ones don't come back.
- **Paste from ChatGPT:** paste a recipe (or several) copied from a ChatGPT chat. The app finds the title, servings, time, ingredients and steps in English or Russian, then shows the form so you can check it before saving. While you edit, it shows the amounts it understood for each ingredient.
- **Shopping:** a list built from the planned meals for the rest of this week or for next week. Matching ingredients are added up (so 1 onion plus 2 onions is 3 onions, and grams become kilograms), scaled to the servings you planned, and grouped by aisle. Spices and oil are grouped separately to check at home. Tick items off, add extra items, or copy the list into a note or message.
- **English and Russian:** switch with EN / RU at the top. The example recipes switch language too; your own recipes stay as you wrote them.
- **Examples:** a new install starts with example recipes and a planned week so you can try everything. **Remove examples** deletes them and their meals.
- **Colour theme:** Auto (follows your phone), Light or Dark, next to EN / RU at the top. The choice is shared with the other apps on nurnhe.github.io, so switching it in one switches them all.

## Data

Everything is saved on the device in the browser's `localStorage`. **Recipes → Back up** saves a backup file and **Restore** loads one, for example to move to a new phone.

## Credits

Icons are inlined SVG from [Tabler Icons](https://github.com/tabler/tabler-icons) (MIT License). Fonts: Unbounded and Nunito (both with Cyrillic), from Google Fonts (SIL Open Font License).
