Transparent Health

A Flask web app for comparing healthcare costs across hospitals in India. The idea is simple: before you commit to a hospital for treatment, you should be able to see what it'll actually cost you compared to other options nearby.

What it does

- Search by disease and see cost, rating, severity, and insurance coverage across different hospitals
- Search by procedure (like an ultrasound or biopsy) and compare providers the same way
- Look up common medicines and compare prices across Apollo Pharmacy, Medplus, and PharmEasy
- Voice input option if you'd rather speak than type

Results are sorted so the better value options show up first, based on a simple cost to rating score.

Files in this repo

- app.py – the Flask app, all the routes and scoring logic live here
- sttts.py – a small standalone script for speech-to-text,text-to-speech
- hospital.json and procedure.json - the datasets the app reads from
- requirements.txt – Python packages needed
- index.html, diseases.html, text.html, medicine_price.html, amaan.html, about.html – the page templates
- style.css, index.css, index.js – styling and frontend behavior
- vercel.json – deployment config

Everything is currently kept flat in the root of the repo. If you want to actually run the app, Flask expects the HTML files inside a templates/HPT folder and the CSS/JS inside a static folder, so you'd need to move things around first.

Running it locally

git clone https://github.com/meghavarshinikuamreshan/Transparent-Health.git
cd Transparent-Health
pip install -r requirements.txt
python app.py

Then open http://127.0.0.1:5000 in your browser.

Routes

- / or /HPT – home page
- /HPT/text – disease cost comparison
- /HPT/text2 – procedure cost comparison
- /HPT/medp – medicine price comparison
- /HPT/voice – voice input page
- /HPT/about – about page

License

Not licensed yet.
