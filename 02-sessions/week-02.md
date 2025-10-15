# Week 02 – AI-900: Azure AI Fundamentals, ML & Agent Scenarios

## 📚 Topics Covered
- Fundamentals of **AI and Machine Learning** in Azure (ML models, training, inference).  
- Core AI workloads: computer vision, NLP (Natural Language Processing), generative AI.  
- Responsible AI principles and considerations (fairness, transparency, privacy).  
- Exploring **agent scenarios** and generative AI in practice (via Microsoft’s AI sims lab).  
- Hands-on lab: **Explore AI agent scenarios** (using this lab:  
  https://microsoftlearning.github.io/mslearn-ai-sims/Instructions/Labs/02-explore-ai-agent.html).

## 🧰 Tools & Setup
- Azure AI / Cognitive Services or ML tools configured (or access via sandbox).  
- Access to the AI sims lab environment (browser, APIs, etc.).  
- Reference to Microsoft Learn / AI-900 exam study materials.  

## 🧑‍💻 Code & Examples
```python
# Example pseudocode or sample for agent logic
def simple_agent(input_text):
    # call Azure OpenAI / cognitive API
    response = call_openai_model(prompt=input_text)
    return response

# Example: generate a response
print(simple_agent("What’s the weather like today?"))
