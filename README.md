SocialPreText
SocialPreText is a professional-grade Python utility for cleaning and preprocessing social media text. It is designed to prepare noisy data for Natural Language Processing (NLP) tasks by normalizing slang, contractions, and social media-specific tokens.

Installation
Install the package directly from PyPI using pip:

pip install socialpretext
Quick Start: The One-Step Solution
The clean_all function is the primary entry point. It runs a pre-defined sequence of cleaning steps to transform messy text into clean, usable English.

Python
from socialpretext import clean_all

raw_text = "OMG idk, @user! This update is lit 🔥 Check it out: [https://example.com](https://example.com) #tech"

# Run the default cleaning pipeline
cleaned = clean_all(raw_text)

print(cleaned)
# Output: "oh my god i do not know this update is amazing check it out"
API Reference & Function Syntaxes
Below are the functions available in the package. Each can be imported and used individually for granular control over your text processing.

The Main Pipeline
socialpretext.clean_all(text, pipeline_steps=None): The master function. Accepts a string and an optional list of steps to run. If no steps are provided, it runs the full default suite.

Content Expansion
socialpretext.expand_slang(text): Converts internet shorthand into formal English. Example: "idk" becomes "I do not know".

socialpretext.expand_contractions(text): Expands standard English contractions. Example: "it's" becomes "it is".

Token Removal
socialpretext.remove_urls(text): Strips out http, https, and www web links.

socialpretext.remove_mentions(text): Removes @username mentions from the text.

socialpretext.remove_hashtags(text): Removes #hashtags while keeping the rest of the sentence intact.

socialpretext.remove_punctuation(text): Strips all standard punctuation marks (e.g., !, ?, .).

Emoji Handling
socialpretext.remove_emojis(text): Completely deletes emoji characters from the string.

socialpretext.demojize(text): Replaces emojis with their text descriptions. Example: "🔥" becomes ":fire:".

Formatting
socialpretext.normalize_whitespace(text): Fixes formatting by replacing multiple spaces or newlines with a single space.

Author
Akash Goyal (akashpgoyal@gmail.com)
