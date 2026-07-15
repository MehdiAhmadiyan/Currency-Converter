# Currency Converter 💱

An elegant, real-time Currency Converter web application built with Python and [Streamlit](https://streamlit.io/). This application allows users to instantly convert amounts between 160+ currencies with a modern, responsive, and seamless graphical user interface.

To ensure high performance and minimize API overhead, the application implements an advanced **caching mechanism** to store exchange rate data locally.

## 🌟 Key Features

* **Modern Streamlit Web UI**: Built with a clean, interactive graphical interface. The conversion happens automatically in real-time as you type the amount or change currencies—no "Submit" button required.
* **Smart Performance Caching**: Powered by the `cachetools` library. It implements a Time-To-Live (TTL) cache (`TTLCache`) configured to retain exchange rates for **3 hours**. This drastically reduces redundant API calls to the ExchangeRate-API, speeds up response times, and saves bandwidth.
* **Visual Metric Widgets**: Displays the conversion results clearly using Streamlit's metric components, showing the base amount, a clean directional arrow, and the final converted value.
* **Modular Architecture**: Built following best practices with separate modules for configuration constants (`constants.py`), core utility logic (`currency_converter.py`), and the user interface (`app.py`).

## 📂 Project Structure

```text
Currency-Converter/
│
├── src/
│   ├── __init__.py             # Identifies src as a Python package
│   ├── constants.py            # Contains the list of supported fiat currencies
│   └── currency_converter.py   # Core conversion logic & TTLCache implementation
│
├── app.py                      # Streamlit web application interface
├── requirements.txt            # Project dependencies
├── LICENSE                     # MIT License
└── README.md                   # Project documentation
```

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MehdiAhmadiyan/Currency-Converter.git
   cd Currency-Converter
   ```

2. **Set up your API Key:**
   This project requires an API key from [ExchangeRate-API](https://www.exchangerate-api.com/). Once you get your key, set it as an environment variable:

   **On Linux/macOS:**
   ```bash
   export EXCHANGE_API_KEY="your_api_key_here"
   ```

   **On Windows (CMD):**
   ```cmd
   set EXCHANGE_API_KEY=your_api_key_here
   ```

   **On Windows (PowerShell):**
   ```powershell
   $env:EXCHANGE_API_KEY="your_api_key_here"
   ```

3. **Install the dependencies:**
   Ensure you have Python installed, then run:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the application:**
   Start the interactive Streamlit web server:
   ```bash
   streamlit run app.py
   ```

## 🛠️ Technologies Used
* **Python 3.x**
* **Streamlit**: For creating the interactive and modern web interface.
* **Requests**: For communicating with the ExchangeRate-API.
* **Cachetools**: For implementing the `TTLCache` mechanism to optimize API requests.

## 📜 License
This project is open-source and available under the terms of the MIT License.
