# AI STORY TELLER
## How to Run:

### On Google Colab:

1. **Launch Google Colab:** Start a Google Colab session, preferably using the free GPU runtime provided by Google.

2. **Run Notebook Cells:** Execute all cells in the notebook.

3. **Access Gradio Server:** After running the cells, a Gradio server URL will be generated in the output.

4. **Input Keywords:** Click on the generated URL and enter corresponding keywords to generate the desired story.

### Outside Google Colab:

1. **Install Necessary Libraries:**
   ```bash
   pip install openai==0.28 gradio diffusers invisible_watermark transformers accelerate safetensors
   ```
2. **Run Code Cell:** Execute the second code cell provided in the notebook.
3. **Access Gradio Server:** After running the code cell, a Gradio server URL will be generated in the output.
4. **Input Keywords:** Click on the generated URL and enter corresponding keywords to generate the desired story.


## Advantages of the project:
- Helps users create unique stories and images they may not have thought of before.
- The use of AI automates the creative and illustrative process, saving users time and effort.
- Enables everyone, regardless of writing skills, to create their own work.
- Applicable in various fields such as education, entertainment, marketing, etc.

## Disadvantages of the project:
- Due to AI models being used to create, stories and images may lack the user's creativity and personal touch.
- AI models may make mistakes in understanding user information or generate undesired results, and current evaluation models are not widely known or publicly available.
- The use of AI for artistic creation may lead to debates about copyright, ethics, and human impact.
- Using AI tools may require users to have a certain level of technical knowledge.

## Summary of the project's method:
1. **Gather information from users:**
   - A user interface (GUI) built with Gradio allows users to input details about the story they want to create, including story genre, main characters, setting, language, and story ending.
2. **Generate story titles and content:**
   - Utilize OpenAI's GPT-3.5 model to generate story text based on the information provided by users. Reuse the model to generate story titles based on the transmitted story.
3. **Generate illustrative images:**
   - Use the Diffusion Pipeline from StabilityAI to create images based on the summarized content of the story (expanded with details from Google's T5ForConditionalGeneration model).
4. **Deliver results:**
   - The interface will display the story title, illustrative image, and text content of the story. Users can download the story text as a .txt file.
