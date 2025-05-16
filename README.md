# 🍓 Melanie's Smoothies

**Melanie's Smoothies** is a web-based application that allows users to customize and order their favorite smoothies. Built using [Streamlit](https://streamlit.io/), this app provides an interactive interface to select ingredients, view nutritional information, and place orders.

## Features

* **Interactive Smoothie Builder**: Choose up to 5 fruits to create your custom smoothie.
* **Real-time Nutritional Information**: Fetches and displays nutritional data for selected fruits using the Fruityvice API.
* **Order Submission**: Submit your custom smoothie order with a personalized name.
* **Snowflake Integration**: Stores order details in a Snowflake database for backend processing.([GitHub][1])

## Getting Started

### Prerequisites

* Python 3.8 or higher
* [Anaconda](https://www.anaconda.com/products/distribution) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) (recommended for environment management)
* [Snowflake Account](https://signup.snowflake.com/) (for database integration)

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Chrisharris1001/melanies_smoothies.git
   cd melanies_smoothies
   ```



2. **Create and Activate the Conda Environment**

   ```bash
   conda create --name melanies_smoothies_env python=3.8
   conda activate melanies_smoothies_env
   ```



3. **Install Required Packages**

   ```bash
   pip install -r requirements.txt
   ```



4. **Configure Snowflake Connection**

   Ensure you have a `secrets.toml` file in the `.streamlit` directory with your Snowflake credentials:

   ```toml
   [connections.snowflake]
   user = "YOUR_USERNAME"
   password = "YOUR_PASSWORD"
   account = "YOUR_ACCOUNT"
   ```



5. **Run the Application**

   ```bash
   streamlit run streamlit_app.py
   ```



The application will launch in your default web browser.

## Project Structure

```plaintext
├── .devcontainer/
├── .streamlit/
│   └── secrets.toml
├── LICENSE
├── README.md
├── requirements.txt
└── streamlit_app.py
```



* `.devcontainer/`: Development container configuration files.
* `.streamlit/secrets.toml`: Contains Snowflake connection credentials.
* `streamlit_app.py`: Main application script.
* `requirements.txt`: Python dependencies.([cheat-sheet.streamlit.app][2], [Medium][3])

## Usage

1. **Enter Your Name**: Input the name to be associated with your smoothie order.
2. **Select Ingredients**: Choose up to 5 fruits from the provided list.
3. **View Nutritional Information**: For each selected fruit, nutritional data will be displayed.
4. **Submit Order**: Click the "Submit Order" button to place your order.([GitHub][1])

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Chrisharris1001/melanies_smoothies/blob/main/LICENSE) file for details.

## Acknowledgments

* Developed by [Chrisharris1001](https://github.com/Chrisharris1001).
* Utilizes the [Fruityvice API](https://www.fruityvice.com/) for nutritional information.
* Integrates with [Snowflake](https://www.snowflake.com/) for data storage.
