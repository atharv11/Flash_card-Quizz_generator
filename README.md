# AI-Powered Learning Assistant for Exam Preparation

 # Frontend & Backend
The system combines a modern ReactJS front end with a robust Django backend to ensure efficiency, scalability, and accessibility. TailwindCSS provides a responsive, mobile-friendly UI, while Context API handles state management. Key features include PDF uploads, adaptive quizzes, and performance tracking.

The backend, built with Django and DRF, uses a modular architecture. It integrates an LLM to process uploaded text and generate quizzes, stores data in PostgreSQL, tracks user responses, and provides personalized performance summaries.
![image](https://github.com/user-attachments/assets/7b7758da-2aad-4218-854b-596f3d6e7116)
![image](https://github.com/user-attachments/assets/d7757355-fc1e-4672-af62-c1d27e3b27d4)
![image](https://github.com/user-attachments/assets/fee6986e-5bd9-48a9-a2ef-d984fa092c2d)
![image](https://github.com/user-attachments/assets/c49c6314-4033-4309-bf7c-85f371d1e3d7)
![image](https://github.com/user-attachments/assets/565ae6c3-a919-419c-a2d9-b8bcbe2059f3)
![image](https://github.com/user-attachments/assets/e00d67e0-6632-48e5-a122-9ff4e51f1453)







 # LLM: 
DiscoLM_German_7B_v1 serves as the foundational largelanguage
model (LLM) driving advanced question and flashcard generation in
the German language. Designed specifically for educational and research purposes,
DiscoLM_German_7B_v1 excels in creating coherent, contextually relevant
educational materials. This model has been meticulously trained on largescale
German text corpora, including academic articles, educational resources,
and linguistic databases, ensuring a profound understanding of German language
structure, nuances, and context.

# Genetic Algorithm: 
   We implemented an adaptive genetic algorithm
to select a sequence of quiz questions that cater to the user’s learning progress.
The algorithm maintains a population of candidate quizzes, each represented by
a list of questions. The fitness of a candidate quiz is evaluated based on two
factors:
1. The user’s performance on the topic covered by each question, and
2. The diversity of topics within the quiz.
3. The amount of time the user spends on a particular question.
To encourage the exploration of various topics, we penalize quizzes with
repeated topics. The genetic algorithm employs crossover and mutation operators
to generate new candidate quizzes in each iteration. Selection is performed using
a tournament selection strategy, where better-performing quizzes are more likely
to be selected for reproduction. This iterative process ensures that the algorithm
converges towards a quiz sequence that is both challenging and informative for
the user, considering their past performance and topic coverage.

# Model Experiments
To ensure the system’s ability to generate contextually appropriate educational
content, three primary language models were tested. The goal was to evaluate
these models based on their architecture, training data, and ability to generate
high-quality educational material for German learners.
1. DiscoResearch/DiscoLM_German_7b_v1
– Pre-trained on German-specific corpora, this model is highly proficient
in understanding the nuances of the language.
– Tailored for instruction-following tasks, making it ideal for generating
structured educational content.
– Demonstrated a balance between computational efficiency and highquality
output, producing contextually accurate quizzes and flashcards[1].
2. DiscoResearch/Llama3-German-8B-32k
– A larger model with 8 billion parameters and a context window of 32,000
tokens, suitable for processing extensive and complex German texts.
– Despite its superior performance on large-scale tasks, its higher computational
requirements made it less efficient for this project, which involves
shorter, focused tasks[2].
3. mistralai/Mistral-7B-Instruct-v0.3
– Optimized for general-purpose instruction-following across multiple languages.
– While it performed well in multilingual tasks, it lacked the specialized
focus on German-specific nuances that DiscoLM_German_7b_v1
offered[3].
DiscoLM_German_7b_v1 was chosen for its specialization in the German
language and its ability to handle instructional tasks efficiently. This model
provided the best balance between computational feasibility and the generation
of high-quality, German-focused content.

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
