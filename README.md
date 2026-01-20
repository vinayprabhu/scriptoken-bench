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

