 Just follow these steps:

    Paste Your Content: Start by pasting your text or markdown into the provided area. This is the core content that the AI will use to build your slides.

    Add Optional Guidance: Give the AI a hint about the tone or purpose of your presentation (e.g., "make it a research summary" or "investor pitch").

    Plug in Your API Key: GyaanSetu uses large language models (LLMs) to understand and structure your content. You'll need to provide your API key for a supported provider like OpenAI, Anthropic, or Gemini.

    Use a Template (Optional): Want a specific look? Upload a .pptx or .potx template file. The AI will intelligently map your new content onto the template's existing styles, layouts, fonts, and even images to maintain brand consistency.

    Generate and Download: Click the "Generate" button. The system will handle the rest, and you can download your perfectly formatted, ready-to-use PowerPoint deck in seconds.

The frontend also includes handy features like toasts for notifications, real-time progress feedback, and a history of your past generations.

Frontend

This user interface is a responsive web page built with HTML and styled with Tailwind CSS for a clean, modern look.
It handles all user interactions, from accepting your text and template uploads to managing the file download. 
It also provides a seamless user experience with toasts for quick notifications, progress indicators to show the status of your generation, and a local history log of all the presentations you've created.

Backend

The backend is an API built with FastAPI, designed for speed and efficiency. It serves as the intelligent engine behind the app:

    Input Processing: It receives your content, guidance, API key, and template file.

    Intelligent Splitting: The backend uses the chosen LLM to analyze your text, intelligently dividing it into logical sections suitable for individual slides.

    Template Mapping: It leverages the python-pptx library to programmatically insert the new, structured content into your uploaded template. This process ensures that the final deck inherits all of your template's styling, from fonts to color schemes.

    File Generation: The final, styled .pptx file is then generated and sent back to the frontend for you to download.
