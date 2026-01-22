# Scriptoken-bench
Benchmarking all the tokenizer vocabularies through the Unicode-script lensing

| Model         | Type           | Vocab Size | Samples                                                                                               |
|---------------|----------------|------------|-------------------------------------------------------------------------------------------------------|
| GPT-OSS       | BPE (Tiktoken) | 200019     | 'Arb', 'переп', 'notify', 'तान', 'zak'                                                                |
| Llama-4       | BPE (Tiktoken) | 201135     | 'ÄĲáº·c', 'odziel', 'une', 'Consider', 'weich'                                                        |
| Mistral       | BPE (Tekken)   | 131072     | 'skirts', 'Empty', '"),Ċ', 'ìĿ¸ë¯¼', 'hatt'                                                           |
| Gemma-3       | SentencePiece  | 262145     | 'setOnAction', '▁Exist', '▁Fah', '教会', '<unused3749>'                                                 |
| GLM-4         | BPE (Tiktoken) | 151343     | 'b' Provision'', 'b' pr\textbackslash xc3\textbackslash xb3xima'', 'b' newVal'', 'b'yii'', 'b'nicas'' |
| Qwen-2.5      | BPE            | 151665     | 'hacking', 'datable', '-ring', 'plung', 'ĉti'                                                         |
| DeepSeek-V3   | BPE            | 128815     | 'Industrial', 'Revenue', 'å¾ĹäºĨ', 'ãģłãģĳãģ§', 'å¾ĭ'                                                 |
| Phi-4         | BPE            | 100352     | 'rein', 'audio', 'perse', '.Gray', '\%-'                                                              |
| RNJ-1         | SentencePiece  | 128256     | 'transition', 'req', 'ÎºÎ±', 'aisy', 'Ð»ÑİÐ´ÐµÐ¹'                                                     |
| OLMo-3        | BPE            | 100278     | 'hasta', 'acquiring', 'lu', 'XmlElement', 'amendments'                                                |
| All\_combined | N/A            | 1555080    | Total Aggregate Vocabulary                                                                            |
## Ratios

| Tokenizer | Vocabulary Size | % of Dataset |
|-----------|----------------|--------------|
| Gemma-3 | 262,145 | 16.86% |
| Llama-4 | 201,135 | 12.93% |
| GPT-OSS | 200,019 | 12.86% |
| Qwen-2.5 | 151,665 | 9.75% |
| glm-4-9b-chat | 151,343 | 9.73% |
| Mistral | 131,072 | 8.43% |
| DeepSeek-V3 | 128,815 | 8.28% |
| RNJ-1 | 128,256 | 8.25% |
| Phi-4 | 100,352 | 6.45% |
| OLMo-3 | 100,278 | 6.45% |

##

**STS Perspective -   Representation:**
- **Hemispheric bias**: 77.44% of all tokens represent Latin-centric scripts (Latin, Common, Inherited), while 22.56% cover all other world languages combined

  **Top 5 Most Represented Scripts:**
  1. **Latin**: 1,051,942 tokens (67.65%)
  2. **Han** (Chinese): 137,815 tokens (8.86%)
  3. **Cyrillic**: 85,253 tokens (5.48%)
  4. **Common** (symbols, punctuation): 79,131 tokens (5.09%)
  5. **Arabic**: 43,366 tokens (2.79%)

 **Latin-Centric Dominance:**
  - Latin + Common + Inherited scripts: **77.44%**
 - All other scripts combined: **22.56%**

- **Severe digital divide**: 50 scripts (60% of all scripts) have less than 0.01% representation, creating a multi-tiered linguistic hierarchy
- **High inequality**: Gini coefficient of 0.9502 indicates extreme concentration of tokenizer resources in a small number of scripts
- **Tokenization inefficiency**: Non-Latin scripts show higher fragmentation, requiring more tokens to encode the same semantic content

**LLM Attacks Perspective - Security Vulnerabilities:**
- **Adversarial opportunities**: 22 "stealth scripts" present in only one tokenizer create asymmetric attack surfaces
- **Jailbreaking vectors**: 61 underrepresented scripts (<0.1%) could bypass content filters due to limited training coverage
- **Homoglyph attacks**: 13,506 mixed-script tokens (0.87%) enable character substitution attacks across 9 major script pairs
- **Cross-model inconsistencies**: 21 scripts show inconsistent coverage (3-7 tokenizers), enabling model-specific exploits
- **Fairness attacks**: Extreme representation disparities can be exploited to generate biased outputs favoring Western languages

These findings have profound implications for both AI equity and security, highlighting the need for more inclusive tokenizer design and robust security measures against script-based attacks.




#### Token length findings

Average token length by script (top 20 scripts):

| Script | Mean Length | Std Dev | Interpretation |
|--------|-------------|---------|----------------|
| SPECIAL_TOKEN | 12.47 | 39.71 | Control tokens |
| Mixed_Han_Hiragana | 9.83 | 3.11 | High fragmentation |
| Greek | 8.62 | 3.28 | Moderate efficiency |
| Bengali | 8.60 | 3.20 | Moderate efficiency |
| Malayalam | 8.55 | 3.14 | Moderate efficiency |
| Tamil | 8.53 | 3.08 | Moderate efficiency |
| Latin | 5.52 | 3.38 | **High efficiency** |
| Common | 2.92 | 2.74 | Very high efficiency |


**Jailbreaking Candidate Scripts (< 0.1% representation):**

| Script | Token Count | Tokenizer Coverage | Jailbreak Risk |
|--------|-------------|-------------------|----------------|
| Mixed_Hiragana_Latin | 4 | 1 | **Critical** |
| Samaritan | 4 | 1 | **Critical** |
| Limbu | 3 | 1 | **Critical** |
| Lepcha | 1 | 1 | **Critical** |
| Glagolitic | 9 | 1 | **High** |
| Phoenician | 6 | 1 | **High** |
| Gothic | 10 | 1 | **High** |
| Mandaic | 6 | 1 | **High** |
| Buginese | 5 | 1 | **High** |
| Old_Persian | 1 | 1 | **High** |

