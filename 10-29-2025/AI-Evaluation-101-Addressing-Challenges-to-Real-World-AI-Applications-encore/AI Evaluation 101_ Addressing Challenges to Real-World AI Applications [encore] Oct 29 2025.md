# AI Evaluation 101: Addressing Challenges to Real-World AI Applications [encore]

October 29, 2025, 11:45 am

## Notes

### **AI Capabilities and Future Outlook**
- The group recognized a shift in AI strengths from traditional logic-based reasoning to creative, intuitive generation, reshaping how we view AI-human differences and future AI progress (03:38).
- **Rohit** highlighted that early AI models focused on logic and rules, but modern deep learning resembles human intuitive thinking, excelling at creative token generation rather than strict reasoning (03:38).  
    - This shift surprised many, as AI's creative abilities challenge the old idea that humans are uniquely creative while AI is purely logical.  
    - The team noted this reframes the human-AI comparison to integration of logic and intuition rather than a strict either/or.  
    - This new understanding impacts product design by encouraging blending AI creativity with human oversight.  
    - It also adjusts expectations around AI’s role, emphasizing augmentation over replacement in cognitive tasks.  
- The group remained optimistic about AI’s continued evolution despite concerns about hitting a scaling wall, with most believing progress will persist, especially through recombining current AI "kernels" into new agent systems that transform workflows (06:38).  
    - Rohit used historical tech analogies like transistors and packet switching to illustrate how foundational AI components can enable future revolutions despite limits on core intelligence growth.  
    - The emerging decade of "agents" was seen as a key growth area, building on existing AI capabilities to create impactful, flexible systems.  
    - This optimism drives continued investment in agent frameworks and multi-tool integrations as strategic priorities.  
    - Potential risks include stagnation if core intelligence improvements plateau, but creative recombination mitigates that risk.  
### **Challenges and Strategies in AI Evaluation**
- Ensuring AI systems reliably meet task goals requires robust evaluation frameworks tailored to specific use cases, balancing cost, accuracy, and scalability (14:15).
- The team agreed on a working definition of an **evaluation (eval)** as an ordered ranking of AI systems by task performance, created by sampling model outputs and scoring them against criteria (15:34).  
    - Building evals involves selecting representative samples of task data, collecting model responses, and ranking outputs by quality.  
    - Manual human evals are costly and suffer from poor interrater agreement, limiting accuracy especially for closely matched models.  
    - Rohit stressed the importance of defining the system under test clearly and tailoring evals to that system’s specific task context.  
    - The fintech founder expressed challenges around sampling diverse financial queries to cover broad user scenarios, highlighting domain-specific complexities in eval design.  
- To reduce costs and improve speed, the group discussed **auto evals** that use automated scoring methods, such as multiple-choice probability checks or model-based judges, which can run in minutes rather than days (21:21).  
    - Multiple-choice evals work well early in training but are limited by their closed answer set and lack of real-world task fidelity.  
    - Using large language models as judges to score outputs can reach human-level agreement but requires careful prompt design and fine-tuning on eval data.  
    - Despite cost savings, auto evals still face challenges with subjective criteria and hallucination detection.  
    - Rohit cautioned that judge models should not be repurposed as reward models during training to avoid feedback loop issues.  
### **Improving Evaluation Accuracy and Resolution**
- Fine-grained and context-specific evaluation rubrics enhance the precision of model scoring, especially when distinguishing between closely performing AI systems (29:18).
- Creating **rubrics or constitutions** that specify detailed criteria for judging responses helps models evaluate outputs more objectively and consistently (29:18).  
    - Rubrics enable partial credit for responses, helping identify when models partially succeed versus fully fail.  
    - They allow tailoring evaluation style to task needs, such as expecting bulleted lists or specific data points, increasing evaluation resolution.  
    - This approach reduces ambiguity and improves the ability to differentiate model performance on subtle aspects.  
    - Rohit noted this method helps bypass the fundamental subjectivity in defining “good” responses by focusing on measurable elements.  
