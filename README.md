# SMM Expert with AI

This project is a Python-based application that automates the work of an SMM specialist using artificial intelligence. The application helps in generating posts, images, scheduling publications, and retrieving statistics from social networks like VKontakte.

## Features
- **Post Generation**: Automatically generates text posts on given topics and in specified tones using the OpenAI API.
- **Image Generation**: Generates images based on the context of the post using the OpenAI API (DALL-E).
- **Auto-Publication**: Supports scheduling and automatic posting to VKontakte.
- **Statistics**: Retrieves and displays engagement statistics (views, likes, followers, etc.) from VKontakte.

## Technologies Used
- **Python**: Core programming language.
- **Flask**: Web framework for building the application's frontend.
- **OpenAI API**: Used for generating text and images.
- **VK API**: Used for publishing posts and retrieving statistics from VKontakte.
- **SQLAlchemy**: ORM for managing the database.
- **Bootstrap**: Used for styling the frontend.

## Project Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/username/smm-expert-ai.git
   cd smm-expert-ai
   ```

2. **Install dependencies:**
   It's recommended to use a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   Create a `.env` file and add your OpenAI and VKontakte API keys:
   ```bash
   OPENAI_API_KEY=<your_openai_api_key>
   VK_API_KEY=<your_vk_api_key>
   VK_GROUP_ID=<your_vk_group_id>
   ```

4. **Run the application:**
   ```bash
   flask run
   ```

## Key Modules
- `generators/text_gen.py`: Handles text generation using OpenAI.
- `generators/image_gen.py`: Handles image generation using OpenAI.
- `social_publishers/vk_publisher.py`: Manages interaction with VKontakte API for posting.
- `social_stats/vk_stats.py`: Retrieves and processes VKontakte statistics.

## Project Structure
```
smm-expert-ai/
│
├── app/
│   ├── __init__.py
│   ├── models.py
│   ├── auth.py
│   ├── smm.py
│   ├── templates/
│   └── static/
│
├── generators/
│   ├── text_gen.py
│   └── image_gen.py
├── social_publishers/
│   └── vk_publisher.py
├── social_stats/
│   └── vk_stats.py
├── config.py
├── requirements.txt
└── README.md
```

## How It Works

1. **Post Generation**: The user inputs a topic and tone, and the application generates a post using OpenAI's GPT model.
2. **Image Generation**: A description of the image is generated based on the post, and the image is created using the OpenAI image generation API.
3. **Publishing**: The post and image are automatically published to VKontakte.
4. **Statistics**: The app retrieves VK statistics (followers, likes, etc.) and displays them.

## License
This project is licensed under the MIT License.
