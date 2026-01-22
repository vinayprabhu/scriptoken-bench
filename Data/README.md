# List of data-assets share here

1. **df_tokka_bench_2026.tsv** : Size(1555080, 5) | Columns | 
- 'model_tokenizer_name': Top-10 models: [['GPT-OSS', 'Llama-4', 'Mistral', 'Gemma-3', 'Qwen-2.5',
       'DeepSeek-V3', 'Phi-4', 'RNJ-1', 'OLMo-3', 'glm-4-9b-chat']
- 'tokenizer_token_index' : Index mapping to the token in that model's tokenizer
-  'token': Example: ["b'!'", 'b\'"\'', "b'#'", "b'$'", "b'%'"]
-  'decoded_token': Example: ['!', '"', '#', '$', '%']
-  'script': 83 values:
    - ['Common', 'Latin', 'Cyrillic', 'Arabic', 'Devanagari', 'Georgian',
       'Hebrew', 'Armenian', 'Malayalam', 'Greek', 'Bengali', 'Han',
       'Gujarati', 'Tamil', 'Kannada', 'Telugu', 'Thai', 'Hangul',
       'Inherited', 'Hiragana', 'Katakana', 'Gurmukhi', 'Sinhala',
       'Khmer', 'Myanmar', 'Mixed_Han_Hiragana', 'Oriya',
       'Mixed_Han_Latin', 'Unknown', 'Tibetan', 'Braille',
       'Mixed_Han_Katakana', 'Mixed_Cyrillic_Latin', 'Lao',
       'BYTE_FRAGMENT', 'Ethiopic', 'Thaana', 'SPECIAL_TOKEN',
       'Mixed_Hiragana_Katakana', 'Mixed_Greek_Latin',
       'Mixed_Hiragana_Latin', 'Syriac', 'Mixed_Katakana_Latin',
       'Cherokee', 'Ogham', 'Ol_Chiki', 'Tifinagh', 'Cuneiform', 'Coptic',
       'Canadian_Aboriginal', 'Vai', 'Bopomofo', 'Egyptian_Hieroglyphs',
       'Yi', 'Mongolian', 'Javanese', 'Old_Turkic', 'Kaithi', 'Tai_Le',
       'Meetei_Mayek', 'Nko', 'Tai_Viet', 'Bamum', 'New_Tai_Lue', 'Runic',
       'Mandaic', 'Phags_Pa', 'Tai_Tham', 'Balinese', 'Buginese',
       'Gothic', 'Limbu', 'Sundanese', 'Batak', 'Lepcha', 'Phoenician',
       'Glagolitic', 'Samaritan', 'Lisu', 'Cham', 'Old_Persian',
       'Inscriptional_Parthian', 'Modi']
       
2. **df_unicode_17.tsv**
- Shape: (159866, 5)
- Background: 
- There are 1,114,112 = 220 + 216 or 17 × 216 = 0x110000 code points up for grabs
- (As of Unicode 17.0, released in September 2025)
  - 303,808 (27%) of these code points are allocated
  - 159,866 (14%) have been assigned characters (This dataframe)
    - 159,629 graphical characters (some of which do not have a visible glyph, but are still counted as graphical)
    - 237 special purpose characters for control and formatting.
  - 137,468 (12%) are reserved for private use
  - 2,048 are used to enable the mechanism of surrogates
  - 66 are designated as noncharacters
  - 810,304 (73%) unallocated.
  - The number of encoded characters is made up as follows: 

