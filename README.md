# MyTone — Personal Color Analysis Web Application

MyTone is a web-based personal color analysis platform that helps users discover their seasonal color profile through image-based analysis. The system provides a modern interactive experience with personalized results, curated color palettes, fashion recommendations, and seasonal insights.

---

## Features

- Upload portrait image for analysis
- Image preview before submission
- Simulated loading progress during analysis
- Seasonal result generation:
  - Spring
  - Summer
  - Autumn
  - Winter
- Personalized color palettes
- Fashion recommendations
- Gender-specific styling pages
- Season detail pages
- Responsive modern interface
- Dynamic Flask routing

---

## Project Structure

```bash
project-name/
│
├── venv/
│
├── app.py #Route flask
│          #Bagian ('analyze')
│          #ganti predicted_season = "summer"  jadi
│          #predicted_season = predict_image(image)  
│          #predict_image itu nama variable hasil model  
│          
├── model/ #Nanti bikin folder model
│   ├── pipeline.py #Ini modelnya, sambungin ke app.py
│
├── data/
│   ├── __init__.py
│   └── analysis_results.py #Analysis Result Data
│
├── templates/
│   ├── layouts/
│   │   └── base.html #The base layout
│   │
│   ├── partials/
│   │   ├── navbar.html
│   │   └── footer.html
│   │
│   └── pages/ #Sesuai nama per halaman
│       ├── discover.html
│       ├── analysis.html
│       ├── result.html
│       ├── seasons.html
│       ├── autumn.html
│       ├── summer.html
│       ├── spring.html
│       ├── winter.html
│       ├── fashion.html
│       ├── gender.html
│       └── shop.html
│
├── static/
│   ├── css/
│   │
│   │   ├── pages/ #Sesuai nama
│   │   │   ├── analysis.css
│   │   │   ├── discover.css
│   │   │   ├── fashion.css
│   │   │   ├── gender.css
│   │   │   ├── result.css
│   │   │   ├── season-detail.css #Ini untuk 4 seasons yang autumn.html, etc
│   │   │   ├── seasons.css
│   │   │   └── shop.css
│   │
│   │   ├── components.css #Buat buttons, palette
│   │   ├── global.css #Layout web
│   │   ├── layout.css #Layout navbar ama web secara keseluruhan
│   │   ├── responsive.css #Biar gak aneh kalo zoom in zoom out
│   │   └── variables.css #Warna, font, sizes
│   │
│   ├── js/
│   │   ├── main.js
│   │   └── analysis.js #Buat ambil input gambar
│   │
│   └── images/
│
└── README.md
```

---

## Technologies Used

Frontend:

- HTML5
- CSS3
- JavaScript

Backend:

- Flask
- Jinja2 Template Engine

Programming Language:

- Python

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/mytone.git
```

Go into project folder:

```bash
cd mytone
```

Create virtual environment:

```bash
python -m venv venv
```

Activate virtual environment:

Windows:

```bash
venv\Scripts\activate
```

Mac/Linux:

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install flask
```

---

## Run Application

Run:

```bash
python app.py
```

or:

```bash
flask run
```

Open browser:

```bash
http://127.0.0.1:5000
```

---

## Application Flow

1. User visits Discover page

2. User navigates to Analysis page

3. Upload portrait image

4. System previews uploaded image

5. User starts analysis

6. Loading animation appears

7. User redirected to Result page

8. Personalized seasonal palette displayed

---

## Current Analysis Data

Current version uses predefined seasonal datasets inside:

```bash
data/analysis_results.py
```

Future implementation can replace this with:

- CNN image classification
- Skin tone extraction
- Face detection
- AI color recommendation model
- Real machine learning prediction pipeline

---

## Future Improvements

- Deep Learning integration
- Facial landmark detection
- Automatic skin undertone extraction
- User authentication
- Save analysis history
- Database integration
- Outfit recommendation engine
- E-commerce integration
- Dark mode

---

## Contributors

Developed for Human Computer Interaction (HCI) Project.

Members:

- Your Name
- Team Member
- Team Member

---

## License

This project is for educational purposes only.