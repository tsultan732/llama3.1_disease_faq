## llama3.1_disease_faq
This project involves scraping a dataset of disease-related FAQs, which includes question-answer pairs about various health conditions. I developed a baseline model using Llama 3.1 to demonstrate initial capabilities. Fine-tuning Llama 3.1 on a larger dataset with extensive hyperparameter tuning can be time-consuming, so this baseline model serves as a starting point for further development.

## Data Processing
1. **Data Scraping:** I scraped the FAQs dataset from "https://www.medindia.net/patients/diseasefaqs/" and saved it in JSON format.
2. **Data Augmentation:** The original dataset was small, so I augmented it to create a larger dataset.
3. **Data Preparation:** After augmentation, I removed the original data from the augmented dataset. I used the filtered augmented dataset as the training set and retained the original dataset as the evaluation dataset.

## Challenges and Solutions
Fine-tuning Llama 3.1 can be very time-consuming, especially when using free GPUs like those provided by Google Colab, which have limited usage time. Interruptions in runtime can force you to restart the fine-tuning process from scratch.

To address this, I referenced Maxime Labonne's blog on Hugging Face and the unslothai GitHub repository. I included an evaluation dataset and modified the code to save checkpoints every 500 steps. This approach ensures that if the runtime is interrupted, I can resume fine-tuning from the last saved checkpoint rather than starting over, effectively managing limited GPU resources.

## Future Updates
As this is a baseline model, fine-tuning with different hyperparameter sets may take longer. I plan to keep updating the code file (.ipynb) to reflect improvements and results from ongoing fine-tuning experiments. Check back for updates as I experiment with various configurations to enhance model performance.

## Credits
- Special thanks to [Maxime Labonne's blog](https://huggingface.co/blog/mlabonne/sft-llama3) for insights on faster fine-tuning Llama3.1.
- Thanks to the [unslothai GitHub repository](https://github.com/unslothai/unsloth) for valuable reference and implementation guidance.
