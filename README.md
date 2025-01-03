# MCQ-generation-Chain
> LLMs-enabled automatic generation of multiple-choice questions in math subjects using langchain tools, incorporating Google search and PoT assistance

## How to run
### 1. Environment Requirement

python version == 3.11.1

pip version== 24.0

### 2. Create Conda Virtual Env

run the command in root folder:

```
conda create -n MCQ
conda activate MCQ
```

### 3. Install Dependency

```
pip install -r requirements.txt
```

### 4. Replace Your Keys

open `main.py` and edit line `4` &`5`

```python
# API-KEY Settings
os.environ["OPENAI_API_KEY"] = "your openai key"
os.environ["SERPAPI_API_KEY"] = "your serpapi key"
```

Your openai api-key should be available to GPT4 model.

 SerpApi key is available if you subscribe at : https://serpapi.com/manage-api-key

### 5. Modify Question Settings

open `main.py` and edit line `7-11` 

```python
# Question settings
cnt = 1 # question quantity
knowledge = 'simple equations' # knowledge component
difficulty_level = 0 # difficulty level: 0 easy, 1 middle, 2 hard
isScene = True # Whether or not to set the context
otherRestriction = "" 
```

### 6. Run

Run the command in root folder.

```
python main.py
```

### 7. Expected Result

```
> Entering new AgentExecutor chain...

# Typical Application Problems of Simple Equations in Primary and Secondary Schools

This document summarizes common types and examples of typical application problems in primary and secondary school mathematics. These problems often involve real-life practical issues and are solved using the steps of defining unknowns, setting up equations, solving them, and obtaining answers.

---

## Common Problem Types

1. **Unification Problems**:  
   Involve converting different items or quantities into a common unit or standard for comparison or calculation.

2. **Aggregation Problems**:  
   Involve combining quantities from multiple parts into a total amount.

3. **Sum and Difference Problems**:  
   Involve the sum or difference of two or more quantities.

4. **Ratio Problems**:  
   Involve relationships of proportions between two or more quantities.

5. **Work Problems**:  
   Involve relationships between work efficiency, time, and workload.

---

## Examples

### 1. **Unification Problem Example**  
   Xiaoming and Xiaohong have 30 apples. Xiaoming has twice as many apples as Xiaohong. How many apples do each have?  

   - Let Xiaohong have \(x\) apples. Then Xiaoming has \(2x\) apples.  
   - Equation:  
     \[
     x + 2x = 30
     \]  
   - Solution:  
     \[
     x = 10 \quad \text{(Xiaohong)}, \quad 2x = 20 \quad \text{(Xiaoming)}
     \]

---

### 2. **Aggregation Problem Example**  
   A class has 20 boys. The number of girls is 10 more than the boys. How many students are in the class?  

   - Let the number of boys be \(x\). Then the number of girls is \(x+10\).  
   - Equation:  
     \[
     x + (x + 10) = 30
     \]  
   - Solution:  
     \[
     x = 10 \quad \text{(boys)}, \quad x+10 = 20 \quad \text{(girls)}, \quad \text{Total = 30}
     \]

---

### 3. **Sum and Difference Problem Example**  
   Two numbers have a sum of 50 and a difference of 10. Find these two numbers.  

   - Let the two numbers be \(x\) and \(y\).  
   - System of equations:  
     \[
     x + y = 50  
     \]  
     \[
     x - y = 10
     \]  
   - Solution:  
     \[
     x = 30, \quad y = 20
     \]

---

### 4. **Ratio Problem Example**  
   A rope is 120 cm long and is cut into two pieces, one of which is three times as long as the other. Find the lengths of the two pieces.  

   - Let the shorter piece be \(x\). Then the longer piece is \(3x\).  
   - Equation:  
     \[
     x + 3x = 120
     \]  
   - Solution:  
     \[
     x = 30 \quad \text{(shorter)}, \quad 3x = 90 \quad \text{(longer)}
     \]

---

### 5. **Work Problem Example**  
   A and B together can complete a task in 4 hours. A alone can complete the task in 6 hours. How long would B alone take to complete the task?  

   - A’s work rate: \( \frac{1}{6} \) (tasks per hour).  
   - A and B’s combined work rate: \( \frac{1}{4} \) (tasks per hour).  
   - B’s work rate:  
     \[
     \frac{1}{4} - \frac{1}{6} = \frac{1}{12}
     \]  
   - Solution:  
     B alone would take 12 hours to complete the task.

---

## How to Use This Repository

1. **Understand the Problem Type**:  
   Identify the type of application problem by analyzing its structure.

2. **Set Up the Equation**:  
   Define the unknown(s), set up the equation(s), and include the necessary conditions.

3. **Solve the Problem**:  
   Solve the equation(s) step-by-step.

4. **Validate Your Answer**:  
   Verify your solution by substituting it back into the original problem conditions.

---

### Contributions

If you have additional examples or suggestions for improving this content, feel free to submit a pull request or open an issue.

### License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

```

