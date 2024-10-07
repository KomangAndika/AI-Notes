# Fine-Tuning-LLM
Most LLM are created on the basis of general use, while they are powerful, they lack the ability of specific use case or special domain. <br>
By fine-tuning the model you can increase the accuracy and the knowledge base of the model on specific domain <br>
Fine-tuning basically adjusting parameters of the pre-trained LLM to a specific task or domain, fine-tuning addressing the general knowledge of an LLM by allowing the model to learn from domain-specific data to make it more accurate and effective for the intended use case. <br>

## At what point i need fine-tuned LLM
#### a. Customization
- Every domain or task hasi its own terminologies, patterns, and contextual nuances. By fine-tuning the LLM, it can understand the task better or the specific knowledge.
- The fine-tuning data can be a legal documents, medical reports, business analytics, or internal comapny data.

#### b. Data Compliance
- Many industries like healthcare, finance, and law, strict regulations govern the use and hadling of sensitive information. Organizations can ensure the model follow the data comliance standards by fine-tuning the LLM on proprietary or regulated data.

#### c. Limited Labeled Data
- In the real word, large quantities of labeled data for specific task is hard to find or very costly. Fine-tuning allows allows organization to leverage pre-existing labeled data more effectively by adapting a pre-trained LLM to the dataset, maximizing its utility and performance.

## Primary fine-tuning Approach
#### a. Feature Extraction (repurposing)
- Feature extraction or repurposing is a primary approach in fine tuning. Pre-trained LLM is treated as a fixed extractor. The model, having been trained on vast dataset, has already learned that can be repurposed for the specific task ath hand. 
- The final layers of the model are then trained on the task-specific data while then rest of the model stay frozen. This approach leverages rich representations learned by the LLM and adapts them to the specific task, offering a cost-effective and efficient way to fine-tune LLMs.
#### b. Full Fine-tuning
- In feature extraction only the final layer are adjusted, full fine-tuning involves training the entire model on the task-specific data. This means all the model layer are adjusted.
- This approach beneficial when task-specific dataset is large and significantly different from the pre-training data. But this approach requires more computational resources and time compared to feature extraction.




## Source
[Turing website](https://www.turing.com/resources/finetuning-large-language-models)