# Extended Strings

**Note:** This is an unfinished resource pack.

**Note:** [options.languageWarning](# "Language translations may not be 100% accurate")

Extended Strings resource pack fills in missing strings by default and adds strings that might be used frequently, such as in commands.

## Available Strings

* Roman numerals for enchantment levels from XI (11) to CCLV (255) (keys are based on built-in styles)
* Time units such as "1 day", "2 weeks", and “3 month(s)”, etc. (some keys are based on built-in styles)
* Music Disc composers name
* Strings for custom colored items such as “Green Apple”, “Green Torch”, and “Magenta Torch”, etc.
* Strings for custom items with effects such as “Apple of Fire Resistance”, “Mundane Carrot”, and “Bread of Swiftness”, etc.
* String “%s Spawn Egg” for custom Spawn Egg
* “When Attacked:”, “When Used:”
* Roman numerals for effect amplifiers I (1) and from VII (7) to CCLVI (256) (keys are based on built-in styles)
* “Add”, “Apply”, “Close”
* “Copy”, “Paste”, “Cut”
* String “%s + %s” for custom keyboard shortcut
* “Learn more”, “Save”, “Search”, “Sort”, “Sort by”
* Strings “%s ago” and “%s later” to indicate before or after time
* “A few seconds”
* “Clear”, “Rain”, “Rain & Thunder”

For more information about available strings, see [the source code](https://github.com/myhttps/extended-strings/blob/main/assets/minecraft/lang/en_us.json).

## How to Use Strings

To display the word “Search”, the following commands might be used frequently:

```
/tellraw @s "Search"
/tellraw @s {"text": "Search"}
```

**Result:** English: `Search`, Japanese: `Search`, When no resource pack was used: `Search`

---

To display the word “Search (`text.type.search`)” using a string, use the following command:

```
/tellraw @s {"translate": "text.type.search", "fallback": "Search"}
```

**Result:** English: `Search`, Japanese: `検索`, When no resource pack was used: `Search`

---

To insert the word “A few seconds (`text.type.time.few`)” into %s of “%s ago (`text.type.time.ago`)”, use the following command:

```
/tellraw @s {"translate": "text.type.time.ago", "fallback": "%s ago", "with": [{"translate": "text.type.time.few", "fallback": "A few seconds"}]}
```

**Result:** English: `A few seconds ago`, Japanese: `数秒前`, When no resource pack was used: `A few seconds ago`

## Translation

Join [Crowdin](https://crowdin.com/project/extended-strings) and help me translate Extended Strings!