- The team discussed the limits of relying on consensus among models to detect hallucination, noting that model agreement does not guarantee correctness and may reinforce shared errors (33:36).  
    - Rohit recommended fine-tuning judge models on the specific eval set to improve hallucination detection accuracy without creating harmful feedback loops.  
    - He emphasized that eval models can be overfit to the eval data since they are not used in training, reducing risks of bias propagation.  
    - This precision tuning improves reliability in high-stakes scenarios without compromising broader model behavior.  
    - The group recognized hallucination evaluation as a creative, ongoing challenge requiring diverse question design and benchmarking approaches.  
### **Use Case–Driven Evaluation Design**
- Building effective evals requires tailoring to the unique demands and data characteristics of each use case, especially in high-stakes or sparse-data domains (39:18).
- A youth mental health company’s chatbot use case illustrated the challenge of evaluating rare but critical events like suicidality detection, where real incident data is sparse (39:18).  
    - Rohit advised creating synthetic data sets with adversarial examples to simulate rare failure cases and measure model robustness.  
    - Combining multiple reasoning threads is a known failure point for AI, so evals should include scenarios requiring such multi-faceted reasoning.  
    - This approach enables capturing error rates on important edge cases and guides agent improvements focused on risk mitigation.  
    - The team reinforced that synthetic adversarial evals are essential in low-incidence, high-impact applications to ensure safety and reliability.  
- Rohit proposed walking through a real use case during the session to demonstrate eval construction, stressing the importance of grounding evals in concrete, domain-specific tasks to maximize relevance (18:37).  
    - This hands-on design helps clarify sampling strategies, rubric creation, and judge model fine-tuning.  
    - It also surfaces domain-specific nuances that generic eval frameworks might miss.  
    - Engaging multiple stakeholders in brainstorming eval scenarios improves coverage and quality of test cases.  
    - This method supports continuous eval refinement as models and use cases evolve over time.  
### **Evaluation Process and Operational Considerations**
- The group acknowledged the complexity of evaluation workflows, emphasizing interrater alignment, cost efficiency, and integration with training pipelines (16:30).
- Misalignment among human evaluators remains a key challenge, requiring clear instructions, majority voting, and sometimes model-based adjudication to improve consistency (16:30).  
    - Human disagreement rates can be as low as 40-60%, complicating reliable model comparisons.  
    - Investing in training evaluators and standardizing criteria partially addresses this but increases cost.  
    - Use of LLM judges can partially offset human inconsistency but introduces new challenges in prompt design and bias control.  
    - The team recognized this as an ongoing trade-off between evaluation precision and practical feasibility.  
- Scaling human evals across many models or large data sets becomes prohibitively expensive, prompting focus on hybrid solutions that combine human judgment with automated approaches (20:00).  
    - Clustering model outputs to reduce pairwise comparisons and progressive elimination strategies were suggested to speed up evaluations of multiple models.  
    - Automated evals enable rapid iteration cycles, critical for agile development and deployment in competitive markets.  
    - The fintech founder’s concern about sampling coverage illustrates the need for domain expertise to guide eval sample design and ensure representativeness.  
    - Rohit emphasized that evaluation strategies must align with product risk profiles and business goals to prioritize resources effectively.  

## Action items

##### **Rohit**
- Facilitate discussion on building evals for selected use cases (18:37)
##### **Fintech startup founder**
- Gather and refine user questions reflecting broad financial personas to aid in sampling representative eval queries (17:06)
##### **AI evaluation teams**
- Work on improving interrater reliability by aligning human annotators and exploring better LLM prompt engineering for judgement consistency (17:30)
##### **AI researchers**
- Develop clustering-based hierarchical evaluation frameworks to scale human eval of large numbers of models efficiently (27:15)
##### **Model evaluators**
- Design and implement rubric-based evaluations with partial credit scoring for nuanced model performance assessment (30:44)
##### **Evaluation teams**
- Create adversarial datasets focused on hallucination scenarios to benchmark and improve agent reliability (36:30)
##### **Rohit and participants**
- Brainstorm documented sets of difficult, multi-threaded reasoning questions to test AI robustness (38:10)
##### **Youth mental health chatbot operator**
- Explore synthetic data creation to simulate low-frequency but critical mental health crisis events for reliable eval (39:18)

