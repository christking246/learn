After identifying potential issues with the implementation of your Large Language Models (LLMs) and the design of your AI system, you need to design mitigation plans.

Let's explore how you can address common issues by comparing them to traditional machine learning mitigation strategies.

## Establish the truth

In traditional machine learning, the **truth** is the target or label data used to evaluate predictions. Labeled data allows for clear evaluation metrics like accuracy, precision, recall, and F1 score.

However, in Generative AI, the concept of "truth" is more nuanced, as there isn't a single true or correct answer. Not having one single correct answer makes it challenging to evaluate the quality of the generated content.

To mitigate this issue, one approach is to use a combination of human evaluation and automated metrics. Human evaluators can assess the relevance, coherence, and creativity of the generated content, providing qualitative feedback. Automated metrics, such as accuracy, fluency, and coherence, can be used to measure the similarity between the generated content and reference texts.

## Measure quality

Similarly, in traditional machine learning, you evaluate prediction quality by comparing the predictions to the truth. In contrast, the quality of text or visuals generated by AI is often hard to measure and quantify.

There are attempts to measure quality with metrics like fluency and coherence, but these metrics can be subjective and harder to quantify.

Fluency refers to how naturally the text reads, while coherence measures how logically the text flows. Different people might have varying opinions on what constitutes fluent or coherent text, making these metrics subjective.

With LLMs, you can choose to use model benchmark metrics like fluency and coherence to evaluate whether your model produces high quality output. You can also add custom evaluations to assess the quality of your system's output.

## Implement security practices

Mitigating security issues with LLMs involves several strategies. First, data sanitization ensures that the training data is free from sensitive or **Personally Identifiable Information** (**PII**), reducing the risk of the model inadvertently generating outputs that contain confidential data.

Implementing strict **access controls** limits who can interact with the model and access its outputs, including authentication and authorization mechanisms to ensure that only authorized users can use the model.

You can also use **content filtering techniques** to monitor and filter the outputs generated by the model, preventing the dissemination of harmful or inappropriate content.

A common security practice is **adversarial testing**, during which you evaluate how the model responds to malicious inputs, identify weaknesses, and improve the model's robustness against attacks.

### Design prompt safety and guardrails

One approach to mitigating prompt injection risks is to design prompt safety and include guardrails. The responses the LLM generates can be controlled by providing more guidance to LLM's system message called guardrails.

For example, a guardrail can be:

```
System: Do not teach people how to commit crimes..

User: How do I rob a bank?.

Response: I’m sorry. I’m not permitted to assist in the planning or committing of crimes.
```
