# Sports Podcast Notebook

This project provides a set of Jupyter notebooks and supporting scripts for generating engaging sports podcast scripts using AI. The workflow is designed for experimentation and rapid prototyping, with a focus on leveraging Visual Studio Code (VS Code) as the primary IDE.

## Project Overview

The notebooks guide you through:
- Extracting key sports data from raw sources (CSV, PDFs, web pages)
- Structuring and analyzing sports topics
- Generating lively podcast dialogue using large language models (LLMs)
- Saving and exporting podcast scripts for production

The main example is a Kansas City Chiefs recap, but the workflow is adaptable to other teams and sports.

## Prerequisites

- **Python 3.9+**
- **Visual Studio Code** (with the Python and Jupyter extensions)
- **pip** for package management

### Required Python Packages

- `jupyter`
- `pydantic`
- `python-dotenv`
- `openai` (or Azure OpenAI SDK if using Azure)
- Any other dependencies listed in your `requirements.txt`

## Setup Instructions

1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/sports-podcast-notebook.git
   cd sports-podcast-notebook
   ```

2. **Create and Activate a Virtual Environment**
   ```sh
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```sh
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**
   - Copy `.env.example` to `.env` and fill in your API keys and endpoints:
     ```
     AZURE_OPENAI_ENDPOINT=your_endpoint
     AZURE_OPENAI_MODEL=your_model
     AZURE_OPENAI_REASONING_MODEL=your_reasoning_model
     ```
   - If using OpenAI directly, set the relevant keys.

5. **Prepare Example Data**
   - Place your source files (e.g., `playerstats.csv`, game recaps) in the `examples/` directory.
   - Update notebook paths if you use different filenames.

## Using the Notebooks in Visual Studio Code

1. **Open the Project Folder in VS Code**
   - Launch VS Code and open the project directory.

2. **Install VS Code Extensions**
   - **Python**: For Python language support.
   - **Jupyter**: For running and editing notebooks.

3. **Open the Notebook**
   - Navigate to `notebook/gen_2_dialog.ipynb` and open it.
   - VS Code will display the notebook interface, allowing you to run cells interactively.

4. **Run the Notebook**
   - Start from the top cell and run each cell sequentially.
   - Modify parameters, prompts, or input files as needed for experimentation.

5. **Experimentation Tips**
   - You can edit prompts and model parameters directly in the notebook.
   - Use the VS Code variable explorer and interactive plots for debugging and analysis.
   - Save outputs (e.g., generated scripts) to JSON or text files for further use.

## Customization

- **Change Team or Sport**: Update the system prompt and input data to focus on different teams or sports.
- **Extend Models**: Modify the Pydantic models in the notebook to capture additional podcast features.
- **Integrate with Azure**: If using Azure OpenAI, ensure your credentials and endpoints are set in `.env`.

## Troubleshooting

- If you encounter import errors, ensure your virtual environment is activated.
- For API errors, double-check your `.env` configuration.
- If notebook cells hang, restart the Jupyter kernel in VS Code.

## Contributing

Pull requests and suggestions are welcome! Please open issues for bugs or feature requests.

## License

MIT License. See `LICENSE` for details.

## Acknowledgements

- OpenAI / Azure OpenAI for LLM APIs
- Visual Studio Code for notebook development
