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

## Prominent Fine-Tuning Methods
### a. Supervised fine-tuning
- In this method model trained on tas-specific labeled dataset. Model learns to adjust its parameters to predict these labels as accurately as possible. Guiding the pre-existing knowledge to specific task at hand. <br>
Some common supervised fine-tuning techniques are:
1. Basic hyperparameter tuning
Involves manually adjusting the model hyperparameters, such as the learning rate, batch size, and the number of epochs, until reached the desired performance.
2. Transfer learning
Beneficial with limited task-specific data. In this approach, a model pre-trained on large, general data is used as a starting point. <br>
The model then fine-tuned on task-specific data, allowing it to adpt its pre-existing knowledge to the new task.
3. Multi-task learning
Model fine-tuned on multiple related task simultaneously. The idea is leveraging commonality across tasks to imporve performance. Works better when the tasks are closely related or when there is limited data for individual task. Require labeled dataset for eacht ask.
4. Few-shot learning
Making the model adapt to new task with little task-specific data, the idea is leverage vast knowledge base and learn from just a few examples of the task. Beneficial when the task-specific labeled data is scarce. <br>
Can also be integrated into the RLHF method if the small amount of data also include human feedback that can guide the model's learning process.

### b. Reinforcement Learning From Human Feedback (RLHF)
1. Reward modeling
Model generate several possible outputs and human evaluators rank or rate these outputs based on their quality. The model then learns to predict these human-provided rewards and adjusting for better score.
2. Proximal policy optimization
PPO is iterative algorithm that updates language model's policy to maximize the expected reward. The core idea is take action that improve policy while ensuring the changes no too drastic from previous policy. Achieved by introducing constraint on the policy update that prevent harmful large update while still allowing beneficial small updates.

### c. Low-Rank Adaptation (LoRA)
- Highly effective method for fine-tuning, makes possible to run a specialized LLM model on a single machine.
- The process basically freezing the original model weights and applying changes to a separate set of weights, which then added to the original parameters. LoRA transforms the model params into lower-rank dimension, reducing number of params that need training, speeding up and lowering cost.
- This useful when multuple clients need fine-tuned models for different applications, allows for creating set of weights for each specific use case without the need for separate models.

### d. Adapters
Source:
[Finetuning LLMs Efficiently with Adapters by Sebastian Raschka, PhD](https://magazine.sebastianraschka.com/p/finetuning-llms-with-adapters)




## Source
[Turing website](https://www.turing.com/resources/finetuning-large-language-models)