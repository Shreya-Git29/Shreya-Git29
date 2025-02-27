# Hi there, I'm Shreya Gautam! 👋  
import pygame
import time
import random

# Initialize pygame
pygame.init()

# Define window size
WIDTH = 600
HEIGHT = 400

# Colors
WHITE = (255, 255, 255)
GREEN = (0, 255, 0)
RED = (213, 50, 80)
BLACK = (0, 0, 0)

# Snake properties
SNAKE_BLOCK = 10
SNAKE_SPEED = 15

# Initialize game window
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Snake Game")

# Clock for controlling speed
clock = pygame.time.Clock()

# Font styles
font_style = pygame.font.SysFont("bahnschrift", 25)

def display_message(msg, color, x, y):
    text = font_style.render(msg, True, color)
    screen.blit(text, [x, y])

def game():
    game_over = False
    game_close = False

    x, y = WIDTH / 2, HEIGHT / 2
    dx, dy = 0, 0

    snake = []
    length = 1

    food_x = round(random.randrange(0, WIDTH - SNAKE_BLOCK) / 10.0) * 10.0
    food_y = round(random.randrange(0, HEIGHT - SNAKE_BLOCK) / 10.0) * 10.0

    while not game_over:
        while game_close:
            screen.fill(WHITE)
            display_message("Game Over! Press C to Play Again or Q to Quit", RED, WIDTH / 6, HEIGHT / 3)
            pygame.display.update()

            for event in pygame.event.get():
                if event.type == pygame.KEYDOWN:
                    if event.key == pygame.K_q:
                        game_over = True
                        game_close = False
                    if event.key == pygame.K_c:
                        game()

        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                game_over = True
            elif event.type == pygame.KEYDOWN:
                if event.key == pygame.K_LEFT:
                    dx = -SNAKE_BLOCK
                    dy = 0
                elif event.key == pygame.K_RIGHT:
                    dx = SNAKE_BLOCK
                    dy = 0
                elif event.key == pygame.K_UP:
                    dx = 0
                    dy = -SNAKE_BLOCK
                elif event.key == pygame.K_DOWN:
                    dx = 0
                    dy = SNAKE_BLOCK

        if x >= WIDTH or x < 0 or y >= HEIGHT or y < 0:
            game_close = True

        x += dx
        y += dy
        screen.fill(BLACK)
        pygame.draw.rect(screen, RED, [food_x, food_y, SNAKE_BLOCK, SNAKE_BLOCK])

        snake_head = []
        snake_head.append(x)
        snake_head.append(y)
        snake.append(snake_head)

        if len(snake) > length:
            del snake[0]

        for block in snake[:-1]:
            if block == snake_head:
                game_close = True

        for segment in snake:
            pygame.draw.rect(screen, GREEN, [segment[0], segment[1], SNAKE_BLOCK, SNAKE_BLOCK])

        pygame.display.update()

        if x == food_x and y == food_y:
            food_x = round(random.randrange(0, WIDTH - SNAKE_BLOCK) / 10.0) * 10.0
            food_y = round(random.randrange(0, HEIGHT - SNAKE_BLOCK) / 10.0) * 10.0
            length += 1

        clock.tick(SNAKE_SPEED)

    pygame.quit()
    quit()

# Run the game
game()


## 🚀 About Me  
 

### 🚀 AI/ML | Data Science | Software Development  

I'm a passionate **AI/ML Developer & Data Scientist** with expertise in building intelligent solutions for real-world problems. From **healthcare AI models** to **financial market analysis**, I love working on projects that make an impact.  

### 💡 What I Do  
🔹 **AI & ML Development** – Built models for **Breast Cancer Detection**, **Financial Sentiment Analysis**, and more.  
🔹 **Data Science & Analytics** – Experience in **EDA, ETL, and dashboard development** for business insights.  
🔹 **Software Development** – Developed applications using **Java, Python, React, and Flutter**.  
🔹 **Research & Innovation** – Published research on **Emotion-Driven Music Therapy App** and released a **patent**.  

### 🔥 Featured Projects  
🚑 **[Breast Cancer Detection](https://github.com/Shreya-Git29/breast-cancer-detection)** – AI model for early cancer detection (92% accuracy).  
🌿 **[Plant Iris Detection](https://github.com/Shreya-Git29)plant-iris-detection)** – Classifies Iris species using Decision Trees (95% accuracy).  
💰 **[Financial Market Sentiment Analysis](https://github.com/Shreya-Git29/financial-sentiment-analysis)** – Predicts market trends using ML & NLP.  

### 🛠️ Tech Stack  
💻 **Languages**: Python, Java, JavaScript, SQL  
📊 **ML & Data Science**: TensorFlow, Scikit-learn, Pandas, Seaborn  
🌍 **Web & App Dev**: React, Flutter, HTML/CSS  
🔍 **Tools**: Google Colab, Jupyter, Git, Docker  





---

### 🔹 Programming & Web Development  
![C++](https://img.shields.io/badge/-C++-000?&logo=C%2B%2B)  
![Python](https://img.shields.io/badge/-Python-000?&logo=Python)  
![JavaScript](https://img.shields.io/badge/-JavaScript-000?&logo=JavaScript)  
![C#](https://img.shields.io/badge/-C%23-000?&logo=Csharp)  
![PHP](https://img.shields.io/badge/-PHP-000?&logo=PHP)  
![SQL](https://img.shields.io/badge/-SQL-000?&logo=MySQL)  

### 🔹 Frontend & Backend  
![HTML5](https://img.shields.io/badge/-HTML5-000?&logo=HTML5)  
![CSS3](https://img.shields.io/badge/-CSS3-000?&logo=CSS3)  
![React](https://img.shields.io/badge/-React-000?&logo=React)  
![Node.js](https://img.shields.io/badge/-Node.js-000?&logo=Node.js)  
![Flask](https://img.shields.io/badge/-Flask-000?&logo=Flask)  
![FastAPI](https://img.shields.io/badge/-FastAPI-000?&logo=FastAPI)  

### 🔹 Databases & Cloud  
![MongoDB](https://img.shields.io/badge/-MongoDB-000?&logo=MongoDB)  
![Firebase](https://img.shields.io/badge/-Firebase-000?&logo=Firebase)  

### 🔹 Tools & Version Control  
![Git](https://img.shields.io/badge/-Git-000?&logo=Git)  
![GitHub](https://img.shields.io/badge/-GitHub-000?&logo=GitHub)  
![Microsoft 360](https://img.shields.io/badge/-Microsoft_Office-000?&logo=Microsoft-Office)  

### 🔹 Data Analytics & BI Tools  
![Power BI](https://img.shields.io/badge/-Power_BI-000?&logo=Power-BI)  
![Tableau](https://img.shields.io/badge/-Tableau-000?&logo=Tableau)  
![Excel](https://img.shields.io/badge/-Excel-000?&logo=Microsoft-Excel)  
  


---

## 🛠 Projects  


---

## 📊 GitHub Stats  
![Shreya's GitHub stats](https://github-readme-stats.vercel.app/api?username=Shreyagautam29&show_icons=true&theme=tokyonight)  
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Shreyagautam29&layout=compact&theme=tokyonight)  

---

## 📬 Connect With Me  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shreya-gautam-821216252/)  
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Shreya-Git29)  
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:gautamshreya04@gmail.com)  

✨ _Let's innovate and build something amazing together!_ 🚀  
