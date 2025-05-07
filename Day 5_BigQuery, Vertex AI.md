## 🧠 Vertex AI:-

## 🔵1. What is Vertex AI?

Vertex AI is a tool from Google Cloud that helps you build, train, and use machine learning models — all in one place. It’s easier to use than the old AI Platform and has more features like model monitoring and automated workflows.

## 🔵2. What’s the difference between AutoML and custom models?

AutoML: You upload your data, and Google does most of the work (training, tuning).

Custom models: You write your own code for more control (using Python, TensorFlow, etc.).

## 🔵3. How do you deploy a model in Vertex AI?

Train a model (AutoML or custom).

Go to the Models section.

Click Deploy.

Choose where to deploy (an endpoint).

Once deployed, you can send data and get predictions.

❓4. What is the Feature Store?
Answer:
Feature Store is like a database for machine learning inputs (features). It helps reuse features, keeps training and prediction data the same, and avoids mistakes like data leakage.

❓5. How does Vertex AI detect if a model is getting worse over time?
Answer:
It uses Model Monitoring to watch for:

Data drift: When new data looks very different from training data.

Prediction problems: If outputs are off, it can alert you.

❓6. What are Pipelines in Vertex AI?
Answer:
Pipelines are like recipes. They describe each ML step (get data → train → test → deploy) so the whole process runs automatically. This is good for MLOps (machine learning + operations).

❓7. How do you train a big model with your own code?
Answer:

Put your code in a Docker container (a kind of app box).

Use CustomContainerTrainingJob.

Pick machine size (with GPU if needed).

Vertex AI runs your code for you on powerful cloud machines.

❓8. What is a model registry?
Answer:
It’s a place to store and manage all your models. You can:

Keep track of different versions

Share with your team

Deploy models safely

❓9. How is Vertex AI different from AWS SageMaker or Azure ML?
Answer:
All are cloud ML platforms. Vertex AI is:

Very good for AutoML and big workflows

Tightly linked with other Google Cloud services

Uses tools like Kubeflow and BigQuery smoothly

❓10. How do you do MLOps in Vertex AI?
Answer:

Build a pipeline (like a flowchart).

Run it when new data comes in.

Store models in the registry.

Use tools like Cloud Build for automation.

Monitor models to keep them accurate over time.
