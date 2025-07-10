# 🏡 Zameen Web Scraper

This is a **Python-based web scraping tool** that collects real estate data from [Zameen.com](https://www.zameen.com), the most popular property website in Pakistan.  
It  extracts useful information like price, location, size, number of rooms, and agent details.  

The data is saved in a **CSV file**, which can be used for data analysis, visualization, or business insights.

---

## 📑 Table of Contents

- [📌 Objective](#-objective)
- [⚙️ How It Works](#-how-it-works)
- [🧰 Technologies Used](#-technologies-used)
- [🗃️ Data Fields Extracted](#-data-fields-extracted)
- [🚀 How to Use](#-how-to-use)
- [📂 Output File](#-output-file)
- [⚠️ Disclaimer](#️-disclaimer)
- [💬 Feedback](#-feedback)

---

## 📌 Objective

The main goal of this project is to:

- Automatically collect property listings from Zameen.com.
- Save details like **price, area, number of beds/baths, agent info**, and **posting date**.
- Convert relative dates like "2 days ago" into actual dates.
- Save all data into a **CSV file** for future use.

This scraper is helpful for:
- Real estate analysts
- Property investors
- Students working on data projects
- Business intelligence use cases

---

## ⚙️ How It Works

Here's what the script does, step-by-step:

1. **Opens Zameen.com listing pages** for flats in Peshawar using `Selenium` and ChromeDriver.
2. **Extracts property details** (title, price, location, beds, baths, area) from each listing.
3. For every group of 4 listings, it:
   - Opens each one in a **new tab** to get extra details:
     - **Agent Name**
     - **Posting Date** (converted to full date and time)
     - **Company Name**
4. **Closes all extra tabs** and goes back to the main listing page.
5. Saves all the data into a file called `zameen_data.csv`.

The script uses **waits and error handling** to avoid crashes if a listing is missing a detail.

---

## 🧰 Technologies Used

This scraper uses the following tools and libraries:

| Tool           | Purpose                                      |
|----------------|----------------------------------------------|
| Python         | Programming language                         |
| Selenium       | Automates browser for dynamic content        |
| BeautifulSoup  | Parses HTML content                         |
| ChromeDriver   | Controls the Chrome browser                  |
| CSV Module     | Saves the data to a CSV file                 |
| datetime       | Converts relative time (e.g. "3 days ago")   |

---

## 🗃️ Data Fields Extracted

Each row in the CSV contains the following columns:

| Field     | Description                                              |
|-----------|----------------------------------------------------------|
| Title     | Title of the property listing                            |
| Price     | Price of the flat or apartment                           |
| Location  | Area or neighborhood in Peshawar                         |
| Beds      | Number of bedrooms                                       |
| Area      | Size of the flat in square feet                          |
| Baths     | Number of bathrooms                                      |
| Agent     | Name of the real estate agent                            |
| Date      | Actual date and time the listing was posted              |
| Company   | Company or agency name of the agent                      |

---

## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/zaifi320/zameen-web-scraper.git
cd zameen-web-scraper
````

### 2. Install Required Libraries

Make sure you have Python installed (version 3.x). Then install the necessary libraries:

```bash
pip install selenium beautifulsoup4
```

### 3. Set Up ChromeDriver

* Download ChromeDriver from [https://chromedriver.chromium.org/](https://chromedriver.chromium.org/)
* Place the `.exe` file in a folder and update the `chrome_driver_path` in the script with the full path to that file.

### 4. Run the Script

```bash
python zameen_scraper.py
```

The script will open your Chrome browser and start collecting data.

---

## 📂 Output File

Once the script runs successfully, it will create a file named:

```
zameen_data.csv
```

This file contains all the extracted property data in tabular form.
You can open it with:

* Microsoft Excel
* Google Sheets
* Any data analysis tool (like Python, Pandas, Power BI)

This file is useful for:

* Sorting and filtering property listings
* Analyzing real estate prices and trends
* Comparing agent/company performance
* Building data-driven dashboards

---

## ⚠️ Disclaimer

* This project is developed **for learning, research, and academic purposes only**.
* Please **respect the terms and conditions** of [Zameen.com](https://www.zameen.com).
* Do **not use this scraper for bulk or commercial scraping** without permission.
* Always check Zameen’s [robots.txt](https://www.zameen.com/robots.txt) to see which pages are allowed for crawling.
* Web scraping can lead to IP bans if done excessively — use it responsibly and avoid high-frequency requests.

---

## 💬 Feedback

If you found this project helpful, please consider giving it a ⭐ on GitHub!

I welcome suggestions, improvements, or bug reports.
Feel free to:

* Open an issue
* Submit a pull request
* Share ideas to make this scraper better

Your feedback is appreciated! 😊

---

**Made with ❤️ by \Huzaifa Bin Saeed – For Real Estate Data Analysis in Pakistan**

```
