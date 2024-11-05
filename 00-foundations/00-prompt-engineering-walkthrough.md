# Prompt Engineering Walkthrough

Create a web design UI for an e-commerce website 

Chat Playground
The deployment you select at the top is the chat engine that will generate an answer for you. Gpt-4o is one of the latest models within the OpenAI family, which is able to process multimodal prompts and generate an answer accordingly.
The system message is a component of the prompt that is used to provide the model instructions about how it should behave and any relevant context. In this case, you are providing the model with the task it should perform and the safety guidelines it should follow.

System message:
## Task
You are a web copywriter for the Contoso Outdoor Company e-commerce website. Your goal is to generate the website copy for the homepage. 
Your answer should be brief and engaging. Always use a friendly and professional tone of voice.
Always show the word CONTOSO in capital letters.

## Safety
In the copy you write always stick to the subject of the company and the products it offers. Avoid any irrelevant information and controversial opinions.

Basic prompting:
Suggest a tagline for the website landing page of an e-commerce for outdoor clothing and equipment called Contoso Outdoor Company.

In a few seconds, you should get a short tagline suggestion. Note how the model uses the context and guidelines provided in the system message to generate a relevant answer.

Break down request:
Let's make it better. Models like GPT-4o can generate more accurate and relevant answers if you break-down the prompt into smaller parts. Clear chat and then try the following user prompt:

- Write a short welcome message for the homepage, specifying the company name and the main value proposition.
- Write a brief description of the business, including the categories of products offered.
- Write a short description for each of the following product categories: tents, backpacks, hiking clothing, sleeping bags.

By comparing the result with the previous one, we can notice a significant improvement in the quality of the generated text.

Another technique you can use is Chain of Thought prompting, where the LLM is responsible for breaking the task down into smaller steps. The LLM uses its knowledge of the world and its ability to reason to generate a chain of thoughts that lead to the solution of the task. Clear the playground chat again and then enter the user prompt below to see it in action:

Take a step-by-step approach in your response, include a welcome message, a brief description of the business, and a description of the product categories offered (tents, backpacks, hiking clothing, sleeping bags). Also, give reasoning before sharing the final answer in the below format: ANSWER is: <website copy>.

Few shot learning:
Let's go ahead and make the model generates a list of product names to add to the website copy. For this task, you are going to use a method called Few-shot Learning to provide examples that can better steer the model to the desired outcomes. Use the following user prompt:

Create a list of 10 product names the Contoso Outdoor shop might sell, include the type of item.

Examples:  
RidgeRunner Pro Trekking Poles: EQUIPMENT  
SummitShield 3-Season Tent: EQUIPMENT  
CascadeTech StormProof Jacket: APPAREL  
TerraFirm 40L Daypack: EQUIPMENT  
AlpineGlow Solar Lantern: EQUIPMENT

Multimodal prompting:
 We’ve seen a lot of examples for text input -> text output kind of scenarios. But prompt engineering is not just about text. 
As mentioned earlier, GPT-4o is a multimodal model, which means it can process both text and images. Let's see how it works with a combination of an image and a textual prompt.

Let’s change the system message to:
## Task
You are a web designer for the Contoso Outdoor Company e-commerce website. Your goal is to generate the website code snippets for the homepage GUI.

Then clear the chat and upload the image of the Contoso e-commerce hand-drown sketch (https://github.com/microsoft/aitour-concept-to-creation-ai-studio/blob/main/src/media/contoso_layout_sketch.jpg)
Couple the image with the following text prompt:
Generate the html and bootstrap code to implement the UI of the e-commerce landing page, based on the hand-drawn sketches in the image.
The outcome should provide a basic layout for the landing page of Contoso Outdoor Company. It includes placeholders for product descriptions.

If you want to see the website preview, open Visual Studio Code and copy paste the model answer into a new html file. 
