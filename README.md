# Zero-Shot-Classification-using-GPT-3.5-

The primary task of this project is to evaluate the performance of the GPT-3.5 Turbo model in answering multiple-choice questions. The code provided here is a part of this evaluation process. Specifically, it's aimed at assessing how well the model can answer questions by comparing its responses to the correct answers.

## Requirements

Before running this code, make sure you have the following requirements in place:

- An OpenAI API key: You'll need to sign up for and obtain an OpenAI API key, which should be set as the `openai.api_key` variable in the code.

- Python and Libraries: You should have Python installed on your system along with the necessary libraries such as `openai`, `requests`, `json`, and `pandas`.

- Dataset: You need a dataset containing multiple-choice questions and answers. In this example, the code reads data from a CSV file named 'llmtrain.csv'.

## Usage

Here's how the code works:

1. **Data Loading**: The code reads the dataset from a CSV file into a Pandas DataFrame. The dataset should have columns such as 'id', 'prompt', 'A', 'B', 'C', 'D', 'E', and 'answer'.

2. **Interaction with GPT-3.5 Turbo**: For each question in the dataset, the code calls the `generate_answer` function. This function interacts with the GPT-3.5 Turbo model to generate answers. The model is provided with context through system and user messages.

3. **Scoring**: The model's answers are compared to the correct answers provided in the dataset. A scoring system is used to award points to the model's responses. The scoring system is designed to give higher scores for correct answers that were guessed earlier.

4. **Average Score Calculation**: After processing a set number of questions (in this example, the first 100), the code calculates the average score of the model's performance. The average score is indicative of how well the model answered these specific questions.

## Example Output

Here's an example of the output you can expect:

```python
Average Score: 0.7266666666666666
```

This score indicates the model's average performance across the first 100 multiple-choice questions.

## Additional Notes

- You can modify the code to work with your specific dataset and adjust the number of questions you want to evaluate.

- The code also includes a function (`generate_answer`) for interacting with the GPT-3.5 Turbo model. This function is designed to set up the conversation with the model and extract its responses.

- Make sure you have the necessary permissions and access to the OpenAI GPT-3.5 Turbo model for API interactions.

- This is just a simple example of using GPT-3.5 Turbo for multiple-choice question answering. You can further customize it to suit your specific use case.

Feel free to use this code as a starting point for your own evaluation of the GPT-3.5 Turbo model's performance in multiple-choice question answering.
