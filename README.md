

# **Product Recommendation System**

This Python project recommends products based on the input product category and budget. The model uses **OpenAI GPT** along with the **LangChain** library to generate relevant product recommendations.

## **Features**:
- **Product Recommendation**: Get product recommendations for a given product category and budget.
- **User-friendly**: Simply input the desired product type (e.g., mobile, laptop) and your budget, and the model will recommend products accordingly.

## **Requirements**:
- Python 3.x
- OpenAI API Key
- LangChain
- Python-dotenv

Install the necessary dependencies:
```bash
pip install openai langchain python-dotenv
```

## **Setup**:

### 1. Get Your OpenAI API Key:
- Visit [OpenAI API](https://platform.openai.com/) to generate your API key.
- Store the key in a `.env` file like this:
  ```
  OPENAI_API_KEY=your_api_key_here
  ```

### 2. Clone this Repository:
```bash
git clone https://github.com/sanjushri777/Recommendation-chatbot.git
cd Recommendation-chatbot
```

### 3. Load the Environment Variables:
Ensure that your `.env` file with the `OPENAI_API_KEY` is in the same directory as your script.

### 4. Run the Script:
```bash
python product_recommendation.py
```

### 5. Input Your Product and Budget:
- The program will prompt you to input a product category (e.g., "mobile", "laptop").
- Then, input your desired budget (e.g., 5000).

Example:
```
ENTER THE PRODUCTS: mobile
ENTER THE BUDGET: 5000
```

The program will provide a list of recommendations, like:

```
Recommendation:
1. Xiaomi Redmi 7A
2. Samsung Galaxy M01
3. Realme C2
4. Nokia 2.2
...
```

---

## **How the Model Works**:

1. **User Input**: The user provides the type of product they are looking for and the maximum budget.
   
2. **Prompt Engineering**: The LangChain `ChatPromptTemplate` is used to structure the query to the model, asking for product recommendations based on the user input.

3. **Model Interaction**: The `ChatOpenAI` model processes the input and generates recommendations accordingly.

4. **Output Parsing**: The response is parsed using LangChain's `StrOutputParser` to display a clean list of product recommendations.

---

## **Pros**:
- Quickly get recommendations based on your budget.
- User-friendly interface for interacting with the model.

## **Cons**:
- Recommendations may depend on the model's training data, which could limit the variety or accuracy of the results.
- OpenAI API key required for usage.

---

## **License**:
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

