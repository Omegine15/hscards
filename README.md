# 🃏 Hearthstone Complete Card Archive

Complete archive of **ALL Hearthstone cards** optimized for AI analysis with Perplexity.

## 📦 What's Included

This archive contains every Hearthstone card ever released, organized into:

1. **`collectible_cards.json`** - Cards you CAN add to decks (~3,000+ cards)
2. **`tokens.json`** - Cards generated during gameplay that CANNOT be added to decks (~1,500+ cards)
3. **`metadata.json`** - Dataset information and statistics

## 🚀 Quick Start

### Generate the Archive

```bash
python fetch_cards.py
```

This will download the latest card data from HearthstoneJSON and create the JSON files.

### Requirements

- Python 3.6 or higher
- No external dependencies (uses standard library only)

## 📋 Card Data Structure

Each card contains comprehensive information:

```json
{
  "id": "CS2_200",
  "name": "Boulderfist Ogre",
  "cardClass": "NEUTRAL",
  "type": "MINION",
  "rarity": "FREE",
  "cost": 6,
  "attack": 6,
  "health": 7,
  "text": "",
  "flavor": "He's got fists like boulders!",
  "artist": "Nate Bowden",
  "collectible": true,
  "set": "CORE",
  "_note": "This card CAN be added to decks"
}
```

### Available Attributes

Not all cards have all attributes, but common fields include:

- **`id`** - Unique card identifier
- **`name`** - Card name
- **`cardClass`** - Class (e.g., MAGE, WARRIOR, NEUTRAL)
- **`type`** - Card type (MINION, SPELL, WEAPON, HERO, etc.)
- **`rarity`** - FREE, COMMON, RARE, EPIC, LEGENDARY
- **`cost`** - Mana cost
- **`attack`** - Attack value (minions/weapons)
- **`health`** / **`durability`** - Health (minions) or Durability (weapons)
- **`text`** - Card effect/ability text
- **`flavor`** - Flavor text
- **`artist`** - Artist name
- **`set`** - Expansion/set name
- **`mechanics`** - Array of mechanics (e.g., ["BATTLECRY", "TAUNT"])
- **`race`** - Minion tribe (BEAST, DRAGON, MECH, etc.)
- **`collectible`** - Whether the card can be added to decks

## 🤖 Using with Perplexity

### Upload the Files

1. Go to [Perplexity](https://www.perplexity.ai/)
2. Click the attachment icon to upload files
3. Upload `collectible_cards.json` and/or `tokens.json`
4. Ask your questions!

### Example Queries

**Deckbuilding:**
- "What are the best neutral cards for aggro decks under 4 mana?"
- "Show me all Paladin cards with Divine Shield"
- "Which legendary minions have Battlecry effects?"

**Meta Analysis:**
- "What are the most powerful spells for Mage in terms of value?"
- "List all cards that generate other cards"
- "Which cards synergize with Demon Hunter's hero power?"

**Card Evaluation:**
- "Analyze this card for Arena: [card name]"
- "What cards counter Deathrattle strategies?"
- "Find all cards that deal direct damage to the enemy hero"

**Tribal/Synergies:**
- "Show me all Beast cards that buff other Beasts"
- "What are the best Mech cards for a synergy deck?"
- "List all cards that interact with Dragons"

## 📊 Data Source

- **Source**: [HearthstoneJSON](https://hearthstonejson.com/)
- **API**: `https://api.hearthstonejson.com/v1/latest/enUS/cards.json`
- **Language**: English (enUS)
- **Updates**: Run the script again to get the latest cards after new expansions

## 🔄 Updating the Archive

Hearthstone releases new cards regularly. To update your archive:

```bash
# Simply run the script again
python fetch_cards.py
```

This will download the latest card data and regenerate all files.

## 📝 File Sizes

Approximate file sizes:

- `collectible_cards.json`: ~3-4 MB
- `tokens.json`: ~1-2 MB
- `metadata.json`: ~2 KB

**Total**: ~5-6 MB (easy to upload to any AI platform)

## 💡 Pro Tips

1. **Focus on collectible cards** for deckbuilding advice
2. **Use tokens.json** to understand card generation mechanics
3. **Check metadata.json** for dataset statistics
4. **Filter by set** to focus on Standard or Wild formats
5. **Search by mechanics** to find specific card abilities

## 🎯 Use Cases

✅ Deckbuilding assistance  
✅ Meta analysis  
✅ Card interaction queries  
✅ Strategy recommendations  
✅ Arena/Draft evaluation  
✅ Learning card mechanics  
✅ Theorycrafting new decks  

## 🛠️ Troubleshooting

**Script fails to download:**
- Check your internet connection
- The API might be temporarily down
- Try again in a few minutes

**Files are empty:**
- Make sure you have write permissions in the directory
- Check that the script completed without errors

**Old card data:**
- Run the script again to fetch the latest updates

## 📜 License

Card data provided by [HearthstoneJSON](https://hearthstonejson.com/).  
Hearthstone® is a trademark of Blizzard Entertainment, Inc.

---

**Enjoy building amazing decks! 🎮✨**
