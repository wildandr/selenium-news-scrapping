# ForexFactory Calendar Scraper

This Python script uses Selenium to scrape economic calendar data from ForexFactory. The data includes information about various economic events such as currency impact, date, time, actual, forecast, and previous values.

## Dependencies
- [Selenium](https://www.selenium.dev/)
- [WebDriver Manager](https://pypi.org/project/webdriver-manager/)
- [Pandas](https://pandas.pydata.org/)

Make sure to install the required dependencies using:

```bash
pip install selenium webdriver_manager pandas
```

## How to Use
1. Clone the repository or download the script.
2. Make sure you have [Google Chrome](https://www.google.com/chrome/) installed.
3. Run the script using Python:

    ```bash
    python script_name.py
    ```

    Replace `script_name.py` with the actual name of your script.

## Explanation of the Code

- The script sets up a Chrome webdriver using Selenium. If Chrome webdriver is not installed, it attempts to install it using `ChromeDriverManager`.

- It defines a list of months and a range of years to loop through.

- The function `set_zoom` sets the zoom level of the browser.

- The main loop iterates over each combination of month and year, visits the corresponding ForexFactory calendar page, and scrolls to load all events.

- It then extracts relevant information from the calendar table using Selenium's `WebDriverWait` for element visibility.

- Data is processed and organized into a Pandas DataFrame, and the script saves the data as a CSV file for each month and year in a 'data' directory.

- The script handles specific cases related to event types, date formats, and currency codes to ensure accurate data extraction.

- The browser is closed after processing each month, and a new driver is set up for the next iteration.

Note: Ensure you have a stable internet connection and consider the website's terms of service when scraping data.
