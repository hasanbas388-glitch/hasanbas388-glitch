![Header](github-header.png)

<img width="1500" height="500" alt="github-header png" src="https://github.com/user-attachments/assets/272ca46c-675a-402d-9896-60f82fa631e8" />


**hasanbas388-glitch/hasanbas388-glitch** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

👤 About Me

Aspiring Data Analyst focused on retail analytics, financial trends, and operational insights using Python, SQL, and Excel. I enjoy turning raw data into clear business decisions through analysis, visualization, and storytelling.

I am also interested in:

Data storytelling
Language systems
Structured thinking through data

🧰 Skills & Tools

Programming & Data Analysis
Python (Pandas, NumPy, Matplotlib)
SQL (basic querying, aggregations, joins)
Excel (Pivot Tables, dashboards, data cleaning)

 Data Visualization & Reporting
Data storytelling and insights communication
Trend analysis and KPI reporting
Basic dashboard creation (Excel / Python plots)

Analytics Concepts
KPI analysis (CTR, CPC, Conversion Rate, ROAS)
Financial trend analysis
Business performance analysis
Retail and operational analytics

🛠 Tools
Google Colab
Jupyter Notebook
Microsoft Excel
GitHub
Python libraries for data analysis

 Soft Skills
Analytical thinking
Attention to detail
Structured problem solving
Clear written communication



📁 Featured Projects

S&P 500 Market Trend & Volatility Study

Analyzed historical S&P 500 data (1990–2025) using Python and Excel to identify long-term market trends and volatility behavior.

Key insights:

Confirmed long-term upward growth trend in the S&P 500
Identified high-volatility periods during economic downturns
Observed cyclical behavior in market corrections
 Basketball Performance Analytics Dashboard

Analyzed basketball player and team performance data using visualization techniques to identify trends across seasons.

Key insights:

Compared player efficiency across multiple seasons
Identified performance consistency patterns
Visualized scoring and win-rate trends
 Healthcare Workforce Efficiency Analysis (Excel Pivot Tables)

Built dashboards using pivot tables to analyze healthcare workforce distribution and operational efficiency.

Key insights:

Identified staffing distribution across departments
Compared workload and efficiency metrics
Summarized large datasets into actionable reports
 Digital Advertising Campaign Performance Analysis

Built a simulated digital marketing analytics system to evaluate campaign performance using KPIs such as CTR, CPC, Conversion Rate, and ROAS.

Key insights:

Campaign performance varied significantly across channels
High CTR did not always lead to high conversions, highlighting funnel inefficiencies
Certain campaigns delivered strong ROAS, indicating efficient ad spend
Social and video channels generally outperformed display ads in engagement
Cost efficiency varied widely across campaigns, suggesting targeting inconsistencies

🔭 Currently Working On
Improving Python for data analysis
Learning SQL more deeply
Building retail-focused analytics projects
Developing stronger data storytelling skills

🌱 Currently Learning
Python for Data Science
SQL for Analytics
Turkish & Spanish language basics

## Veiw Projects
[Healthcare_Data_PivotChart1.xlsx](https://github.com/user-attachments/files/28230106/Healthcare_Data_PivotChart1.xlsx)

[retail_sales_inventory_analysis.ipynb](https://github.com/user-attachments/files/28276307/retail_sales_inventory_analysis.ipynb)

[nba_predictor_model.ipynb](https://github.com/user-attachments/files/28276302/nba_predictor_model.ipynb)

[S&P 500 Trend Analysis (1990-2025).xlsx](https://github.com/user-attachments/files/28230553/S.P.500.Trend.Analysis.1990-2025.xlsx)

[digital_ad_campaign_performance_tracker.ipynb](https://github.com/user-attachments/files/28276699/digital_ad_campaign_performance_tracker.ipynb)


- {
  "cells": [{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "code",
      "execution_count": 3,
      "metadata": {
        "id": "ovJAb1ZM4oOb"
      },
      "outputs": [],
      "source": [
        "import pandas as pd\n",
        "import numpy as np\n",
        "import matplotlib.pyplot as plt"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "np.random.seed(42)\n",
        "\n",
        "data = {\n",
        "    \"Product\": np.random.choice(\n",
        "        [\"Electronics\", \"Apparels\", \"Groceries\", \"Furniture\"],\n",
        "        200\n",
        "    ),\n",
        "\n",
        "    \"Region\": np.random.choice(\n",
        "        [\"North\", \"South\", \"East\", \"West\"],\n",
        "        200\n",
        "    ),\n",
        "\n",
        "    \"Sales\": np.random.randint(100, 10000, 200),\n",
        "\n",
        "    \"Inventory\": np.random.randint(10, 1000, 200),\n",
        "\n",
        "    \"Month\": np.random.choice(\n",
        "        [\"Jan\", \"Feb\", \"Mar\", \"Apr\", \"May\", \"Jun\"],\n",
        "        200\n",
        "    )\n",
        "}\n",
        "\n",
        "df = pd.DataFrame(data)\n",
        "\n",
        "df.head()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 215
        },
        "id": "xW9ejIgD7h23",
        "outputId": "84328c21-9e9a-4658-c168-8707007de7c5"
      },
      "execution_count": 4,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "       Product Region  Sales  Inventory Month\n",
              "0    Groceries   East   1748        917   Jan\n",
              "1    Furniture   West   5639        699   Mar\n",
              "2  Electronics   East   9737        684   May\n",
              "3    Groceries  North   4299        389   Apr\n",
              "4    Groceries   West   8545        554   Jun"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-f8b75804-1589-4a1b-b72e-26f237a70f28\" class=\"colab-df-container\">\n",
              "    <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Product</th>\n",
              "      <th>Region</th>\n",
              "      <th>Sales</th>\n",
              "      <th>Inventory</th>\n",
              "      <th>Month</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Groceries</td>\n",
              "      <td>East</td>\n",
              "      <td>1748</td>\n",
              "      <td>917</td>\n",
              "      <td>Jan</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>Furniture</td>\n",
              "      <td>West</td>\n",
              "      <td>5639</td>\n",
              "      <td>699</td>\n",
              "      <td>Mar</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>Electronics</td>\n",
              "      <td>East</td>\n",
              "      <td>9737</td>\n",
              "      <td>684</td>\n",
              "      <td>May</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Groceries</td>\n",
              "      <td>North</td>\n",
              "      <td>4299</td>\n",
              "      <td>389</td>\n",
              "      <td>Apr</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>Groceries</td>\n",
              "      <td>West</td>\n",
              "      <td>8545</td>\n",
              "      <td>554</td>\n",
              "      <td>Jun</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>\n",
              "    <div class=\"colab-df-buttons\">\n",
              "\n",
              "  <div class=\"colab-df-container\">\n",
              "    <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-f8b75804-1589-4a1b-b72e-26f237a70f28')\"\n",
              "            title=\"Convert this dataframe to an interactive table.\"\n",
              "            style=\"display:none;\">\n",
              "\n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\">\n",
              "    <path d=\"M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z\"/>\n",
              "  </svg>\n",
              "    </button>\n",
              "\n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    .colab-df-buttons div {\n",
              "      margin-bottom: 4px;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "    <script>\n",
              "      const buttonEl =\n",
              "        document.querySelector('#df-f8b75804-1589-4a1b-b72e-26f237a70f28 button.colab-df-convert');\n",
              "      buttonEl.style.display =\n",
              "        google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "      async function convertToInteractive(key) {\n",
              "        const element = document.querySelector('#df-f8b75804-1589-4a1b-b72e-26f237a70f28');\n",
              "        const dataTable =\n",
              "          await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                    [key], {});\n",
              "        if (!dataTable) return;\n",
              "\n",
              "        const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "          '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "          + ' to learn more about interactive tables.';\n",
              "        element.innerHTML = '';\n",
              "        dataTable['output_type'] = 'display_data';\n",
              "        await google.colab.output.renderOutput(dataTable, element);\n",
              "        const docLink = document.createElement('div');\n",
              "        docLink.innerHTML = docLinkHtml;\n",
              "        element.appendChild(docLink);\n",
              "      }\n",
              "    </script>\n",
              "  </div>\n",
              "\n",
              "\n",
              "    </div>\n",
              "  </div>\n"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "dataframe",
              "variable_name": "df",
              "summary": "{\n  \"name\": \"df\",\n  \"rows\": 200,\n  \"fields\": [\n    {\n      \"column\": \"Product\",\n      \"properties\": {\n        \"dtype\": \"category\",\n        \"num_unique_values\": 4,\n        \"samples\": [\n          \"Furniture\",\n          \"Apparels\",\n          \"Groceries\"\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"Region\",\n      \"properties\": {\n        \"dtype\": \"category\",\n        \"num_unique_values\": 4,\n        \"samples\": [\n          \"West\",\n          \"South\",\n          \"East\"\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"Sales\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 2847,\n        \"min\": 104,\n        \"max\": 9974,\n        \"num_unique_values\": 197,\n        \"samples\": [\n          4852,\n          3869,\n          7044\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"Inventory\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 283,\n        \"min\": 18,\n        \"max\": 987,\n        \"num_unique_values\": 185,\n        \"samples\": [\n          406,\n          510,\n          666\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"Month\",\n      \"properties\": {\n        \"dtype\": \"category\",\n        \"num_unique_values\": 6,\n        \"samples\": [\n          \"Jan\",\n          \"Mar\",\n          \"Feb\"\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    }\n  ]\n}"
            }
          },
          "metadata": {},
          "execution_count": 4
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "product_sales = df.groupby(\"Product\")[\"Sales\"].sum()\n",
        "print(product_sales)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "6rbYARXg-pej",
        "outputId": "e23c1221-f279-4b02-a73a-70ecc06f0c91"
      },
      "execution_count": 5,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Product\n",
            "Apparels       258176\n",
            "Electronics    209876\n",
            "Furniture      255220\n",
            "Groceries      279238\n",
            "Name: Sales, dtype: int64\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "region_inventory = df.groupby(\"Region\")[\"Inventory\"].mean()\n",
        "print(region_inventory)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "gZ99LPMi_NpK",
        "outputId": "53b565e2-1340-46e4-a565-939a80a1a204"
      },
      "execution_count": 6,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Region\n",
            "East     505.820000\n",
            "North    532.775510\n",
            "South    403.900000\n",
            "West     516.803279\n",
            "Name: Inventory, dtype: float64\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "product_sales.plot(kind=\"bar\")\n",
        "\n",
        "plt.title(\"Total Sales by Product Category\")\n",
        "\n",
        "plt.ylabel(\"Sales\")\n",
        "\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 533
        },
        "id": "Fdh6g4oE_nO0",
        "outputId": "593a814b-0dda-47d4-831f-73f2f22ae4e7"
      },
      "execution_count": 7,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 640x480 with 1 Axes>"
            ],
            "image/png": "iVBORw0KGgoAAAANSUhEUgAAAlUAAAIECAYAAAAw1NvgAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjAsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvlHJYcgAAAAlwSFlzAAAPYQAAD2EBqD+naQAAVBdJREFUeJzt3XlcFfX+x/E3oCwugBsgiaK5i0suIZVbkqiUWlpppmiat65LSmlSXtdS81630vR3s1xKy2wxVxRxKyXLBdewNNcUd0BRWef3hw/mesQFbfAgvJ6Px3no+c73zHzOmYO8nfnOdxwMwzAEAACAv8XR3gUAAADkB4QqAAAACxCqAAAALECoAgAAsAChCgAAwAKEKgAAAAsQqgAAACxAqAIAALAAoQoAAMAChCogn1i/fr0cHBy0fv36+77t5s2bq3nz5vd1mw4ODurXr9993aY9+Pv7q0ePHvYuA0AOEKqAv8HBwSFHj5wEnbFjx2rx4sW5XrMk7d69W506dVKFChXk6uqqhx56SE899ZQ++uij+7L9B0VWUM16FC5cWJUqVVL37t31559/2rs8SyxYsEBTpky5q9dkZGRo9uzZat68uUqWLCkXFxf5+/urZ8+e2rp1613XsG/fPo0cOVKHDx++69cCeUkhexcAPMg+//xzm+fz5s1TVFRUtvYaNWrccV1jx45Vp06d1KFDBytLzGbz5s1q0aKFypcvr1dffVU+Pj46duyYfv75Z02dOlX9+/fP1e0/iAYMGKBGjRopLS1N27dv13//+18tX75cu3fvlq+vr73L+1sWLFigPXv2aODAgTnqf+XKFT333HOKjIxU06ZN9c4776hkyZI6fPiwvv76a82dO1dHjx5VuXLlclzDvn37NGrUKDVv3lz+/v739kaAPIBQBfwNL7/8ss3zn3/+WVFRUdna85L3339fHh4e+vXXX+Xp6Wmz7PTp0/YpKo9r0qSJOnXqJEnq2bOnqlatqgEDBmju3LmKiIi46WuSk5NVtGjR+1nmfTF48GBFRkZq8uTJ2YLYiBEjNHnyZPsUdh9kZmYqNTVVrq6u9i4FeRSn/4BclpycrDfffFN+fn5ycXFRtWrV9J///EeGYZh9HBwclJycrLlz55qnmrLG0Rw5ckT//Oc/Va1aNbm5ualUqVJ6/vnn7/lUycGDB1WrVq1sgUqSvLy8bJ7Pnj1bTz75pLy8vOTi4qKaNWtqxowZOdpOSkqKRowYocqVK8vFxUV+fn4aMmSIUlJSbPpFRUXpiSeekKenp4oVK6Zq1arpnXfeyfH7mT9/vqpVqyZXV1c1aNBAGzduNJetW7dODg4O+v7777O9bsGCBXJwcFBMTEyOt5XlySeflCQdOnRIkjRy5Eg5ODho3759eumll1SiRAk98cQTkqT09HSNGTNGDz/8sHma7J133sn2ORiGoffee0/lypVTkSJF1KJFC+3duzfbtrO2daM5c+bIwcEh2/di5cqVatasmYoXLy53d3c1atRICxYskHRtLNzy5ct15MgR83t3uyNFx48f1//93//pqaeeuumRLScnJ7311lvmUaqcfHfnzJmj559/XpLUokWLm54yX7lypZo0aaKiRYuqePHiCg0Nvelns2jRItWsWVOurq4KCAjQ999/rx49emR7Tzn5mZT+N25v/vz5qlWrllxcXLRy5Ur5+/urffv22bZ/9epVeXh46B//+MctP0PkbxypAnKRYRhq166d1q1bp169eqlevXpatWqVBg8erL/++sv8X/3nn3+u3r1769FHH1WfPn0kSQ8//LAk6ddff9XmzZvVuXNnlStXTocPH9aMGTPUvHlz7du3T0WKFLmrmipUqKCYmBjt2bNHAQEBt+07Y8YM1apVS+3atVOhQoW0dOlS/fOf/1RmZqb69u17y9dlZmaqXbt2+umnn9SnTx/VqFFDu3fv1uTJk/X777+bY8f27t2rp59+WnXq1NHo0aPl4uKiAwcOaNOmTTl6Lxs2bNDChQs1YMAAubi46OOPP1br1q31yy+/KCAgQM2bN5efn5/mz5+vZ5991ua18+fP18MPP6ygoKAcbet6Bw8elCSVKlXKpv35559XlSpVNHbsWPMXdO/evTV37lx16tRJb775prZs2aJx48bpt99+swl7w4cP13vvvae2bduqbdu22r59u1q1aqXU1NS7ri/LnDlz9Morr6hWrVqKiIiQp6enduzYocjISL300kt69913lZiYqOPHj5vfxWLFit1yfStXrlR6erq6deuWo+3n5LvbtGlTDRgwQB9++KHeeecd81R51p+ff/65wsLCFBISog8++ECXL1/WjBkz9MQTT2jHjh1mYFq+fLlefPFF1a5dW+PGjdOFCxfUq1cvPfTQQzY15fRnMsva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c+NVeqdOnZK7u7vc3Nzk5OQkJyenm/a5fh13quVGLi4ucnFxuYtPAgAAPKjseqTKMAz169dP33//vdauXauKFSvaLG/QoIEKFy6s6Ohos23//v06evSogoKCJElBQUHavXu3zVV6UVFRcnd3V82aNc0+168jq0/WOpydndWgQQObPpmZmYqOjjb75KQWAABQcNn1SFXfvn21YMEC/fDDDypevLg5NsnDw0Nubm7y8PBQr169FB4erpIlS8rd3V39+/dXUFCQebVdq1atVLNmTXXr1k0TJkxQfHy8hg0bpr59+5pHiV577TVNmzZNQ4YM0SuvvKK1a9fq66+/1vLl/7t6Ijw8XGFhYWrYsKEeffRRTZkyRcnJyerZs6dZ051qAQAABZddQ9WMGTMkSc2bN7dpnz17tnr06CFJmjx5shwdHdWxY0elpKQoJCREH3/8sdnXyclJy5Yt0+uvv66goCAVLVpUYWFhGj16tNmnYsWKWr58uQYNGqSpU6eqXLlymjVrlkJCQsw+L774os6cOaPhw4crPj5e9erVU2RkpM3g9TvVAgAACq48NU9Vfsc8VfbBPDYFC/u7YGF/FyzMUwUAAFAAEKoAAAAsQKgCAACwAKEKAADAAoQqAAAACxCqAAAALECoAgAAsAChCgAAwAKEKgAAAAsQqgAAACxAqAIAALAAoQoAAMAChCoAAAALEKoAAAAsQKgCAACwAKEKAADAAoQqAAAACxCqAAAALECoAgAAsAChCgAAwAKEKgAAAAsQqgAAACxAqAIAALAAoQoAAMAChCoAAAALEKoAAAAsQKgCAACwAKEKAADAAoQqAAAACxCqAAAALECoAgAAsAChCgAAwAKEKgAAAAsQqgAAACxAqAIAALAAoQoAAMAChCoAAAALEKoAAAAsQKgCAACwAKEKAADAAoQqAAAACxCqAAAALECoAgAAsAChCgAAwAKEKgAAAAtYEqoyMjIUGxurCxcuWLE6AACAB849haqBAwfq008/lXQtUDVr1kz169eXn5+f1q9fb2V9AAAAD4R7ClXffPON6tatK0launSpDh06pLi4OA0aNEjvvvuupQUCAAA8CO4pVJ09e1Y+Pj6SpBUrVuj5559X1apV9corr2j37t2WFggAAPAguKdQ5e3trX379ikjI0ORkZF66qmnJEmXL1+Wk5OTpQUCAAA8CArd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bW/s74KF/V2wsL/ts13DMG7bj1CVQ2fPnlVGRoa8vb1t2r29vRUXF3fT14wbN06jRo3K1u7n55crNeLmPKbYuwLcT+zvgoX9XbDYe39fvHhRHh4et1xOqMpFERERCg8PN59nZmbq/PnzKlWqlBwcHOxY2f2VlJQkPz8/HTt2TO7u7vYuB7mM/V2wsL8LloK6vw3D0MWLF+Xr63vbfoSqHCpdurScnJx06tQpm/ZTp07Jx8fnpq9xcXGRi4uLTZunp2dulZjnubu7F6gfwoKO/V2wsL8LloK4v293hCoLA9VzyNnZWQ0aNFB0dLTZlpmZqejoaAUFBdmxMgAAkBdwpOouhIeHKywsTA0bNtSjjz6qKVOmKDk5WT179rR3aQAAwM4IVXfhxRdf1JkzZzR8+HDFx8erXr16ioyMzDZ4HbZcXFw0YsSIbKdCkT+xvwsW9nfBwv6+PQfjTtcHAgAA4I4YUwUAAGABQhUAAIAFCFUAAAAWIFQBAABYgFAFAABgAUIVAACABQhVyHUZGRmKjY3VhQsX7F0KAOAuXblyRZcvXzafHzlyRFOmTNHq1avtWFXeRKiC5QYOHKhPP/1U0rVA1axZM9WvX19+fn5av369fYtDrpg7d66WL19uPh8yZIg8PT312GOP6ciRI3asDLnl4MGDGjZsmLp06aLTp09LklauXKm9e/fauTJYrX379po3b54kKSEhQYGBgZo4caLat2+vGTNm2Lm6vIVQBct98803qlu3riRp6dKlOnTokOLi4jRo0CC9++67dq4OuWHs2LFyc3OTJMXExGj69OmaMGGCSpcurUGDBtm5Olhtw4YNql27trZs2aLvvvtOly5dkiTt3LlTI0aMsHN1sNr27dvVpEkTSdf+fff29taRI0c0b948ffjhh3auLm8hVMFyZ8+elY+PjyRpxYoVev7551W1alW98sor2r17t52rQ244duyYKleuLElavHixOnbsqD59+mjcuHH68ccf7VwdrDZ06FC99957ioqKkrOzs9n+5JNP6ueff7ZjZcgNly9fVvHixSVJq1ev1nPPPSdHR0c1btyYI9E3IFTBct7e3tq3b58yMjIUGRmpp556StK1H0wnJyc7V4fcUKxYMZ07d07StX90s/a5q6urrly5Ys/SkAt2796tZ599Nlu7l5eXzp49a4eKkJsqV66sxYsX69ix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JGn37t168skn5ebmplKlSqlPnz66dOmSub6MjAyFh4fL09NTpUqV0pAhQ7LdVNrf319TpkyxaatXr55GjhxpPk9ISNA//vEPeXt7y9XVVQEBAVq2bJnWr1+vnj17KjEx0TzKdv3rAOQthCoABZabm5tSU1MlSdHR0dq/f7+ioqK0bNkyJScnKyQkRCVKlNCvv/6qRYsWac2aNerXr5/5+okTJ2rOnDn67LPP9NNPP+n8+fP6/vvv76qGzMxMtWnTRps2bdIXX3yhffv2afz48XJyctJjjz2mKVOmyN3dXSdPntTJkyf11ltvWfoZALAOp/8AFDiGYSg6OlqrVq1S//79debMGRUtWlSzZs0yT/t98sknunr1qubNm2fey3DatGl65pln9MEHH8jb21tTpkxRRESEnnvuOUnSzJkztWrVqruqZc2aNfrll1/022+/qWrVqpKkSpUqmcs9PDzk4OAgHx8fK946gFzEkSoABcayZctUrFgxubq6qk2bNnrxxRfN02m1a9e2GUf122+/qW7dumagkqTHH39cmZmZ2r9/vxITE3Xy5EkFBgaaywsVKqSGDRveVU2xsbEqV66cGagAPLg4UgWgwGjRooVmzJghZ2dn+fr6qlCh//0TeH14spKjo2O2cVZpaWnm393c3HJluwDuP45UASgwihYtqsqVK6t8+fI2gepmatSooZ07dyo5Odls27RpkxwdHVWtWjV5eHiobNmy2rJli7k8PT1d27Zts1lPmTJldPLkSfN5UlKSDh06ZD6vU6eOjh8/rt9///2mdTg7OysjI+Ou3icA+yBUAcBNdO3aVa6urgoLC9OePXu0bt069e/fX926dZO3t7ck6Y033tD48eO1ePFixcXF6Z///KcSEhJs1vPkk0/q888/148//qjdu3crLCxMTk5O5vJmzZqpadOm6tixo6KionTo0CGtXLlSkZGRkq5dPXjp0iVFR0fr7Nmzunz58n37DADcHUIVANxEkSJFtGrVKp0/f16NGjVSp06d1LJlS02bNs3s8+abb6pbt24KCwtTUFCQihcvrmeffdZmPREREWrWrJmefvpphYaGqkOHDnr44Ydt+nz77bdq1KiRunTpopo1a2rIkCHm0anHHntMr732ml588UWVKVNGEyZMyP03D+CeOBg3nuwHAADAXeNIFQAAgAUIVQAAABYgVAEAAFiAUAUAAGABQhUAAIAFCFUAAAAWIFQBAABYgFAFAABgAUIVAACABQhVAAAAFiBUAQAAWOD/ASYNviVN/jIJAAAAAElFTkSuQmCC\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "monthly_sales = df.groupby(\"Month\")[\"Sales\"].sum()\n",
        "\n",
        "monthly_sales.plot(kind=\"line\", marker=\"o\")\n",
        "\n",
        "plt.title(\"Monthly Sales Trends\")\n",
        "\n",
        "plt.ylabel(\"Sales\")\n",
        "\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 472
        },
        "id": "IPLgos7aAL3O",
        "outputId": "65144c59-40f0-4d39-b6e8-4f0b3f68d17b"
      },
      "execution_count": 8,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 640x480 with 1 Axes>"
            ],
            "image/png": "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JiZWGt+uXTu0a9cO06dPx759+9CjRw988cUXeO+998ySD1Ft461AogbOyckJn3/+OWbNmoWBAwfeNu7hhx+GXq/HokWLTNZ//PHHUCgUGDBgQLXf29g3qTae+ho2bBgUCgUmTJiA8+fP3/FpQKOCggLExcVVus04hsx4C8t4tebWqzMHDhy47f5GKpUKjz/+OH777TccP368wvbr169Lf/7n049qtRqhoaEQQlTaTuJePfbYY1CpVJg9e3aFq05CiDs+jXk7Dz/8MK5du4Zff/1VWldQUIAvv/zSJC4nJwdlZWUm69q1awelUllpawYiS8UrVkR021tStxo4cCD69euHt956CxcuXECHDh3wxx9/4Pfff8fEiRNNBplXVZcuXQCUdwsfOnQobG1tMXDgQLM0qvTy8kJUVBRWrFgBV1dXREdH33WfgoIC3H///ejevTuioqIQEBCA7OxsrF69Grt370ZMTAw6deoEAHjkkUewcuVKDB48GNHR0UhOTsYXX3yB0NBQ5OXl3fF9PvjgA2zfvh1hYWF4/vnnERoaiszMTBw+fBhbtmyRWj30798fvr6+6NGjB3x8fHDq1CksWrQI0dHRFca6mUPz5s3x3nvvYdq0abhw4QJiYmLg7OyM5ORkrFq1Ci+88AL+7//+r1rHfP7557Fo0SKMGDEC8fHx8PPzww8//AAHBweTuG3btmH8+PF48skn0bJlS5SVleGHH36QClEia8HCioiqRKlUYs2aNZgxYwaWL1+OJUuWoEmTJpg3bx5ef/31Gh3zvvvuw7vvvosvvvgCGzduhMFgQHJystk6gI8YMQKxsbEYMmRIlabocXV1xVdffYV169ZhyZIlSE1NhUqlQqtWrTBv3jyTJyJHjRqF1NRU/Pe//8WmTZsQGhqKH3/8EStWrLjrxMI+Pj44ePAg3nnnHaxcuRKfffYZPDw80KZNG3z44YdS3L/+9S/873//w0cffYS8vDw0btwYr776KqZPn17jc3I3b7zxBlq2bImPP/5YGscVEBCA/v3749FHH6328RwcHLB161a88sor+PTTT+Hg4IDhw4djwIABJtMDdejQAZGRkVi7di2uXr0KBwcHdOjQARs2bED37t3N9vmIaptC1HSUIRGRhfv9998RExODXbt2oVevXnKnQ0QNAAsrIqq3HnnkEZw6dQpJSUm1OlCeiMiItwKJqN75+eefcfToUaxbtw6ffPIJiyoiqjO8YkVE9Y5CoYCTkxOeeuopfPHFF7Cx4e+QRFQ3+NOGiOod/r5IRHJhHysiIiIiM2FhRURERGQmvBVYhwwGA65duwZnZ2cOpiUiIrISQgjk5ubC398fSuWdr0mxsKpD165dQ0BAgNxpEBERUQ1cvnz5rhOCs7CqQ8YpKC5fvgwXFxeZsyEiIqKqyMnJQUBAQJWmkmJhVYeMt/9cXFxYWBEREVmZqgzj4eB1IiIiIjNhYUVERERkJiysiIiIiMyEhRURERGRmbCwIiIiIjITFlZEREREZsLCioiIiMhMWFgRERERmQkLKyIiIiIzYed1IiIismp6g8DB5Eyk5xbB29kO3Zq6Q6W8e5f02sDCioiIiKzWxuMpmL32JFJ0RdI6P60dZg4MRVRbvzrPh7cCiYiIyCptPJ6Cl348bFJUAUCqrggv/XgYG4+n1HlOLKyIiIjI6ugNArPXnoSoZJtx3ey1J6E3VBZRe1hYERERkdU5mJxZ4UrVrQSAFF0RDiZn1l1SYGFFREREVig99/ZFVU3izIWFFREREVkdb2c7s8aZCwsrIiIisjrdmrrDT2uH2zVVUKD86cBuTd3rMi0WVkRERGR9VEoFZg4MrXSbsdiaOTC0zvtZsbAiIiIiqxTV1g+fP9MZNv8onny1dvj8mc6y9LFig1AiIiKyWp0C3VB2s6XCvwe3RVNPJ1k7r8t6xWrOnDm477774OzsDG9vb8TExCAxMdEkpqioCOPGjYOHhwecnJzw+OOPIy0tzSTm0qVLiI6OhoODA7y9vTF58mSUlZWZxOzYsQOdO3eGRqNBcHAwli5dWiGfxYsXo0mTJrCzs0NYWBgOHjxY7VyIiIio7uw5ewMA0L6xFk+HBSG8uYdsRRUgc2G1c+dOjBs3Dvv378fmzZtRWlqK/v37Iz8/X4p57bXXsHbtWqxYsQI7d+7EtWvX8Nhjj0nb9Xo9oqOjUVJSgn379uG7777D0qVLMWPGDCkmOTkZ0dHR6NevHxISEjBx4kQ899xz2LRpkxSzfPlyTJo0CTNnzsThw4fRoUMHREZGIj09vcq5EBERUd3am1ReWPUI9pQ5k5uEBUlPTxcAxM6dO4UQQmRnZwtbW1uxYsUKKebUqVMCgIiLixNCCLF+/XqhVCpFamqqFPP5558LFxcXUVxcLIQQYsqUKaJNmzYm7/XUU0+JyMhIablbt25i3Lhx0rJerxf+/v5izpw5Vc7lbnQ6nQAgdDpdleKJiIjo9gwGg7jvvc0iaGqs2Hv2eq29T3W+vy1q8LpOpwMAuLuXPxoZHx+P0tJSRERESDEhISEIDAxEXFwcACAuLg7t2rWDj4+PFBMZGYmcnBycOHFCirn1GMYY4zFKSkoQHx9vEqNUKhERESHFVCUXIiIiqjtn0vKQnlsMO1slOge5yZ0OAAsavG4wGDBx4kT06NEDbdu2BQCkpqZCrVbD1dXVJNbHxwepqalSzK1FlXG7cdudYnJyclBYWIisrCzo9fpKY06fPl3lXP6puLgYxcXF0nJOTs7dTgMRERFV0Z6btwHva+IOO1uVzNmUs5grVuPGjcPx48fx888/y52K2cyZMwdarVZ6BQQEyJ0SERFRvbHn7HUAQK8WFjK+ChZSWI0fPx6xsbHYvn07GjduLK339fVFSUkJsrOzTeLT0tLg6+srxfzzyTzj8t1iXFxcYG9vD09PT6hUqkpjbj3G3XL5p2nTpkGn00mvy5cvV+FsEBER0d2UlBlw4OYEyz2DvWTO5m+yFlZCCIwfPx6rVq3Ctm3b0LRpU5PtXbp0ga2tLbZu3SqtS0xMxKVLlxAeHg4ACA8Px7Fjx0ye3tu8eTNcXFwQGhoqxdx6DGOM8RhqtRpdunQxiTEYDNi6dasUU5Vc/kmj0cDFxcXkRURERPfu8KUsFJTo4emkRoivs9zpSGQdYzVu3DgsW7YMv//+O5ydnaWxSlqtFvb29tBqtRg7diwmTZoEd3d3uLi44JVXXkF4eDi6d+8OAOjfvz9CQ0Px7LPPYu7cuUhNTcX06dMxbtw4aDQaAMCLL76IRYsWYcqUKRgzZgy2bduGX375BevWrZNymTRpEkaOHImuXbuiW7duWLBgAfLz8zF69Ggpp7vlQkRERHXD2Gbh/uaeUMrYt6qCWns2sQoAVPpasmSJFFNYWChefvll4ebmJhwcHMTgwYNFSkqKyXEuXLggBgwYIOzt7YWnp6d4/fXXRWlpqUnM9u3bRceOHYVarRbNmjUzeQ+jTz/9VAQGBgq1Wi26desm9u/fb7K9KrncCdstEBERmcegRXtE0NRYsfzQpVp/r+p8fyuEEEK+sq5hycnJgVarhU6n421BIiKiGtIVlKLTu3/AIIB9bzwAf1f7Wn2/6nx/W8TgdSIiIqKqijufAYMAmnk51npRVV0srIiIiMiq7Em62WbBUqaxuQULKyIiIrIqxomXe7awnDYLRiysiIiIyGpczizAhYwCqJQKdG/mLnc6FbCwIiIiIqthbLPQMcAVzna2MmdTEQsrIiIishq7bxZWPS1wfBXAwoqIiIishMEgsO9mYWVJ8wPeioUVERERWYWTKTnIKiiFk8YGHQJc5U6nUiysiIiIyCrsvvk0YPdm7rBVWWYJY5lZEREREf2DsX+VpY6vAlhYERERkRUoKtXj0IUsAJbZv8qIhRURERFZvEMXMlFSZoCvix2aeznKnc5tsbAiIiIii/d3t3VPKBQKmbO5PRZWREREZPGMA9cttc2CEQsrIiIismgZecU4mZIDALi/OQsrIiIiohrbey4DABDi6wwvZ43M2dwZCysiIiKyaHvOlrdZsPTbgAALKyIiIrJgQohbBq5bbpsFIxZWREREZLGSb+Tjmq4IapUS3Zq4y53OXbGwIiIiIou15+aky12C3GCvVsmczd2xsCIiIiKLtfuW/lXWgIUVERERWaQyvQH7bz4RaMnzA96KhRURERFZpCNXdMgtLoPW3hZtG2nlTqdKWFgRERGRRTI+Ddgj2AMqpeVOY3MrFlZERERkkfYmGQsr67gNCLCwIiIiIguUV1yGw5eyAAC9gi2/f5URCysiIiKyOAfOZ6DMIBDo7oBADwe506kyFlZERERkcaytzYIRCysiIiKyOMbxVdbSZsGIhRURERFZlFRdEc6m50GhAO5v7iF3OtXCwoqIiIgsinEam/aNtHB1UMucTfWwsCIiIiKLYo1tFoxYWBEREZHFEEJIV6ysbeA6wMKKiIiILEhiWi6u5xbD3laFLkFucqdTbSysiIiIyGIYp7Hp1tQdGhuVzNlUHwsrIiIishh7rLTNghELKyIiIrIIxWV6HDifCcA6x1cBLKyIiIjIQhy+mI3CUj08ndQI8XWWO50akbWw2rVrFwYOHAh/f38oFAqsXr3aZHtaWhpGjRoFf39/ODg4ICoqCmfPnjWJKSoqwrhx4+Dh4QEnJyc8/vjjSEtLM4m5dOkSoqOj4eDgAG9vb0yePBllZWUmMTt27EDnzp2h0WgQHByMpUuXVsh38eLFaNKkCezs7BAWFoaDBw+a5TwQERGRaZsFhUIhczY1I2thlZ+fjw4dOmDx4sUVtgkhEBMTg/Pnz+P333/HX3/9haCgIERERCA/P1+Ke+2117B27VqsWLECO3fuxLVr1/DYY49J2/V6PaKjo1FSUoJ9+/bhu+++w9KlSzFjxgwpJjk5GdHR0ejXrx8SEhIwceJEPPfcc9i0aZMUs3z5ckyaNAkzZ87E4cOH0aFDB0RGRiI9Pb2Wzg4REVHDstvKx1cBAISFACBWrVolLScmJgoA4vjx49I6vV4vvLy8xFdffSWEECI7O1vY2tqKFStWSDGnTp0SAERcXJwQQoj169cLpVIpUlNTpZjPP/9cuLi4iOLiYiGEEFOmTBFt2rQxyeepp54SkZGR0nK3bt3EuHHjTHLx9/cXc+bMqfJn1Ol0AoDQ6XRV3oeIiKghyM4vEU3fiBVBU2NFSnah3OmYqM73t8WOsSouLgYA2NnZSeuUSiU0Gg327NkDAIiPj0dpaSkiIiKkmJCQEAQGBiIuLg4AEBcXh3bt2sHHx0eKiYyMRE5ODk6cOCHF3HoMY4zxGCUlJYiPjzeJUSqViIiIkGJu9xlycnJMXkRERFRR3PkbMAgg2NsJvlq7u+9goSy2sDIWSNOmTUNWVhZKSkrw4Ycf4sqVK0hJSQEApKamQq1Ww9XV1WRfHx8fpKamSjG3FlXG7cZtd4rJyclBYWEhbty4Ab1eX2mM8RiVmTNnDrRarfQKCAio/okgIiJqAHafrQe3AWHBhZWtrS1WrlyJM2fOwN3dHQ4ODti+fTsGDBgApdJi0zYxbdo06HQ66XX58mW5UyIiIrJI1t6/yshG7gTupEuXLkhISIBOp0NJSQm8vLwQFhaGrl27AgB8fX1RUlKC7Oxsk6tWaWlp8PX1lWL++fSe8anBW2P++SRhWloaXFxcYG9vD5VKBZVKVWmM8RiV0Wg00Gg0NfvwREREDcTlzAJczCiASqlA9+YecqdzT6zi0o9Wq4WXlxfOnj2LP//8E4MGDQJQXnjZ2tpi69atUmxiYiIuXbqE8PBwAEB4eDiOHTtm8vTe5s2b4eLigtDQUCnm1mMYY4zHUKvV6NKli0mMwWDA1q1bpRgiIiKqGePVqk4BrnDSWPQ1n7uSNfu8vDwkJSVJy8nJyUhISIC7uzsCAwOxYsUKeHl5ITAwEMeOHcOECRMQExOD/v37AygvuMaOHYtJkybB3d0dLi4ueOWVVxAeHo7u3bsDAPr374/Q0FA8++yzmDt3LlJTUzF9+nSMGzdOupr04osvYtGiRZgyZQrGjBmDbdu24ZdffsG6deuk3CZNmoSRI0eia9eu6NatGxYsWID8/HyMHj26Ds8YERFR/WOcH9Bau62bqIOnFG9r+/btAkCF18iRI4UQQnzyySeicePGwtbWVgQGBorp06dLLRKMCgsLxcsvvyzc3NyEg4ODGDx4sEhJSTGJuXDhghgwYICwt7cXnp6e4vXXXxelpaUVcunYsaNQq9WiWbNmYsmSJRXy/fTTT0VgYKBQq9WiW7duYv/+/dX6vGy3QEREZKpMbxAdZm8SQVNjxZ8XMuROp1LV+f5WCCGEjHVdg5KTkwOtVgudTgcXFxe50yEiIpLdsSs6DFy0B04aGyTMeAg2KssbpVSd72/Ly56IiIgajN1J1wEA3Zt5WGRRVV3W/wmIiIjIahnHV/WqD+OrwMKKiIiIZFJYosefF7IA1JOB62BhRURERDI5dCETJXoD/LR2aObpKHc6ZsHCioiIiGRxa7d1hUIhczbmwcKKiIiIZLG7PvWvuomFFREREdW5G3nFOJWSAwDoYeXzA96KhRURERHVub03bwO29nOBp1P9mVeXhRURERHVufrWZsGIhRURERHVKSGEdMWqZz26DQiwsCIiIqI6dv5GPq7piqBWKXFfE3e50zErFlZERERUp4y3Abs2cYO9WiVzNubFwoqIiIjqVH1ss2DEwoqIiIjqTJnegP3nMwAAvYK9ZM7G/FhYERERUZ05ciUbecVlcHWwRai/i9zpmB0LKyIiIqozxtuAPZp7QqWsH9PY3IqFFREREdUZqc1CPRxfBbCwIiIiojqSV1yGvy5lA6h//auMWFgRERFRndh/LgNlBoEgDwcEuDvInU6tYGFFREREdWJPPe22fisWVkRERFQnjIVVfZsf8FYsrIiIiKjWpegKkZSeB6UCCG/GwoqIiIioxozT2LRr7Aqtg63M2dQeFlZERERU64xtFnrV4/FVAAsrIiIiqmVCCOxJKp/GpgcLKyIiIqKaO52aixt5xbC3VaFzkKvc6dQqFlZERERUq4zjq8KauUNjo5I5m9rFwoqIiIhqVUPoX2XEwoqIiIhqTXGZHgeSy8dX1df5AW/FwoqIiIhqTfzFLBSVGuDlrEErH2e506l1LKyIiIio1uy95TagQqGQOZvax8KKiIiIao1x4Hp9b7NgxMKKiIiIakV2QQmOXtUBaBgD1wEWVkRERFRL4s5lQAighbcTfLV2cqdTJ1hYERERUa3YndSwbgMCLKyIiIiolhjHV/VqAG0WjFhYERERkdldyijApcwC2CgVCGvmIXc6dYaFFREREZmdsdt650A3OGlsZM6m7shaWO3atQsDBw6Ev78/FAoFVq9ebbI9Ly8P48ePR+PGjWFvb4/Q0FB88cUXJjFFRUUYN24cPDw84OTkhMcffxxpaWkmMZcuXUJ0dDQcHBzg7e2NyZMno6yszCRmx44d6Ny5MzQaDYKDg7F06dIK+S5evBhNmjSBnZ0dwsLCcPDgQbOcByIiovpmT9J1AA1rfBUgc2GVn5+PDh06YPHixZVunzRpEjZu3Igff/wRp06dwsSJEzF+/HisWbNGinnttdewdu1arFixAjt37sS1a9fw2GOPSdv1ej2io6NRUlKCffv24bvvvsPSpUsxY8YMKSY5ORnR0dHo168fEhISMHHiRDz33HPYtGmTFLN8+XJMmjQJM2fOxOHDh9GhQwdERkYiPT29Fs4MERGR9dIbBPYmNZxpbEwICwFArFq1ymRdmzZtxDvvvGOyrnPnzuKtt94SQgiRnZ0tbG1txYoVK6Ttp06dEgBEXFycEEKI9evXC6VSKVJTU6WYzz//XLi4uIji4mIhhBBTpkwRbdq0MXmfp556SkRGRkrL3bp1E+PGjZOW9Xq98Pf3F3PmzKnyZ9TpdAKA0Ol0Vd6HiIjI2hy5nCWCpsaKtjM2itIyvdzp3LPqfH9b9Bir+++/H2vWrMHVq1chhMD27dtx5swZ9O/fHwAQHx+P0tJSRERESPuEhIQgMDAQcXFxAIC4uDi0a9cOPj4+UkxkZCRycnJw4sQJKebWYxhjjMcoKSlBfHy8SYxSqURERIQUU5ni4mLk5OSYvIiIiOq73TefBuze3AM2KosuNczOoj/tp59+itDQUDRu3BhqtRpRUVFYvHgxevfuDQBITU2FWq2Gq6uryX4+Pj5ITU2VYm4tqozbjdvuFJOTk4PCwkLcuHEDer2+0hjjMSozZ84caLVa6RUQEFD9k0BERGRlGmKbBSOLL6z279+PNWvWID4+HvPnz8e4ceOwZcsWuVOrkmnTpkGn00mvy5cvy50SERFRrSos0SP+YhaAhjONza0s9vnHwsJCvPnmm1i1ahWio6MBAO3bt0dCQgL+85//ICIiAr6+vigpKUF2drbJVau0tDT4+voCAHx9fSs8vWd8avDWmH8+SZiWlgYXFxfY29tDpVJBpVJVGmM8RmU0Gg00Gk3NTgAREZEVOnghEyV6Axq52qOpp6Pc6dQ5i71iVVpaitLSUiiVpimqVCoYDAYAQJcuXWBra4utW7dK2xMTE3Hp0iWEh4cDAMLDw3Hs2DGTp/c2b94MFxcXhIaGSjG3HsMYYzyGWq1Gly5dTGIMBgO2bt0qxRARERGw56yxzYIHFAqFzNnUPVmvWOXl5SEpKUlaTk5ORkJCAtzd3REYGIg+ffpg8uTJsLe3R1BQEHbu3Invv/8eH330EQBAq9Vi7NixmDRpEtzd3eHi4oJXXnkF4eHh6N69OwCgf//+CA0NxbPPPou5c+ciNTUV06dPx7hx46SrSS+++CIWLVqEKVOmYMyYMdi2bRt++eUXrFu3Tspt0qRJGDlyJLp27Ypu3bphwYIFyM/Px+jRo+vwjBEREVk248D1ni28ZM5EJrX/kOLtbd++XQCo8Bo5cqQQQoiUlBQxatQo4e/vL+zs7ESrVq3E/PnzhcFgkI5RWFgoXn75ZeHm5iYcHBzE4MGDRUpKisn7XLhwQQwYMEDY29sLT09P8frrr4vS0tIKuXTs2FGo1WrRrFkzsWTJkgr5fvrppyIwMFCo1WrRrVs3sX///mp9XrZbICKi+iw9p0gETY0VQVNjxY3cIrnTMZvqfH8rhBBCxrquQcnJyYFWq4VOp4OLi4vc6RAREZnV7wlXMeHnBIT6uWD9hF5yp2M21fn+ttgxVkRERGRddjfgNgtGLKyIiIjongkhpP5VDW4am1tYbLsFIkujNwgcTM5Eem4RvJ3t0K2pO1TKhvfECxFRZc5dz0dqThHUNkrc18Rd7nRkw8KKqAo2Hk/B7LUnkaIrktb5ae0wc2Aootr6yZgZEZFlMLZZuK+JG+xsVTJnIx/eCiS6i43HU/DSj4dNiioASNUV4aUfD2Pj8RSZMiMishx7km7eBgxuoG0WbmJhRXQHeoPA7LUnUdmjs8Z1s9eehN7Ah2uJqOEq1Ruw/3wmgIY9cB3grUCiOzqYnFnhStWtBIAUXRFaTd8AZzsbOGps4KSxgYNaJf357/+q4KC+dV15jKPGBo7q8u3GbbYNbDb4W3EsG5H1OXI5G3nFZXBzsEWoX8NuJ8TCiugO0nNvX1TdqswgkFVQiqyCUrO8r9pGKRVoxmJLKsbUxuVbijf138smBZ3aBg4aldUUahzLRmSdjG0W7g/2hLKB/yLEworoDryd7aoUt2hYJ7TydUZecRnyi/XIKy5DQUkZ8ovLkFesv/nf8uWCEr3057ziMuSXlO+TX1yG4rLyeTBLygzILCtBZr55PoexUHO8WZg5aWzg8I9C7e8C7p/rVH/H3yzgbGqhUDOOZfvnTVXjWLbPn+nM4orIQu29Ob6qV3DDvg0IsLAiuqNuTd3h5aTB9bziSrcrAPhq7TCgnZ9ZbleV6g0oKNYjr+Tvwqug+O9CLL/kduvKC7P8Wwq1vOIylNRSoaaRCjXTq2pOt1xJ+7s4M72S9s+rcI5qFRQKxR3HsilQPpbtoVBf3hYksjC5RaX463I2gIbdv8qIhRXRHSgVgJdz5YWV8et95sBQs33Z26qU0DoooXWwNcvxSvWGm8WW6VUz45W0gpJb191arOlvift7e4m+vFArLjOguKwEGfklZsnTVqVAqf72DwAYx7IdTM5EeHMPs7wnEZnH/vOZ0BsEmng4oLGbg9zpyI6FFdEdbDieipMpObBRKuDmoDYpsHytYOyPrUoJVwc1XM30s66kzHBLMaa/5fZmFW553twnv6RioXanoupWVR3zRkR1x9i/ileryrGwIrqN/OIyvLP2JADg5b7NMSGiZYN/Wk1to4TaRg1XB7VZjldSVn5FbffZ63j154S7xjuq+SOLyNKwf5Up63hUiEgGC7eeRWpOEQLc7fFyv2ColAqEN/fAoI6NEN7co8EVVbVBbaOEm6Ma0e394ae1w93O6MTlf2Hh1rPILTLP05dEdG9SdIU4dz0fSgV4m/4mFlZElTiTlotv9iQDAGY/2qZBT89QF1RKBWYODAWACsWVcbmRqx3yivX4aPMZ9J67Hf/deQ6FJfo6zZOITBnbLLRv7AqtvXnGhlo7FlZE/yCEwPTVx1FmEHgo1AcPhPjInVKDENXWD58/0xm+WtMWF75aO3zxTGfsnvIAPh3WCc28HJFVUIo5G06j19ztWLo3GcVlLLCI5CC1WeD4KgkHLBD9w+qEqziYnAk7W6V0FYXqRlRbPzwU6nvbsWwDO/hjQFtfrE64hk+2nsHlzELMWnsSX+46j/EPtMCTXRtbTTNUImtnMAipsOrJ/lUSFlZEt9AVluL9dacAAK880IKPDsvAOJbtdmxUSjzRpTEe7eCPFfGXsWhbEq7pivDmqmP4Yuc5THiwBWI6NeIYOKJadjo1FzfySuCgVqFToJvc6VgM/mpHdIuP/kjEjbwSNPNyxPO9msmdDt2B2kaJ4WFB2P5/fTFzYCg8nTS4lFmA11ccQf+PdyL26DUYODk2Ua3Zk1TeZiGsqTvUNiwnjHgmiG46flWHH/ZfBAC8O6gtf1BYCTtbFUb3aIpdU/rijQEhcHWwxbnr+Ri/7C88vHA3Np9MgxAssIjMbU9SBgCgZwu2WbgVvzmIUD5WYPrq4zCI8nE8PThewOo4qG3wYp/m2D2lH16LaAlnjQ1Op+bi+e//RMzivdh55joLLCIzKSrV42DyzcKKPy9NsLAiArD8z8tIuJwNJ40Npke3ljsdugfOdraYENECu6f2w7h+zeGgVuHIFR1GfnsQQ/4bh/3nM+ROkcjqHb6YhaJSA7ydNWjp4yR3OhaFhRU1eJn5Jfhw42kAwMSIFvBxsbvLHmQNXB3UmBwZgl1T+uG5nk2htlHi0IUsDP1yP575+gAOX8qSO0Uiq7XnlqcBFQo+KHIrFlbU4M3deBrZBaUI8XXGqPubyJ0OmZmnkwbTHwnFrsn98Gz3INiqFNiTdAOPfbYPY5cewvGrOrlTJLI6xsKKwyYqYmFFDVr8xSz8fOgyAOC9mLawYQ+kestXa4d3Y9pi2+t9MaRrY6iUCmw9nY5HPt2Dl36Mx5m0XLlTJLIKWfklOHbzFxJOvFwRv0WowSrTG/D26uMAgCe6NEbXJu4yZ0R1IcDdAXOf6IDNr/XGoI7+UCiADcdTEblgFyb+/Bcu3MiXO0Uii7bvXAaEAFr6OHHoRCVYWFGD9eP+iziZkgOtvS2mDQiROx2qY828nPDJ0E7YOKE3otr4QghgdcI1PPjRTkz99SiuZBXInSKRRfp7fBXbLFSGhRU1SOm5RZj/xxkAwOTIVvBw0sicEcmlla8zvni2C2Jf6YkHQryhNwgs//My+v1nB2b8fhxpOUVyp0hkUYyNQXu2uP0MCQ0ZCytqkP697hRyi8vQvrEWw7oFyp0OWYC2jbT4dtR9+O2l+9Ej2AOleoHv4y6i99zteH/dSWTkFcudIpHsLmbk43JmIWxVCoQ1ZWFVGRZW1ODEncvA6oRrUCjKB6xzTjm6VZcgN/zvue5Y9nwYuga5objMgK92J6PX3O34z6ZE6ApK5U6RSDbG24CdAt3gqOF0w5VhYUUNSkmZATN+Lx+wPjwsEO0bu8qbEFms+5t7YsWL4Vg6+j60a6RFQYkei7YnoefcbVi49Sxyi1hgUcOz5+zf/auociysqEH5dm8yzqbnwcNRjcn9OWCd7kyhUKBvK2+sGd8DXz7bBSG+zsgtKsNHm8+g99zt+O/Ocygs0cudJlGd0BsE9p0zzg/Iwup2WFhRg3EtuxCfbDkLAHhjQAi0DrYyZ0TWQqFQoH8bX6x/tRc+HdYJzbwckVVQijkbTqPX3O1YujcZxWUssKh+O35VB11hKZztbNC+kVbudCwWCytqMN6NPYnCUj3ua+KGxzs3ljsdskJKpQIDO/jjj4m98Z8nOyDA3R438ooxa+1J9Ju3A8sOXEKp3iB3mkS1wji+6v7mHmymfAc8M9Qg7EhMx4bjqVApFXg3pi2UHLBO98BGpcQTXRpj66S+eH9wW/hp7XBNV4Q3Vx3Dg/N34rf4K9AbhNxpEpnV7rM32yxwfNUdsbCieq+oVI+Za04AAEbd3wQhvi4yZ0T1hdpGieFhQdj+f30xc2AoPJ00uJRZgNdXHEH/j3ci9ug1GFhgUT1QUFKG+IvlE5f3bMHGoHfCworqvf/uPI+LGQXwdtZgYkQLudOhesjOVoXRPZpi15S+eGNACFwdbHHuej7GL/sLDy/cjc0n0yAECyyyXgeTM1GqF2jkao8mHg5yp2PRzFJY6fV6JCQkICsryxyHIzKbixn5WLwjCQDw9iOhcLbjgHWqPQ5qG7zYpzl2T+mH1yJawlljg9OpuXj++z8Rs3gvdp65zgKLrNKtbRYUCg6luJMaFVYTJ07EN998A6C8qOrTpw86d+6MgIAA7Nixo8rH2bVrFwYOHAh/f38oFAqsXr3aZLtCoaj0NW/ePCkmMzMTw4cPh4uLC1xdXTF27Fjk5eWZHOfo0aPo1asX7OzsEBAQgLlz51bIZcWKFQgJCYGdnR3atWuH9evXm2wXQmDGjBnw8/ODvb09IiIicPbs2Sp/Vqp7QgjMWnMCJWUG9Az2xCPt/eROiRoIZztbTIhogd1T++Hlvs1hb6vCkSs6jPz2IIb8Nw77z2fInSJRtUjzA7LNwl3VqLD69ddf0aFDBwDA2rVrkZycjNOnT+O1117DW2+9VeXj5Ofno0OHDli8eHGl21NSUkxe3377LRQKBR5//HEpZvjw4Thx4gQ2b96M2NhY7Nq1Cy+88IK0PScnB/3790dQUBDi4+Mxb948zJo1C19++aUUs2/fPgwbNgxjx47FX3/9hZiYGMTExOD48eNSzNy5c7Fw4UJ88cUXOHDgABwdHREZGYmiIs4jZqn+OJmG7YnXYatSYPagNvwti+qcq4MaU6JCsHtqP4zt2RRqGyUOXcjC0C/345mvD+DwJV7lJ8uXnluE06m5UCiAHhy4fneiBjQajbh8+bIQQojnn39eTJgwQQghxPnz54Wzs3NNDikAiFWrVt0xZtCgQeKBBx6Qlk+ePCkAiEOHDknrNmzYIBQKhbh69aoQQojPPvtMuLm5ieLiYilm6tSpolWrVtLykCFDRHR0tMl7hYWFiX/9619CCCEMBoPw9fUV8+bNk7ZnZ2cLjUYjfvrppyp/Rp1OJwAInU5X5X2oZvKLS8X9c7aKoKmxYu7GU3KnQySEECIlu1BMX3VMBL+5TgRNjRVBU2PFmCUHxbEr2XKnRnRbqw5fEUFTY0X0wl1ypyKb6nx/1+iKlY+PD06ePAm9Xo+NGzfioYceAgAUFBRApVKZrei7VVpaGtatW4exY8dK6+Li4uDq6oquXbtK6yIiIqBUKnHgwAEppnfv3lCr1VJMZGQkEhMTpTFhcXFxiIiIMHm/yMhIxMXFAQCSk5ORmppqEqPVahEWFibFVKa4uBg5OTkmL6obn25LwtXsQjRytcf4fhywTpbBV2uHd2PaYtvrfTGka2OolApsPZ2ORz7dg5d+jMeZtFy5UySqYPfN8VW8WlU1NSqsRo8ejSFDhqBt27ZQKBRSwXHgwAGEhNTONCHfffcdnJ2d8dhjj0nrUlNT4e3tbRJnY2MDd3d3pKamSjE+Pj4mMcblu8Xcuv3W/SqLqcycOXOg1WqlV0BAQJU/L9VcUnoevt59HgAwc2Ao7NW1U+wT1VSAuwPmPtEBm1/rjUEd/aFQABuOpyJywS5M/PkvJN/IlztFIgDlY1X3JJX3r+oVzDYLVVGjwmrWrFn4+uuv8cILL2Dv3r3QaDQAAJVKhTfeeMOsCRp9++23GD58OOzs7Grl+LVh2rRp0Ol00uvy5ctyp1TvCSEw4/fjKNULPBjijYdCfe6+E5FMmnk54ZOhnbBxQm9EtfGFEMDqhGuI+Ggnpv56FFeyCuROkRq4c9fzkJZTDI2NEl2buMmdjlWwqemOTzzxBACYDN4eOXLkvWdUid27dyMxMRHLly83We/r64v09HSTdWVlZcjMzISvr68Uk5aWZhJjXL5bzK3bjev8/PxMYjp27HjbvDUajVR0Ut1YezQF+85lQGOjxKxHOWCdrEMrX2d88WwXHL+qw0ebz2Db6XQs//MyVv51BcO6BWJcv2D4uFjPL5VUfxhvA97XxB12trz6XxU1umKl1+vx7rvvolGjRnBycsL58+W3Xd5++22pDYM5ffPNN+jSpYv0JKJReHg4srOzER8fL63btm0bDAYDwsLCpJhdu3ahtLRUitm8eTNatWoFNzc3KWbr1q0mx968eTPCw8MBAE2bNoWvr69JTE5ODg4cOCDFkPxyi0rxXuxJAMC4fsEIcGcTO7IubRtp8e2o+/DbS/ejR7AHSvUC38ddRO+52/Fe7EncyCuWO0VqYKT+VWyzUGU1Kqzef/99LF26FHPnzjUZFN62bVt8/fXXVT5OXl4eEhISkJCQAKB8kHhCQgIuXbokxeTk5GDFihV47rnnKuzfunVrREVF4fnnn8fBgwexd+9ejB8/HkOHDoW/vz8A4Omnn4ZarcbYsWNx4sQJLF++HJ988gkmTZokHWfChAnYuHEj5s+fj9OnT2PWrFn4888/MX78eADl/bQmTpyI9957D2vWrMGxY8cwYsQI+Pv7IyYmpjqnjmrRx5vPIj23GE08HPBC72Zyp0NUY12C3PC/57pj2fNh6BrkhuIyA77ek4zec7dj3qbT0BWU3v0gRPeoVG+Qeq5xfsBqqMljh82bNxdbtmwRQgjh5OQkzp07J4QQ4tSpU8LV1bXKx9m+fbsAUOE1cuRIKea///2vsLe3F9nZlT+OnJGRIYYNGyacnJyEi4uLGD16tMjNzTWJOXLkiOjZs6fQaDSiUaNG4oMPPqhwnF9++UW0bNlSqNVq0aZNG7Fu3TqT7QaDQbz99tvCx8dHaDQa8eCDD4rExMQqf1Yh2G6hNp24qhPNppU/wr4zMV3udIjMxmAwiO2n08QjC3dLLRraztwoPtlyRuQUlsidHtVjB5MzRNDUWNHpnT+EXm+QOx1ZVef7WyFE9edXsLe3x+nTpxEUFARnZ2ccOXIEzZo1w8mTJ9GtW7cKnc+pXE5ODrRaLXQ6HVxcOBGwuRgMAk/+Nw7xF7PwcDtffDa8i9wpEZmdEAJ/nEzDR3+cQeLNtgxuDrZ4sU9zjAhvwqdfyew+2nwGC7eexSPt/bDo6c5ypyOr6nx/1+hWYGhoKHbv3l1h/a+//opOnTrV5JBENfbr4SuIv5gFB7UKbz8SKnc6RLVCoVAgso0vNkzohYXDOqGZpyOyCkoxZ8Np9Jq7HUv3JqO4TC93mlSP7Dl7s80Cx1dVS42eCpwxYwZGjhyJq1evwmAwYOXKlUhMTMT333+P2NhYc+dIdFvZBSX4YMNpAMDEiBbw09rLnBFR7VIqFXi0gz8ebuuL1QnXsGDLGVzJKsSstSfx5a7zGP9ACzzZtTFsVTX6vZkIAJBTVIojV3QAgJ4t2L+qOmr0L2/QoEFYu3YttmzZAkdHR8yYMQOnTp3C2rVrpS7sRHVh7qZEZOaXoKWPE0b3aCp3OkR1xkalxBNdGmPb633x/uC28HWxwzVdEd5cdQwPzt+J3+KvQG+o9kgPIgDA/nMZ0BsEmno6opErf2Gtjhr3serVqxc2b95szlyIquXI5Wz8dLD8CdJ3BrXlb+jUIKltlBgeFoTHOzfGsgOX8NmOJFzKLMDrK47gsx1JeO2hlni4rR+USvZ0o6rbk3SzzQKfBqw2fhORVdIbBKavPg4hgMGdGqF7Mw+5UyKSlZ2tCmN6NsWuKf0wNSoErg62OHc9H+OX/YWHF+7G5pNpuPVZJb1BIO5cBn5PuIq4m1cniIykworjq6qtyles3NzcqtzFOjMzs8YJEVXFsoOXcOyqDs52Npj2cO3MT0lkjRzUNnipb3M80z0Q3+65gK93n8fp1Fw8//2f6NBYi0n9W6GguAzvxJ5Eiu7vmTP8tHaYOTAUUW397nB0agiuZRfi/PV8KBVAeHP+0lpdVS6sFixYUItpEFXdjbxizNtYPmD9//q3grczp/og+idnO1tMiGiBkfcH4ctd57Fk7wUcuaLDyG8PVhqfqivCSz8exufPdGZx1cAZu613CHCFi52tzNlYnyoXVrU1DyBRdc1Zfxo5RWVo4++CZ7oHyZ0OkUVzdVBjSlQIxvRsisXbk7Bk74VK4wQABYDZa0/ioVBfqDgmq8Ey3gbsxfFVNXLPY6yKioqQk5Nj8iKqLQeTM/Hb4StQKID3Ytryhz9RFXk6adA/1PeOMQJAiq4IB5M5nKOhMhgE9krjq9hmoSZqVFjl5+dj/Pjx8Pb2hqOjI9zc3ExeRLWhVG/A26uPAwCG3heAToH8u0ZUHem5RXcPqkYc1T+nUnOQkV8CB7UKHQNc5U7HKtWosJoyZQq2bduGzz//HBqNBl9//TVmz54Nf39/fP/99+bOkQgA8N2+C0hMy4Wbgy2mRHLAOlF1VXU8IsctNlzG8VXdm3lAbcPGATVRoz5Wa9euxffff4++ffti9OjR6NWrF4KDgxEUFIT//e9/GD58uLnzpAYuVVeEjzefAQC8MSAEbo5qmTMisj7dmrrDT2uHVF0RKmuuoADgq7VDt6budZ0aWQj2r7p3NSpHMzMz0axZMwCAi4uL1F6hZ8+e2LVrl/myI7rpvXUnkV+iR+dAVzzZJUDudIiskkqpwMyB5fNpVjY6UQCYOTCUYxcbqKJSvTS+jvMD1lyNCqtmzZohOTkZABASEoJffvkFQPmVLFdXV7MlRwSUX5qOPZoCpQJ4N6YtO0gT3YOotn74/JnO8NVWvN3nam+LPi29ZciKLEH8xSwUlxng46JBsLeT3OlYrRrdChw9ejSOHDmCPn364I033sDAgQOxaNEilJaW4qOPPjJ3jtSAFZfpMeP38gHrI8KboI2/VuaMiKxfVFs/PBTqi4PJmUjPLYKrgy2m/XYM13RF+GZP+UTO1PAYbwP2CPasckNwqqhGhdVrr70m/TkiIgKnT59GfHw8goOD0b59e7MlR/T17mScv5EPTycNJvVvKXc6RPWGSqkw6ao9dUAIJvycgM93nMNT9wXCy1kjY3YkB+PAdd4GvDfVuhUYFxeH2NhYk3XGQewvvvgiFi1ahOLiYrMmSA3X5cwCfLrtLABgenRrdgAmqkUD2/ujfWMt8kv0+GTrGbnToTqWlV+C49d0AIAezVlY3YtqFVbvvPMOTpw4IS0fO3YMY8eORUREBKZNm4a1a9dizpw5Zk+SGqbZa0+iqNSA7s3cMaijv9zpENVrSqUCbz7cGgDw08HLSErPkzkjqkt7z92AEEArH2d4u7Ddxr2oVmGVkJCABx98UFr++eefERYWhq+++gqvvfYaFi5cKA1kJ7oXW06mYcupNNgoFXh3UFve7yeqA92beSCitQ/0BoEPNpyWOx2qQ393W+fVqntVrcIqKysLPj4+0vLOnTsxYMAAafm+++7D5cuXzZcdNUiFJXrMWlt+ZXRsr6Zo4eMsc0ZEDccbA0KgUiqw5VQa9p/PkDsdqgNCCOw+y8LKXKpVWPn4+EhtFkpKSnD48GF0795d2p6bmwtbW46DoXvz2Y4kXMkqhJ/WDq/y6SSiOhXs7YRh3cp7xf17/SkYDJW1EqX65GJGAa5kFcJWpUAYm8Pes2oVVg8//DDeeOMN7N69G9OmTYODgwN69eolbT969CiaN29u9iSp4Ui+kY//7jwPAJjxSCgcNTV6cJWI7sGEB1vCUa3C0Ss6rD16Te50qJYZ2yx0DnSDg5o/c+9VtQqrd999FzY2NujTpw+++uorfPXVV1Cr/55a5Ntvv0X//v3NniQ1DEIIzPj9OEr0BvRp6YWotr5yp0TUIHk5a/BS3/JfkuduTERRqV7mjKg2sc2CeVWrNPX09MSuXbug0+ng5OQElUplsn3FihVwcmK3VqqZ9cdSsfvsDahtlJj9aBsOWCeS0diezfDj/ku4ml2I7+Mu4IXevBtRH+kNAvvO/d0YlO5djaa00Wq1FYoqAHB3dze5gkVUVXnFZXg39iQA4MU+zdHE01HmjIgaNnu1Cq/fbMr76bYkZOWXyJwR1YajV7KRU1QGFzsbtG/sKnc69UKNCisic1u49SxSc4oQ6O6Al/vyN2MiS/BY58YI8XVGblEZPt2WJHc6VAuMbRbub+7JybfNhIUVyS4xNRff7Cl/2nT2o21gZ1vxaigR1T2VUoG3osubhv6w/wIuZuTLnBGZm7HNQg+OrzIbFlYkKyEE3v79OPQGgf6hPugX4i13SkR0i14tvNC7pRdK9QJzNybKnQ6ZUX5xGQ5fygIA9OL4KrNhYUWyWvXXVRxMzoS9rQozBobKnQ4RVeLNh0OgVADrjqUg/mKW3OmQmRy8kIlSvUBjN3sEeTjInU69wcKKZKMrLMW/158CALzyYDAau/EfNpElCvF1wRNdGgMobxoqBJuG1ge3tlngU9jmw8KKZDP/j0TcyCtBcy9HPNezmdzpENEdTHqoFextVYi/mIWNx1PlTofMwFhYsc2CebGwIlkcv6rDj/svAgDeHdQWahv+VSSyZL5aOzzfqykA4MONp1FSZpA5I7oX6blFSEzLhUIB9GjOwsqc+G1Gdc5gEHhr9XEYBPBoB3/cz9+WiKzCC32aw9NJgwsZBfjfgYtyp0P3wNhmoa2/Fm6O7D9pTiysqM79fOgyjlzOhpPGBtNvPspNRJbPSWOD1x4qnxh94daz0BWWypwR1dRu3gasNSysqE5l5pdg7qbTAIDXHmoJbxc7mTMioup4qmsAgr2dkFVQis92sGmoNRJCcH7AWsTCiurUhxtOI7ugFCG+zhgZHiR3OkRUTTYqJaYNCAEALNl7AVeyCmTOiKorKT0P6bnF0Ngo0SXITe506h0WVlRn4i9mYvmflwEA7w9uCxsV//oRWaMHQrwR3swDJWUG/GcTm4ZaG+NtwG5N3TnTRS2Q9Ztt165dGDhwIPz9/aFQKLB69eoKMadOncKjjz4KrVYLR0dH3Hfffbh06ZK0vaioCOPGjYOHhwecnJzw+OOPIy0tzeQYly5dQnR0NBwcHODt7Y3JkyejrKzMJGbHjh3o3LkzNBoNgoODsXTp0gq5LF68GE2aNIGdnR3CwsJw8OBBs5yHhqBMb8D01ScAAE92aYwuQe4yZ0RENaVQKPDmw+XjI1cnXMOxKzqZM6Lq2HNz4HpPjq+qFbIWVvn5+ejQoQMWL15c6fZz586hZ8+eCAkJwY4dO3D06FG8/fbbsLP7e1zOa6+9hrVr12LFihXYuXMnrl27hscee0zartfrER0djZKSEuzbtw/fffcdli5dihkzZkgxycnJiI6ORr9+/ZCQkICJEyfiueeew6ZNm6SY5cuXY9KkSZg5cyYOHz6MDh06IDIyEunp6bVwZuqfH/ZfxKmUHGjtbfHGzdsIRGS92jXWYnCnRgCA99efZNNQK1GqN2D/+QwAQE+Or6odwkIAEKtWrTJZ99RTT4lnnnnmtvtkZ2cLW1tbsWLFCmndqVOnBAARFxcnhBBi/fr1QqlUitTUVCnm888/Fy4uLqK4uFgIIcSUKVNEmzZtKrx3ZGSktNytWzcxbtw4aVmv1wt/f38xZ86cKn9GnU4nAAidTlflfeqDNF2haDtjowiaGit+3H9B7nSIyEwuZ+aLFm+tF0FTY8WWk6l334Fkd+B8hgiaGis6v/OH0OsNcqdjNarz/W2xg1wMBgPWrVuHli1bIjIyEt7e3ggLCzO5XRgfH4/S0lJERERI60JCQhAYGIi4uDgAQFxcHNq1awcfHx8pJjIyEjk5OThx4oQUc+sxjDHGY5SUlCA+Pt4kRqlUIiIiQoqh23t//SnkFpehQ2Mtht4XKHc6RGQmjd0cMKZHedPQf68/hTI9m4Zauj1nrwMA7g/2hFLJaWxqg8UWVunp6cjLy8MHH3yAqKgo/PHHHxg8eDAee+wx7Ny5EwCQmpoKtVoNV1dXk319fHyQmpoqxdxaVBm3G7fdKSYnJweFhYW4ceMG9Hp9pTHGY1SmuLgYOTk5Jq+GZt+5G/g94RoUCuDdmLZQ8R8yUb3ycr/mcHOwxbnr+dLDKWS5dt8cX9WL46tqjcUWVgZD+W8+gwYNwmuvvYaOHTvijTfewCOPPIIvvvhC5uyqZs6cOdBqtdIrICBA7pTqVEmZATN+L78q+ExYENo3dpU3ISIyOxc7W0x4sLxp6MebzyCvuOwue5BccopKceRyNgCOr6pNFltYeXp6wsbGBqGhoSbrW7duLT0V6Ovri5KSEmRnZ5vEpKWlwdfXV4r551OCxuW7xbi4uMDe3h6enp5QqVSVxhiPUZlp06ZBp9NJr8uXG9Zvc9/sSUZSeh48HNX4v/6t5E6HiGrJ02FBaOLhgBt5Jfhy5zm506HbiDuXAYMAmnk5wt/VXu506i2LLazUajXuu+8+JCaa9kg5c+YMgoLKG0t26dIFtra22Lp1q7Q9MTERly5dQnh4OAAgPDwcx44dM3l6b/PmzXBxcZGKtvDwcJNjGGOMx1Cr1ejSpYtJjMFgwNatW6WYymg0Gri4uJi8Goqr2YVYuPUsAGDaw62hdbCVOSMiqi1qG6X0tO+Xu88jVVckc0ZUGWO3dbZZqF02cr55Xl4ekpL+nhIhOTkZCQkJcHd3R2BgICZPnoynnnoKvXv3Rr9+/bBx40asXbsWO3bsAABotVqMHTsWkyZNgru7O1xcXPDKK68gPDwc3bt3BwD0798foaGhePbZZzF37lykpqZi+vTpGDduHDQaDQDgxRdfxKJFizBlyhSMGTMG27Ztwy+//IJ169ZJuU2aNAkjR45E165d0a1bNyxYsAD5+fkYPXp03Z0wK/Lu2pMoLNXjviZueLxzI7nTIaJaFtnGF12D3PDnxSx8tDkRc5/oIHdK9A972b+qbtTBU4q3tX37dgGgwmvkyJFSzDfffCOCg4OFnZ2d6NChg1i9erXJMQoLC8XLL78s3NzchIODgxg8eLBISUkxiblw4YIYMGCAsLe3F56enuL1118XpaWlFXLp2LGjUKvVolmzZmLJkiUV8v30009FYGCgUKvVolu3bmL//v3V+rwNpd3CttNpImhqrGg2bZ04lVK/PysR/S3+YqYImhormrwRK05e4799S3Ilq0D6uawrLJE7HatTne9vhRDs6lZXcnJyoNVqodPp6u1twaJSPSIX7MLFjAI817Mppj8SevediKjeGPe/w1h3LAW9W3rh+zHd5E6Hblp+6BKm/nYMnQNdsfLlHnKnY3Wq8/1tsWOsyDp9sfMcLmYUwMdFg4kPtZQ7HSKqY1OiWsFWpcCuM9ex68x1udOhm/YkGbute8mcSf3HworM5mJGPj7bUf5E0NuPhMJJI+sQPiKSQZCHI57t3gRAedNQvYE3ReRmMAhpfFUvtlmodSysyCyEEJi55gRKygzoGeyJ6HZ+cqdERDJ55YFguNjZ4HRqLn47fEXudBq8kyk5yMwvgaNahY4BrnKnU++xsCKz2HQiDTsSr8NWpcDsQW2gULDDOlFD5eaoxvgHggEA8/9IRGGJXuaMGrY9N69WdW/mAVsVv/ZrG88w3bOCkjK8s7a8w/q/ejdHcy8nmTMiIrmNCG+Cxm72SMspxte7z8udToMmtVngbcA6wcKK7tnCrUm4pitCI1d7jOsXLHc6RGQB7GxVmBxZPuPCFzvP4XpuscwZNUxFpXocTM4EwPFVdYWFFd2TpPRc6bfRWY+2gb1aJXNGRGQpBrb3R4fGWuSX6LFgyxm502mQ/ryQheIyA3xcNLybUEdYWFGNCSHw9uoTKDMIPBjijYdCfeROiYgsiFKpwJsPtwYA/HzoMpLSc2XOqOHZI3Vb9+LY1zrCwopqbM2Ra4g7nwGNjRKzHm0jdzpEZIHCmnngoVAf6A0CH2w4LXc6Dc6epPJeYrwNWHdYWFGN5BSV4r11pwAA4/sFI8DdQeaMiMhSvTEgBCqlAltOpSPuXIbc6TQYmfklOHEtBwDQg/MD1hkWVlQjH28+g+u5xWjq6YgX+jSTOx0ismDNvZzwdLdAAOVNQw1sGlon9ibdgBBAiK8zvJw1cqfTYLCwomo7cU2H7/ZdAADMfrQNNDYcsE5EdzYhogWcNDY4dlWHtUevyZ1OgyC1WeDVqjrFwoqqxWAQeHv1cRgEEN3OD71bct4pIro7TycNXurbHAAwd2MiikrZNLQ2CSGw+yz7V8mBhRVVy6/xV3D4UjYc1CpMf6S13OkQkRUZ06MpfF3scDW7ULrqTbXjQkYBrmYXQq1SoltTd7nTaVBYWFGVZReU4ION5U/1TIxoAT+tvcwZEZE1sVer8H83m4Yu2p6ErPwSmTOqv4xtFjoHucJBbSNzNg0LCyuqsrmbEpGZX4KWPk4Y3aOp3OkQkRUa3KkRWvu5ILeoDAu3nZU7nXprz1ljmwUO16hrLKyoShIuZ+Ong5cAAO8OasuJPImoRlRKBd662TT0h7iLuHAjX+aM6p8yvQH7bra14MD1usdvR7orvUFg+upjEAJ4rFMjhDXzkDslIrJiPVt4ok9LL5QZBOZuYtNQczt6VYfcojJo7W3RtpFW7nQaHBZWdFfLDlzE8as5cLazwbSHOWCdiO7dmw+3hlIBrD+WiviLmXKnU6/svfk04P3NPaBSchqbusbCiu7oem4x5m5KBABMjmzFJnNEZBatfJ3xZJcAAMD7605BCDYNNZfdSWyzICcWVnRHczacQm5RGdo2csHwsCC50yGiemRS/5awt1Xh8KVsbDieKnc69UJ+cRn+upQFgOOr5MLCim7rwPkMrDx8FQpF+YB1XlImInPycbHD873Lp8T6cONplJQZZM7I+h1MzkSpXiDA3R5BHo5yp9MgsbCiSpXqDXj79+MAgKH3BaJToJvMGRFRffSv3s3g6aTBxYwC/Lj/otzpWD2p23ow2yzIhYUVVWrp3gs4k5YHNwdbTLnZ0I+IyNwcNTaY9FBLAMDCbWehKyyVOSPrtiepvH8VbwPKh4UVVZCqK8KCLWcAAG8MCIGbo1rmjIioPhvStTFaeDshu6AUn21Pkjsdq5WeU4QzaXlQKMqfCCR5sLCiCt5ddxL5JXp0DnSVntohIqotNiolpj0cAgBYsu8CLmcWyJyRdTJOY9OukZa/EMuIhRWZ2HXmOtYdTYFSAbwb0xZKDlgnojrQr5U37m/ugZIyA/7zR6Lc6VilPdL4Kt4GlBMLK5IUl+kxc80JAMCI8CZo48+OvURUNxQKBd682YD494RrOHolW96ErIwQQrpixcJKXiysSPLVrvNIvpEPL2cNJvVvKXc6RNTAtG2kxWOdGgFg09DqOpueh/TcYtjZKtGlCZ/ilhMLKwIAXM4swKfbygeNTo9uDRc7W5kzIqKG6PXIVlDbKHEgORNbT6XLnY7VMLZZ6NbUAxoblczZNGwsrAgAMHvtCRSXGRDezAOPdvCXOx0iaqAaudpjbM+mAMpnfijTs2loVew5a2yzwKcB5cbCirDlZBq2nEqHjVKBdwa1gULBAetEJJ+X+jaHu6Ma567n4+dDl+VOx+KVlBlwILl8Ims2BpUfC6sGrrBEj1lrywesP9erGVr4OMucERE1dC52tpjwYAsAwIItZ5BXXCZzRpbtr0tZKCjRw9NJjRBf/gyXGwurBm7x9iRcySqEv9YOrz4YLHc6REQAgKfDAtHU0xE38krw353n5E7HohmfBuwR7MkWORaAhVUDdv56Hr7cdR4AMGNgKBzUNjJnRERUzlalxNSo8qahX+0+j1RdkcwZWS7jwPUebLNgEVhYNVBCCMz4/QRK9Ab0beWFyDa+cqdERGQiso0Puga5oajUgPlsGlopXWGp1POrVwsWVpaAhVUDte5YCvYk3YDaRonZj3LAOhFZHoVCgbeiy5uG/nr4Ck5ey5E5I8sTdy4DBgE093KEn9Ze7nQILKwapLziMrwbexIA8FKf5gjycJQ5IyKiynUKdEN0ez8IUd5+gUztSTK2WeDVKksha2G1a9cuDBw4EP7+/lAoFFi9erXJ9lGjRkGhUJi8oqKiTGIyMzMxfPhwuLi4wNXVFWPHjkVeXp5JzNGjR9GrVy/Y2dkhICAAc+fOrZDLihUrEBISAjs7O7Rr1w7r16832S6EwIwZM+Dn5wd7e3tERETg7Nmz5jkRdeyTLWeQllOMIA8HvNS3udzpEBHd0dTIENiqFNh99gZ2nrkudzoWZW9SBgCgZwu2WbAUshZW+fn56NChAxYvXnzbmKioKKSkpEivn376yWT78OHDceLECWzevBmxsbHYtWsXXnjhBWl7Tk4O+vfvj6CgIMTHx2PevHmYNWsWvvzySylm3759GDZsGMaOHYu//voLMTExiImJwfHjx6WYuXPnYuHChfjiiy9w4MABODo6IjIyEkVF1jWg8nRqDr7dewEAMOvRNrCzZYdeIrJsgR4OGBHeBAAwZ/0p6A2c6gYArmQVIPlGPlRKBbo3c5c7HTISFgKAWLVqlcm6kSNHikGDBt12n5MnTwoA4tChQ9K6DRs2CIVCIa5evSqEEOKzzz4Tbm5uori4WIqZOnWqaNWqlbQ8ZMgQER0dbXLssLAw8a9//UsIIYTBYBC+vr5i3rx50vbs7Gyh0WjETz/9VOXPqNPpBACh0+mqvI85GQwG8eTn+0TQ1FjxwveH7r4DEZGFyMovFu1mbhRBU2PF8oOX5E7HIvx04KIImhorHv9sr9yp1HvV+f62+DFWO3bsgLe3N1q1aoWXXnoJGRkZ0ra4uDi4urqia9eu0rqIiAgolUocOHBAiunduzfUarUUExkZicTERGRlZUkxERERJu8bGRmJuLg4AEBycjJSU1NNYrRaLcLCwqSYyhQXFyMnJ8fkJaeVh6/i4IVM2NuqMGNgG1lzISKqDlcHNV55oLxp6PzNiSgoYdPQ3Ulss2CJLLqwioqKwvfff4+tW7fiww8/xM6dOzFgwADo9XoAQGpqKry9vU32sbGxgbu7O1JTU6UYHx8fkxjj8t1ibt1+636VxVRmzpw50Gq10isgIKBan9+cdAWl0sDPVx9sgUaufHqEiKzLiPuD0NjNHmk5xfh6d7Lc6cjKYBDYd7OwYpsFy2LRhdXQoUPx6KOPol27doiJiUFsbCwOHTqEHTt2yJ1alUybNg06nU56Xb4s35xX//kjETfyShDs7SRNcEpEZE00NipMudk09Iud55Cea11jXM3pZEoOsgpK4aSxQYcAV7nToVtYdGH1T82aNYOnpyeSkpIAAL6+vkhPTzeJKSsrQ2ZmJnx9faWYtLQ0kxjj8t1ibt1+636VxVRGo9HAxcXF5CWHY1d0+PHARQDAO4PaQG1jVf/biYgkA9v7oUOAKwpK9FiwxTqfzDYHY7f17s3cYaviz3RLYlX/N65cuYKMjAz4+fkBAMLDw5GdnY34+HgpZtu2bTAYDAgLC5Nidu3ahdLSUilm8+bNaNWqFdzc3KSYrVu3mrzX5s2bER4eDgBo2rQpfH19TWJycnJw4MABKcZS6Q0C01cfgxDAoI7+uL85LxkTkfVSKBR46+HypqHLD13G2bRcmTOSx96btwHZv8ryyFpY5eXlISEhAQkJCQDKB4knJCTg0qVLyMvLw+TJk7F//35cuHABW7duxaBBgxAcHIzIyEgAQOvWrREVFYXnn38eBw8exN69ezF+/HgMHToU/v7+AICnn34aarUaY8eOxYkTJ7B8+XJ88sknmDRpkpTHhAkTsHHjRsyfPx+nT5/GrFmz8Oeff2L8+PEAyv8hT5w4Ee+99x7WrFmDY8eOYcSIEfD390dMTEydnrPq+vnQJRy5ooOzxkb6YUREZM26NXVH/1Af6A0CH2w4LXc6da6oVI+DFzIBsH+VRaqDpxRva/v27QJAhdfIkSNFQUGB6N+/v/Dy8hK2trYiKChIPP/88yI1NdXkGBkZGWLYsGHCyclJuLi4iNGjR4vc3FyTmCNHjoiePXsKjUYjGjVqJD744IMKufzyyy+iZcuWQq1WizZt2oh169aZbDcYDOLtt98WPj4+QqPRiAcffFAkJiZW6/PWdbuFG7lFov2sTSJoaqz4Zvf5OnlPIqK6kJSeK5pNWyeCpsaKvUnX5U6nTu06ky6CpsaK7v/eIgwGg9zpNAjV+f5WCCHYaa2O5OTkQKvVQqfT1cl4qym/HsEvf15Baz8XrB3fAza8D09E9ciM34/j+7iLaNvIBWvG9YRS2TDmPJ2z4RT+u/M8nujSGP95soPc6TQI1fn+5jdtPRV/MRO//HkFAPBeTBsWVURU70x4sAWcNDY4fjUHa45ckzudOrPnLNssWDJ+29ZDZXoD3lpVPh3PkK6N0SWIUx0QUf3j4aSR5judtykRRaV6mTOqfRl5xThxrbzZNB9GskwsrOqh7+Mu4nRqLrT2tph6s+cLEVF9NLZnU/hp7XA1uxBL912QO51at/dc+ewjIb7O8HLWyJwNVYaFVT2TnlOEjzafAQBMjQqBhxP/4RFR/WVnq8L/9W8FAFi8LQmZ+SUyZ1S79vI2oMVjYVUP6A0Ccecy8HvCVUxcnoC84jJ0CHDF0Pvkm0KHiKiuDO7UCKF+LsgtLsPCrfW3aagQAnuM/avYZsFi2cidAN2bjcdTMHvtSaToTKd2eLitb4N5QoaIGjalUoG3oltj+NcH8OP+ixh5fxM09XSUOy2zS76Rj6vZhVCrlOjWhGNnLRWvWFmxjcdT8NKPhysUVQDwwYbT2Hg8RYasiIjqXo9gT/Rt5YUyg8DcjfWzaaix23qXIDfYq1UyZ0O3w8LKSukNArPXnsSdmpDNXnsSegPblBFRwzBtQGsoFcCG46n482Zn8vrEOD9gT46vsmgsrKzUweTMSq9UGQkAKboiHEyufz9ciIgq08rXGUO6lo8tfX/9KdSn/tdlegPibj4RyIHrlo2FlZVKz719UVWTOCKi+mDSQy1hb6vCX5eysf5YqtzpmM2RKzrkFpdBa2+LNv5audOhO2BhZaW8ne3MGkdEVB94u9jhhd7NAAAfbjyNkjKDzBmZh3F8VY9gD6j4YJJFY2Flpbo1dYef1g63++elAOCntUO3pnxyhIgalhd6N4OXswaXMgvww/6LcqdjFsZpbHoGs82CpWNhZaVUSgVmDgwFgArFlXF55sBQ/mZDRA2Oo8YGkx5qCQD4dNtZ6ApKZc7o3uQVl+HwpSwAHF9lDVhYWbGotn74/JnO8NWa3u7z1drh82c6I6qtn0yZERHJ68kujdHSxwnZBaVYvCNJ7nTuycHkDJQZBALdHRDg7iB3OnQXbBBq5aLa+uGhUF8cTM5Eem4RvJ3Lb//xShURNWQ2KiWmDWiN0UsPYeneC3i2e5DVFiVss2BdeMWqHlApFQhv7oFBHRshvDkHNhIRAUDfVl7oEeyBEr0B8zYlyp1OjRnHV/UKZmFlDVhYERFRvaRQKDBtQGsoFMCaI9dw5HK23ClVW6quCGfT86BQAOHNPeROh6qAhRUREdVbbRtpMbhTIwDW2TTU2GahfSMtXB3UMmdDVcHCioiI6rX/698KGhslDiZnYsupdLnTqZY9SRxfZW1YWBERUb3m72qPsT2bAgDmbDiFUr11NA0VQvxdWLF/ldVgYUVERPXei32bw91RjfPX8/Hzoctyp1MlZ9LycD23GPa2KnQOcpU7HaoiFlZERFTvudjZYmJECwDAgs1nkFtk+U1Dd5+9DqB8pg2NjUrmbKiqWFgREVGDMKxbIJp5OiIjvwT/3Xle7nTuyngbkN3WrQsLKyIiahBsVUpMHRACAPhq93mk6Aplzuj2SsoMOHA+EwDQg/2rrAoLKyIiajD6h/rgviZuKC4zYP4fZ+RO57YOX8pCYakenk4ahPg6y50OVQMLKyIiajAUCgXefLg1AOC3w1dw8lqOzBlVzthtvWewBxQKzqZhTVhYERFRg9Ip0A2PtPeDEMC/LbRp6O6b46t4G9D6sLAiIqIGZ2pUCNQqJfYk3cDOM9flTseErqAUx65kAwB6tWD/KmvDwoqIiBqcAHcHjAgPAgDMWX8aeoPlXLWKO38DBgEEezvBV2sndzpUTSysiIioQRr/QDC09rZITMvFr/GW0zR0tzS+ircBrRELKyIiapBcHdR45YFgAMD8P86goKRM5ozK7U1iYWXNWFgREVGD9Wx4EALc7ZGeW4yvdiXLnQ4uZxbgQkYBbJQKdG/uIXc6VAMsrIiIqMHS2KgwJbK8aeh/d51Dem6RrPkYu613CnSFk8ZG1lyoZlhYERFRg/ZIez90DHBFQYkeH28+K2suxv5VbLNgvVhYERFRg6ZQKPBWdHnT0OWHLuFsWq4seRgMAnvPcX5Aa8fCioiIGrz7mrgjso0PDAL4YMNpWXI4cS0H2QWlcNbYoENjV1lyoHvHwoqIiAjlTUNtlApsPZ2OfTevHNWl3UnljUq7N/eAjYpfz9aK/+eIiIgANPNywvCwQADlU90Y6rhpKNss1A+yFla7du3CwIED4e/vD4VCgdWrV9829sUXX4RCocCCBQtM1mdmZmL48OFwcXGBq6srxo4di7y8PJOYo0ePolevXrCzs0NAQADmzp1b4fgrVqxASEgI7Ozs0K5dO6xfv95kuxACM2bMgJ+fH+zt7REREYGzZ+Ud5EhEROb16oMt4KyxwfGrOfj9yNU6e9+iUj0OXcgCAPTk+CqrJmthlZ+fjw4dOmDx4sV3jFu1ahX2798Pf3//CtuGDx+OEydOYPPmzYiNjcWuXbvwwgsvSNtzcnLQv39/BAUFIT4+HvPmzcOsWbPw5ZdfSjH79u3DsGHDMHbsWPz111+IiYlBTEwMjh8/LsXMnTsXCxcuxBdffIEDBw7A0dERkZGRKCqS99FcIiIyHw8nDV7q1xwA8J9NZ1BUqq+T9z2YnImSMgP8tXZo5ulYJ+9JtURYCABi1apVFdZfuXJFNGrUSBw/flwEBQWJjz/+WNp28uRJAUAcOnRIWrdhwwahUCjE1atXhRBCfPbZZ8LNzU0UFxdLMVOnThWtWrWSlocMGSKio6NN3jcsLEz861//EkIIYTAYhK+vr5g3b560PTs7W2g0GvHTTz9V+TPqdDoBQOh0uirvQ0REdauwpEyE/3uLCJoaKz7bnlQn7/n+upMiaGqs+L9fEurk/ah6qvP9bdFjrAwGA5599llMnjwZbdq0qbA9Li4Orq6u6Nq1q7QuIiICSqUSBw4ckGJ69+4NtVotxURGRiIxMRFZWVlSTEREhMmxIyMjERcXBwBITk5GamqqSYxWq0VYWJgUU5ni4mLk5OSYvIiIyLLZ2arwf5GtAACfbU9CZn5Jrb+nsX8VbwNaP4surD788EPY2Njg1VdfrXR7amoqvL29TdbZ2NjA3d0dqampUoyPj49JjHH5bjG3br91v8piKjNnzhxotVrpFRAQcMfPS0REliGmYyO08XdBbnEZFm6t3fG0N/KKcTKl/BdvNga1fhZbWMXHx+OTTz7B0qVLoVAo5E6nRqZNmwadTie9Ll+2nNnTiYjo9pRKBd56uLxp6I/7LyL5Rn6tvZfxacBQPxd4Omlq7X2oblhsYbV7926kp6cjMDAQNjY2sLGxwcWLF/H666+jSZMmAABfX1+kp6eb7FdWVobMzEz4+vpKMWlpaSYxxuW7xdy6/db9KoupjEajgYuLi8mLiIisw/3BnujXygtlBoEPa7FpqNRmgbcB6wWLLayeffZZHD16FAkJCdLL398fkydPxqZNmwAA4eHhyM7ORnx8vLTftm3bYDAYEBYWJsXs2rULpaWlUszmzZvRqlUruLm5STFbt241ef/NmzcjPDwcANC0aVP4+vqaxOTk5ODAgQNSDBER1T/THm4NpQLYeCIVf17INPvxhRB/j6/ibcB6QdbCKi8vTyqagPJB4gkJCbh06RI8PDzQtm1bk5etrS18fX3RqlX5oMLWrVsjKioKzz//PA4ePIi9e/di/PjxGDp0qNSa4emnn4ZarcbYsWNx4sQJLF++HJ988gkmTZok5TFhwgRs3LgR8+fPx+nTpzFr1iz8+eefGD9+PIDyeaQmTpyI9957D2vWrMGxY8cwYsQI+Pv7IyYmpk7PGRER1Z2WPs546r7y8bHvrz8FIczbNPT8jXxc0xVBbaNEt6buZj02yaTWn1G8g+3btwsAFV4jR46sNP6f7RaEECIjI0MMGzZMODk5CRcXFzF69GiRm5trEnPkyBHRs2dPodFoRKNGjcQHH3xQ4di//PKLaNmypVCr1aJNmzZi3bp1JtsNBoN4++23hY+Pj9BoNOLBBx8UiYmJ1fq8bLdARGR90nSFovXbG0TQ1FgRe+SaWY/93b5kETQ1Vgz7Ms6sxyXzqs73t0IIM5ffdFs5OTnQarXQ6XQcb0VEZEUWbDmDBVvOItDdAZsn9YbGRmWW4z7//Z/YfDINU6Ja4eW+wWY5Jplfdb6/LXaMFRERkaV4oXczeDtrcCmzAD/uv2SWY5bpDdh/LgMA0CvYyyzHJPmxsCIiIroLB7UNJj3UEgCwcOtZ6ApK77LH3R25ko3c4jK4OtiijT/vYtQXLKyIiIiq4MmuAWjl4wxdYSkW70i65+PtOVt+tapHc08oldbZr5EqYmFFRERUBSqlAm88HAIAWLr3Ai5nFtzT8fYkXQfA/lX1DQsrIiKiKurb0gs9gz1Rojdg3qbEGh8nr7gMf13KBsD+VfUNCysiIqIqUigUmPZwCBQKYM2RazhyObtGxzlwPgNlBoEgDwcEuDuYN0mSFQsrIiKiamjjr8VjnRoDqHnT0N3stl5vsbAiIiKqpv+LbAmNjRIHkzOx+WTa3Xf4hz035wfsxfFV9Q4LKyIiomry09rjuV5NAQAfbDyNUr2hyvum6AqRlJ4HpQIIb8bCqr5hYUVERFQDL/ZpDg9HNc5fz8fPB6veNHRvUnmbhXaNXaF1sK2t9EgmLKyIiIhqwNnOFhMjWgAAFmw5i9yiqjUN3XO2vM1CL46vqpdYWBEREdXQ0G6BaObpiIz8Enyx89xd44UQ2HPzihX7V9VPLKyIiIhqyFalxBsDypuGfr07GSm6wjvGJ6bl4kZeMextVegU6FoHGVJdY2FFRER0Dx4K9UG3Ju4oLjPgP5vO3DF2z802C2HN3KGxUdVFelTHWFgRERHdA4VCgTejWwMAVv51BSeu6W4by/5V9R8LKyIionvUMcAVAzv4QwhgzvrTlTYNLS7T40By+fiqXi286jpFqiMsrIiIiMxgSmQrqFVK7Em6gZ1nrlfYfvhiNopKDfBy1qClj5MMGVJdYGFFRERkBgHuDhh5fxCA8qtWeoPpVas9SeXFVs9gTygUijrPj+oGCysiIiIzGd+vBbT2tkhMy8Wv8ZdNtu3h+KoGgYUVERGRmWgdbPHKA8EAgPl/nEFBSRkAQFdQiqNXywe192BhVa+xsCIiIjKjZ8ODEOjugPTcYny1KxkAsO/cDQgBtPB2gq/WTuYMqTaxsCIiIjIjjY0KU6JaAQC+2JmEDcdT8MP+iwCA+4M95EyN6gALKyIiIjOLbueHJh4OKCw14KUfD2PfufI2C2sSrmHj8RSZs6PaxMKKiIjIzDadSMWFjIIK67MLSvHSj4dZXNVjLKyIiIjMSG8QmL32ZKXbjA0YZq89WaEdA9UPLKyIiIjM6GByJlJ0RbfdLgCk6IpwMDmz7pKiOsPCioiIyIzSc29fVNUkjqwLCysiIiIz8nauWjuFqsaRdWFhRUREZEbdmrrDT2uH201aowDgp7VDt6budZkW1REWVkRERGakUiowc2AoAFQorozLMweGQqXkfIH1EQsrIiIiM4tq64fPn+lcocu6r9YOnz/TGVFt/WTKjGqbjdwJEBER1UdRbf3wUKgvDiZnIj23CN7O5bf/eKWqfmNhRUREVEtUSgXCm3Mam4aEtwKJiIiIzISFFREREZGZsLAiIiIiMhMWVkRERERmwsKKiIiIyExkLax27dqFgQMHwt/fHwqFAqtXrzbZPmvWLISEhMDR0RFubm6IiIjAgQMHTGIyMzMxfPhwuLi4wNXVFWPHjkVeXp5JzNGjR9GrVy/Y2dkhICAAc+fOrZDLihUrEBISAjs7O7Rr1w7r16832S6EwIwZM+Dn5wd7e3tERETg7Nmz5jkRREREVC/IWljl5+ejQ4cOWLx4caXbW7ZsiUWLFuHYsWPYs2cPmjRpgv79++P69etSzPDhw3HixAls3rwZsbGx2LVrF1544QVpe05ODvr374+goCDEx8dj3rx5mDVrFr788kspZt++fRg2bBjGjh2Lv/76CzExMYiJicHx48elmLlz52LhwoX44osvcODAATg6OiIyMhJFRZxEk4iIiG4SFgKAWLVq1R1jdDqdACC2bNkihBDi5MmTAoA4dOiQFLNhwwahUCjE1atXhRBCfPbZZ8LNzU0UFxdLMVOnThWtWrWSlocMGSKio6NN3issLEz861//EkIIYTAYhK+vr5g3b560PTs7W2g0GvHTTz9V+TMa89fpdFXeh4iIiORVne9vqxljVVJSgi+//BJarRYdOnQAAMTFxcHV1RVdu3aV4iIiIqBUKqVbhnFxcejduzfUarUUExkZicTERGRlZUkxERERJu8XGRmJuLg4AEBycjJSU1NNYrRaLcLCwqSYyhQXFyMnJ8fkRURERPWXxXdej42NxdChQ1FQUAA/Pz9s3rwZnp6eAIDU1FR4e3ubxNvY2MDd3R2pqalSTNOmTU1ifHx8pG1ubm5ITU2V1t0ac+sxbt2vspjKzJkzB7Nnz66wngUWERGR9TB+bwsh7hpr8YVVv379kJCQgBs3buCrr77CkCFDcODAgQoFlSWaNm0aJk2aJC1fvXoVoaGhCAgIkDErIiIiqonc3Fxotdo7xlh8YeXo6Ijg4GAEBweje/fuaNGiBb755htMmzYNvr6+SE9PN4kvKytDZmYmfH19AQC+vr5IS0sziTEu3y3m1u3GdX5+fiYxHTt2vG3uGo0GGo1GWnZycsLly5fh7OwMhcK8k3Dm5OQgICAAly9fhouLi1mPTX/jea4bPM91g+e5bvA8143aPM9CCOTm5sLf3/+usRZfWP2TwWBAcXExACA8PBzZ2dmIj49Hly5dAADbtm2DwWBAWFiYFPPWW2+htLQUtra2AIDNmzejVatWcHNzk2K2bt2KiRMnSu+zefNmhIeHAwCaNm0KX19fbN26VSqkcnJycODAAbz00ktVzl2pVKJx48b39PnvxsXFhf9w6wDPc93gea4bPM91g+e5btTWeb7blSojWQev5+XlISEhAQkJCQDKB4knJCTg0qVLyM/Px5tvvon9+/fj4sWLiI+Px5gxY3D16lU8+eSTAIDWrVsjKioKzz//PA4ePIi9e/di/PjxGDp0qFRVPv3001Cr1Rg7dixOnDiB5cuX45NPPjG5RTdhwgRs3LgR8+fPx+nTpzFr1iz8+eefGD9+PABAoVBg4sSJeO+997BmzRocO3YMI0aMgL+/P2JiYur0nBEREZEFq/VnFO9g+/btAkCF18iRI0VhYaEYPHiw8Pf3F2q1Wvj5+YlHH31UHDx40OQYGRkZYtiwYcLJyUm4uLiI0aNHi9zcXJOYI0eOiJ49ewqNRiMaNWokPvjggwq5/PLLL6Jly5ZCrVaLNm3aiHXr1plsNxgM4u233xY+Pj5Co9GIBx98UCQmJpr/pNQQWznUDZ7nusHzXDd4nusGz3PdsJTzrBCiCkPcyeIVFxdjzpw5mDZtmsm4LjIvnue6wfNcN3ie6wbPc92wlPPMwoqIiIjITKymQSgRERGRpWNhRURERGQmLKyIiIiIzISFFdE9UigUWL16tdxpEBGRBWBhZSXi4uKgUqkQHR0tdyr10qhRo6BQKCq8kpKS5E6tXho1ahR7wNUBnufaY/yZ8eKLL1bYNm7cOCgUCowaNaruE6tHrPUcs7CyEt988w1eeeUV7Nq1C9euXbunY+n1ehgMBjNlVn9ERUUhJSXF5PXPCbyJiIwCAgLw888/o7CwUFpXVFSEZcuWITAw8J6OXVpaeq/p1Qu1eY5rCwsrK5CXl4fly5fjpZdeQnR0NJYuXSpt27FjBxQKBdatW4f27dvDzs4O3bt3x/Hjx6WYpUuXwtXVFWvWrEFoaCg0Gg0uXbokwyexbBqNBr6+viYvlUqF33//HZ07d4adnR2aNWuG2bNno6yszGTflJQUDBgwAPb29mjWrBl+/fVXmT6F9dm4cSN69uwJV1dXeHh44JFHHsG5c+ek7RcuXIBCocDKlSvRr18/ODg4oEOHDoiLi5Mxa+vTpEkTLFiwwGRdx44dMWvWLGlZoVDg66+/xuDBg+Hg4IAWLVpgzZo1dZuoFencuTMCAgKwcuVKad3KlSsRGBiITp06Seuq+nd8+fLl6NOnD+zs7PC///2vTj+LpTLXOX7ggQek2VSMrl+/DrVaja1bt5o1ZxZWVuCXX35BSEgIWrVqhWeeeQbffvst/tl+bPLkyZg/fz4OHToELy8vDBw40OQ3noKCAnz44Yf4+uuvceLECXh7e9f1x7BKu3fvxogRIzBhwgScPHkS//3vf7F06VK8//77JnFvv/02Hn/8cRw5cgTDhw/H0KFDcerUKZmyti75+fmYNGkS/vzzT2zduhVKpRKDBw+ucFX1rbfewv/93/8hISEBLVu2xLBhwyoUuHTvZs+ejSFDhuDo0aN4+OGHMXz4cGRmZsqdlsUaM2YMlixZIi1/++23GD16tElMVf+Ov/HGG5gwYQJOnTqFyMjIOsnfGpjjHD/33HNYtmyZNNcwAPz4449o1KgRHnjgAfMmLGvfd6qS+++/XyxYsEAIIURpaanw9PQU27dvF0L8PS3Qzz//LMVnZGQIe3t7sXz5ciGEEEuWLBEAREJCQp3nbi1GjhwpVCqVcHR0lF5PPPGEePDBB8W///1vk9gffvhB+Pn5ScsAxIsvvmgSExYWJl566aU6yd0ajRw5UgwaNKjSbdevXxcAxLFjx4QQQiQnJwsA4uuvv5ZiTpw4IQCIU6dO1UW6VuvW8xwUFCQ+/vhjk+0dOnQQM2fOlJYBiOnTp0vLeXl5AoDYsGFDHWRrXYznNj09XWg0GnHhwgVx4cIFYWdnJ65fvy4GDRokRo4cWem+t/s7bvw5T+XMeY4LCwuFm5ub9L0ohBDt27cXs2bNMnveNuYt08jcEhMTcfDgQaxatQoAYGNjg6eeegrffPMN+vbtK8WFh4dLf3Z3d0erVq1Mrpio1Wq0b9++zvK2Rv369cPnn38uLTs6OqJ9+/bYu3evyRUqvV6PoqIiFBQUwMHBAYDp+TcuGycXpzs7e/YsZsyYgQMHDuDGjRvSb5iXLl1C27Ztpbhb//76+fkBANLT0xESElK3Cddzt55nR0dHuLi4ID09XcaMLJuXl5c0REMIgejoaHh6eprEVPXveNeuXes0d2thjnNsZ2eHZ599Ft9++y2GDBmCw4cP4/jx47Vyq5uFlYX75ptvUFZWBn9/f2mdEAIajQaLFi2q8nHs7e2hUChqI8V6w9HREcHBwSbr8vLyMHv2bDz22GMV4u3s7OoqtXpt4MCBCAoKwldffQV/f38YDAa0bdsWJSUlJnG2trbSn41/l/kQRtUplcoKQwgqGyB963kGys81z/OdjRkzRhq/s3jx4grbq/p33NHRsU7ytUbmOMfPPfccOnbsiCtXrmDJkiV44IEHEBQUZPZcWVhZsLKyMnz//feYP38++vfvb7ItJiYGP/30k/Tb+v79+6UnJLKysnDmzBm0bt26znOubzp37ozExMQKBdc/7d+/HyNGjDBZvnVgJVUuIyMDiYmJ+Oqrr9CrVy8AwJ49e2TOqn7y8vJCSkqKtJyTk4Pk5GQZM6o/oqKiUFJSAoVCUWFsFP+Om4c5znG7du3QtWtXfPXVV1i2bFm1Lk5UBwsrCxYbG4usrCyMHTsWWq3WZNvjjz+Ob775BvPmzQMAvPPOO/Dw8ICPjw/eeusteHp6sn+NGcyYMQOPPPIIAgMD8cQTT0CpVOLIkSM4fvw43nvvPSluxYoV6Nq1K3r27In//e9/OHjwIL755hsZM7cObm5u8PDwwJdffgk/Pz9cunQJb7zxhtxp1UsPPPAAli5dioEDB8LV1RUzZsyASqWSO616QaVSSUMv/nlO+XfcPMx1jp977jmMHz8ejo6OGDx4cK3kyqcCLdg333yDiIiICkUVUF5Y/fnnnzh69CgA4IMPPsCECRPQpUsXpKamYu3atVCr1XWdcr0TGRmJ2NhY/PHHH7jvvvvQvXt3fPzxxxUuH8+ePRs///wz2rdvj++//x4//fQTQkNDZcra8hkMBtjY2ECpVOLnn39GfHw82rZti9dee036ZYHunfE8A8C0adPQp08fPPLII4iOjkZMTAyaN28uc4b1h4uLC1xcXCqs599x8zHHOR42bBhsbGwwbNiwWhvOoRD/vOlOVmXHjh3o168fsrKy4OrqKnc6RFUSFRWF4ODgWrsUT+V4nolMXbhwAc2bN8ehQ4fQuXPnWnkPXrEiojqTlZWF2NhY7NixAxEREXKnU2/xPBOZKi0tRWpqKqZPn47u3bvXWlEFcIwVEdWhMWPG4NChQ3j99dcxaNAgudOpt3ieiUzt3bsX/fr1Q8uWLWt9ZgzeCiQiIiIyE94KJCIiIjITFlZEREREZsLCioiIiMhMWFgRERERmQkLKyIimSkUCqxevVruNIjIDFhYEVGDNWrUKCgUCrz44osVto0bNw4KhQKjRo0y2/vNmjULHTt2NNvxiMjysLAiogYtICAAP//8MwoLC6V1RUVFWLZsmTSxORFRVbGwIqIGrXPnzggICMDKlSuldStXrkRgYCA6deokrSsuLsarr74Kb29v2NnZoWfPnjh06JC0fceOHVAoFNi6dSu6du0KBwcH3H///UhMTAQALF26FLNnz8aRI0egUCigUCiwdOlSaf8bN25g8ODBcHBwQIsWLbBmzZra//BEZHYsrIiowRszZgyWLFkiLX/77bcYPXq0ScyUKVPw22+/4bvvvsPhw4cRHByMyMhIZGZmmsS99dZbmD9/Pv7880/Y2NhgzJgxAICnnnoKr7/+Otq0aYOUlBSkpKTgqaeekvabPXs2hgwZgqNHj+Lhhx/G8OHDKxybiCwfCysiavCeeeYZ7NmzBxcvXsTFixexd+9ePPPMM9L2/Px8fP7555g3bx4GDBiA0NBQfPXVV7C3t8c333xjcqz3338fffr0QWhoKN544w3s27cPRUVFsLe3h5OTE2xsbODr6wtfX1/Y29tL+40aNQrDhg1DcHAw/v3vfyMvLw8HDx6ss3NARObBuQKJqMHz8vJCdHQ0li5dCiEEoqOj4enpKW0/d+4cSktL0aNHD2mdra0tunXrhlOnTpkcq3379tKf/fz8AADp6el3Ha91636Ojo5wcXFBenr6PX0uIqp7LKyIiFB+O3D8+PEAgMWLF9f4OLa2ttKfFQoFAMBgMFRrP+O+VdmPiCwLbwUSEQGIiopCSUkJSktLERkZabKtefPmUKvV2Lt3r7SutLQUhw4dQmhoaJXfQ61WQ6/Xmy1nIrI8vGJFRARApVJJt/VUKpXJNkdHR7z00kuYPHky3N3dERgYiLlz56KgoABjx46t8ns0adIEycnJSEhIQOPGjeHs7AyNRmPWz0FE8mJhRUR0k4uLy223ffDBBzAYDHj22WeRm5uLrl27YtOmTXBzc6vy8R9//HGsXLkS/fr1Q3Z2NpYsWWLWBqREJD+FEELInQQRERFRfcAxVkRERERmwsKKiIiIyExYWBERERGZCQsrIiIiIjNhYUVERERkJiysiIiIiMyEhRURERGRmbCwIiIiIjITFlZEREREZsLCioiIiMhMWFgRERERmQkLKyIiIiIz+X/tUZyhBW/5ZwAAAABJRU5ErkJggg==\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "## Key insights\n",
        "\n",
        "- Electronics generated the most sales accross all categories.\n",
        "\n",
        "- Western region maintained the highest average inventory levels.\n",
        "\n",
        "- Sales increased significantly during later months.\n",
        "\n",
        "- Furniture showed lower sales performance compared to other categories."
      ],
      "metadata": {
        "id": "30o56Z9eJ9gL"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## Recommendations\n",
        "\n",
        "- Increase inventory allocation for Electronics products.\n",
        "\n",
        "- Investigate low-performing Furniture category.\n",
        "\n",
        "- Prepare for monthly demand spikes\n",
        "\n",
        "- Optimize inventory distribution accross regions"
      ],
      "metadata": {
        "id": "QXKnWkJ-KigW"
      }
    }
  ]
}
    {
      "cell_type": "code",
      "source": [
        "import pandas as pd\n",
        "\n",
        "games = pd.read_csv(\"games.csv\")\n",
        "teams = pd.read_csv(\"teams.csv\")\n",
        "details = pd.read_csv(\"games_details.csv\")\n",
        "stats = pd.read_csv(\"nba_team_stats_00_to_23.csv\")"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "OhphF3C1MUzb",
        "outputId": "83224203-7bd3-43ad-e942-5e701f4774f6"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/tmp/ipykernel_974/1283371306.py:5: DtypeWarning: Columns (6) have mixed types. Specify dtype option on import or set low_memory=False.\n",
            "  details = pd.read_csv(\"games_details.csv\")\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "SOyD6H8XV4Gw",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "3410ba68-abfc-4787-ccb3-b54c82bd11bb"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "  GAME_DATE_EST   GAME_ID GAME_STATUS_TEXT  HOME_TEAM_ID  VISITOR_TEAM_ID  \\\n",
            "0    2022-12-22  22200477            Final    1610612740       1610612759   \n",
            "1    2022-12-22  22200478            Final    1610612762       1610612764   \n",
            "2    2022-12-21  22200466            Final    1610612739       1610612749   \n",
            "3    2022-12-21  22200467            Final    1610612755       1610612765   \n",
            "4    2022-12-21  22200468            Final    1610612737       1610612741   \n",
            "\n",
            "   SEASON  TEAM_ID_home  PTS_home  FG_PCT_home  FT_PCT_home  ...  AST_home  \\\n",
            "0    2022    1610612740     126.0        0.484        0.926  ...      25.0   \n",
            "1    2022    1610612762     120.0        0.488        0.952  ...      16.0   \n",
            "2    2022    1610612739     114.0        0.482        0.786  ...      22.0   \n",
            "3    2022    1610612755     113.0        0.441        0.909  ...      27.0   \n",
            "4    2022    1610612737     108.0        0.429        1.000  ...      22.0   \n",
            "\n",
            "   REB_home  TEAM_ID_away  PTS_away  FG_PCT_away  FT_PCT_away  FG3_PCT_away  \\\n",
            "0      46.0    1610612759     117.0        0.478        0.815         0.321   \n",
            "1      40.0    1610612764     112.0        0.561        0.765         0.333   \n",
            "2      37.0    1610612749     106.0        0.470        0.682         0.433   \n",
            "3      49.0    1610612765      93.0        0.392        0.735         0.261   \n",
            "4      47.0    1610612741     110.0        0.500        0.773         0.292   \n",
            "\n",
            "   AST_away  REB_away  HOME_TEAM_WINS  \n",
            "0      23.0      44.0               1  \n",
            "1      20.0      37.0               1  \n",
            "2      20.0      46.0               1  \n",
            "3      15.0      46.0               1  \n",
            "4      20.0      47.0               0  \n",
            "\n",
            "[5 rows x 21 columns]\n",
            "Index(['GAME_DATE_EST', 'GAME_ID', 'GAME_STATUS_TEXT', 'HOME_TEAM_ID',\n",
            "       'VISITOR_TEAM_ID', 'SEASON', 'TEAM_ID_home', 'PTS_home', 'FG_PCT_home',\n",
            "       'FT_PCT_home', 'FG3_PCT_home', 'AST_home', 'REB_home', 'TEAM_ID_away',\n",
            "       'PTS_away', 'FG_PCT_away', 'FT_PCT_away', 'FG3_PCT_away', 'AST_away',\n",
            "       'REB_away', 'HOME_TEAM_WINS'],\n",
            "      dtype='object')\n",
            "   LEAGUE_ID     TEAM_ID  MIN_YEAR  MAX_YEAR ABBREVIATION   NICKNAME  \\\n",
            "0          0  1610612737      1949      2019          ATL      Hawks   \n",
            "1          0  1610612738      1946      2019          BOS    Celtics   \n",
            "2          0  1610612740      2002      2019          NOP   Pelicans   \n",
            "3          0  1610612741      1966      2019          CHI      Bulls   \n",
            "4          0  1610612742      1980      2019          DAL  Mavericks   \n",
            "\n",
            "   YEARFOUNDED         CITY                     ARENA  ARENACAPACITY  \\\n",
            "0         1949      Atlanta          State Farm Arena        18729.0   \n",
            "1         1946       Boston                 TD Garden        18624.0   \n",
            "2         2002  New Orleans      Smoothie King Center            NaN   \n",
            "3         1966      Chicago             United Center        21711.0   \n",
            "4         1980       Dallas  American Airlines Center        19200.0   \n",
            "\n",
            "             OWNER  GENERALMANAGER      HEADCOACH DLEAGUEAFFILIATION  \n",
            "0     Tony Ressler  Travis Schlenk   Lloyd Pierce      Erie Bayhawks  \n",
            "1    Wyc Grousbeck     Danny Ainge   Brad Stevens    Maine Red Claws  \n",
            "2       Tom Benson  Trajan Langdon   Alvin Gentry       No Affiliate  \n",
            "3  Jerry Reinsdorf      Gar Forman     Jim Boylen   Windy City Bulls  \n",
            "4       Mark Cuban   Donnie Nelson  Rick Carlisle      Texas Legends  \n",
            "    GAME_ID     TEAM_ID TEAM_ABBREVIATION    TEAM_CITY  PLAYER_ID  \\\n",
            "0  22200477  1610612759               SAS  San Antonio    1629641   \n",
            "1  22200477  1610612759               SAS  San Antonio    1631110   \n",
            "2  22200477  1610612759               SAS  San Antonio    1627751   \n",
            "3  22200477  1610612759               SAS  San Antonio    1630170   \n",
            "4  22200477  1610612759               SAS  San Antonio    1630200   \n",
            "\n",
            "      PLAYER_NAME NICKNAME START_POSITION COMMENT    MIN  ...  OREB  DREB  \\\n",
            "0  Romeo Langford    Romeo              F     NaN  18:06  ...   1.0   1.0   \n",
            "1   Jeremy Sochan   Jeremy              F     NaN  31:01  ...   6.0   3.0   \n",
            "2    Jakob Poeltl    Jakob              C     NaN  21:42  ...   1.0   3.0   \n",
            "3   Devin Vassell    Devin              G     NaN  30:20  ...   0.0   9.0   \n",
            "4       Tre Jones      Tre              G     NaN  27:44  ...   0.0   2.0   \n",
            "\n",
            "   REB  AST  STL  BLK   TO   PF   PTS  PLUS_MINUS  \n",
            "0  2.0  0.0  1.0  0.0  2.0  5.0   2.0        -2.0  \n",
            "1  9.0  6.0  1.0  0.0  2.0  1.0  23.0       -14.0  \n",
            "2  4.0  1.0  1.0  0.0  2.0  4.0  13.0        -4.0  \n",
            "3  9.0  5.0  3.0  0.0  2.0  1.0  10.0       -18.0  \n",
            "4  2.0  3.0  0.0  0.0  2.0  2.0  19.0         0.0  \n",
            "\n",
            "[5 rows x 29 columns]\n"
          ]
        }
      ],
      "source": [
        "print(games.head())\n",
        "print(games.columns)\n",
        "\n",
        "print(teams.head())\n",
        "print(details.head())"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "K5hyGAvlWbVp"
      },
      "outputs": [],
      "source": [
        "games = games[[\n",
        "    \"GAME_ID\",\n",
        "    \"HOME_TEAM_ID\",\n",
        "    \"VISITOR_TEAM_ID\",\n",
        "    \"HOME_TEAM_WINS\"\n",
        "]]"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "DudIg0ArW8iI"
      },
      "outputs": [],
      "source": [
        "y = games[\"HOME_TEAM_WINS\"]"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "3IcPWrBrXG6O"
      },
      "outputs": [],
      "source": [
        "X = games[[\n",
        "    \"HOME_TEAM_ID\",\n",
        "    \"VISITOR_TEAM_ID\"\n",
        "]]"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "ds-4r6JBXVFk"
      },
      "outputs": [],
      "source": [
        "from sklearn.model_selection import train_test_split\n",
        "\n",
        "X_train, X_test, y_train, y_test = train_test_split(\n",
        "    X, y, test_size=0.2, random_state=42\n",
        "    )"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "KBvxJDJHYXqs",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 80
        },
        "outputId": "7e9299b8-ea30-4373-d37a-a18286705208"
      },
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "LogisticRegression()"
            ],
            "text/html": [
              "<style>#sk-container-id-2 {\n",
              "  /* Definition of color scheme common for light and dark mode */\n",
              "  --sklearn-color-text: #000;\n",
              "  --sklearn-color-text-muted: #666;\n",
              "  --sklearn-color-line: gray;\n",
              "  /* Definition of color scheme for unfitted estimators */\n",
              "  --sklearn-color-unfitted-level-0: #fff5e6;\n",
              "  --sklearn-color-unfitted-level-1: #f6e4d2;\n",
              "  --sklearn-color-unfitted-level-2: #ffe0b3;\n",
              "  --sklearn-color-unfitted-level-3: chocolate;\n",
              "  /* Definition of color scheme for fitted estimators */\n",
              "  --sklearn-color-fitted-level-0: #f0f8ff;\n",
              "  --sklearn-color-fitted-level-1: #d4ebff;\n",
              "  --sklearn-color-fitted-level-2: #b3dbfd;\n",
              "  --sklearn-color-fitted-level-3: cornflowerblue;\n",
              "\n",
              "  /* Specific color for light theme */\n",
              "  --sklearn-color-text-on-default-background: var(--sg-text-color, var(--theme-code-foreground, var(--jp-content-font-color1, black)));\n",
              "  --sklearn-color-background: var(--sg-background-color, var(--theme-background, var(--jp-layout-color0, white)));\n",
              "  --sklearn-color-border-box: var(--sg-text-color, var(--theme-code-foreground, var(--jp-content-font-color1, black)));\n",
              "  --sklearn-color-icon: #696969;\n",
              "\n",
              "  @media (prefers-color-scheme: dark) {\n",
              "    /* Redefinition of color scheme for dark theme */\n",
              "    --sklearn-color-text-on-default-background: var(--sg-text-color, var(--theme-code-foreground, var(--jp-content-font-color1, white)));\n",
              "    --sklearn-color-background: var(--sg-background-color, var(--theme-background, var(--jp-layout-color0, #111)));\n",
              "    --sklearn-color-border-box: var(--sg-text-color, var(--theme-code-foreground, var(--jp-content-font-color1, white)));\n",
              "    --sklearn-color-icon: #878787;\n",
              "  }\n",
              "}\n",
              "\n",
              "#sk-container-id-2 {\n",
              "  color: var(--sklearn-color-text);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 pre {\n",
              "  padding: 0;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 input.sk-hidden--visually {\n",
              "  border: 0;\n",
              "  clip: rect(1px 1px 1px 1px);\n",
              "  clip: rect(1px, 1px, 1px, 1px);\n",
              "  height: 1px;\n",
              "  margin: -1px;\n",
              "  overflow: hidden;\n",
              "  padding: 0;\n",
              "  position: absolute;\n",
              "  width: 1px;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-dashed-wrapped {\n",
              "  border: 1px dashed var(--sklearn-color-line);\n",
              "  margin: 0 0.4em 0.5em 0.4em;\n",
              "  box-sizing: border-box;\n",
              "  padding-bottom: 0.4em;\n",
              "  background-color: var(--sklearn-color-background);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-container {\n",
              "  /* jupyter's `normalize.less` sets `[hidden] { display: none; }`\n",
              "     but bootstrap.min.css set `[hidden] { display: none !important; }`\n",
              "     so we also need the `!important` here to be able to override the\n",
              "     default hidden behavior on the sphinx rendered scikit-learn.org.\n",
              "     See: https://github.com/scikit-learn/scikit-learn/issues/21755 */\n",
              "  display: inline-block !important;\n",
              "  position: relative;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-text-repr-fallback {\n",
              "  display: none;\n",
              "}\n",
              "\n",
              "div.sk-parallel-item,\n",
              "div.sk-serial,\n",
              "div.sk-item {\n",
              "  /* draw centered vertical line to link estimators */\n",
              "  background-image: linear-gradient(var(--sklearn-color-text-on-default-background), var(--sklearn-color-text-on-default-background));\n",
              "  background-size: 2px 100%;\n",
              "  background-repeat: no-repeat;\n",
              "  background-position: center center;\n",
              "}\n",
              "\n",
              "/* Parallel-specific style estimator block */\n",
              "\n",
              "#sk-container-id-2 div.sk-parallel-item::after {\n",
              "  content: \"\";\n",
              "  width: 100%;\n",
              "  border-bottom: 2px solid var(--sklearn-color-text-on-default-background);\n",
              "  flex-grow: 1;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-parallel {\n",
              "  display: flex;\n",
              "  align-items: stretch;\n",
              "  justify-content: center;\n",
              "  background-color: var(--sklearn-color-background);\n",
              "  position: relative;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-parallel-item {\n",
              "  display: flex;\n",
              "  flex-direction: column;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-parallel-item:first-child::after {\n",
              "  align-self: flex-end;\n",
              "  width: 50%;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-parallel-item:last-child::after {\n",
              "  align-self: flex-start;\n",
              "  width: 50%;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-parallel-item:only-child::after {\n",
              "  width: 0;\n",
              "}\n",
              "\n",
              "/* Serial-specific style estimator block */\n",
              "\n",
              "#sk-container-id-2 div.sk-serial {\n",
              "  display: flex;\n",
              "  flex-direction: column;\n",
              "  align-items: center;\n",
              "  background-color: var(--sklearn-color-background);\n",
              "  padding-right: 1em;\n",
              "  padding-left: 1em;\n",
              "}\n",
              "\n",
              "\n",
              "/* Toggleable style: style used for estimator/Pipeline/ColumnTransformer box that is\n",
              "clickable and can be expanded/collapsed.\n",
              "- Pipeline and ColumnTransformer use this feature and define the default style\n",
              "- Estimators will overwrite some part of the style using the `sk-estimator` class\n",
              "*/\n",
              "\n",
              "/* Pipeline and ColumnTransformer style (default) */\n",
              "\n",
              "#sk-container-id-2 div.sk-toggleable {\n",
              "  /* Default theme specific background. It is overwritten whether we have a\n",
              "  specific estimator or a Pipeline/ColumnTransformer */\n",
              "  background-color: var(--sklearn-color-background);\n",
              "}\n",
              "\n",
              "/* Toggleable label */\n",
              "#sk-container-id-2 label.sk-toggleable__label {\n",
              "  cursor: pointer;\n",
              "  display: flex;\n",
              "  width: 100%;\n",
              "  margin-bottom: 0;\n",
              "  padding: 0.5em;\n",
              "  box-sizing: border-box;\n",
              "  text-align: center;\n",
              "  align-items: start;\n",
              "  justify-content: space-between;\n",
              "  gap: 0.5em;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 label.sk-toggleable__label .caption {\n",
              "  font-size: 0.6rem;\n",
              "  font-weight: lighter;\n",
              "  color: var(--sklearn-color-text-muted);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 label.sk-toggleable__label-arrow:before {\n",
              "  /* Arrow on the left of the label */\n",
              "  content: \"▸\";\n",
              "  float: left;\n",
              "  margin-right: 0.25em;\n",
              "  color: var(--sklearn-color-icon);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 label.sk-toggleable__label-arrow:hover:before {\n",
              "  color: var(--sklearn-color-text);\n",
              "}\n",
              "\n",
              "/* Toggleable content - dropdown */\n",
              "\n",
              "#sk-container-id-2 div.sk-toggleable__content {\n",
              "  max-height: 0;\n",
              "  max-width: 0;\n",
              "  overflow: hidden;\n",
              "  text-align: left;\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-0);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-toggleable__content.fitted {\n",
              "  /* fitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-0);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-toggleable__content pre {\n",
              "  margin: 0.2em;\n",
              "  border-radius: 0.25em;\n",
              "  color: var(--sklearn-color-text);\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-0);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-toggleable__content.fitted pre {\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-0);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 input.sk-toggleable__control:checked~div.sk-toggleable__content {\n",
              "  /* Expand drop-down */\n",
              "  max-height: 200px;\n",
              "  max-width: 100%;\n",
              "  overflow: auto;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 input.sk-toggleable__control:checked~label.sk-toggleable__label-arrow:before {\n",
              "  content: \"▾\";\n",
              "}\n",
              "\n",
              "/* Pipeline/ColumnTransformer-specific style */\n",
              "\n",
              "#sk-container-id-2 div.sk-label input.sk-toggleable__control:checked~label.sk-toggleable__label {\n",
              "  color: var(--sklearn-color-text);\n",
              "  background-color: var(--sklearn-color-unfitted-level-2);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-label.fitted input.sk-toggleable__control:checked~label.sk-toggleable__label {\n",
              "  background-color: var(--sklearn-color-fitted-level-2);\n",
              "}\n",
              "\n",
              "/* Estimator-specific style */\n",
              "\n",
              "/* Colorize estimator box */\n",
              "#sk-container-id-2 div.sk-estimator input.sk-toggleable__control:checked~label.sk-toggleable__label {\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-2);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-estimator.fitted input.sk-toggleable__control:checked~label.sk-toggleable__label {\n",
              "  /* fitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-2);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-label label.sk-toggleable__label,\n",
              "#sk-container-id-2 div.sk-label label {\n",
              "  /* The background is the default theme color */\n",
              "  color: var(--sklearn-color-text-on-default-background);\n",
              "}\n",
              "\n",
              "/* On hover, darken the color of the background */\n",
              "#sk-container-id-2 div.sk-label:hover label.sk-toggleable__label {\n",
              "  color: var(--sklearn-color-text);\n",
              "  background-color: var(--sklearn-color-unfitted-level-2);\n",
              "}\n",
              "\n",
              "/* Label box, darken color on hover, fitted */\n",
              "#sk-container-id-2 div.sk-label.fitted:hover label.sk-toggleable__label.fitted {\n",
              "  color: var(--sklearn-color-text);\n",
              "  background-color: var(--sklearn-color-fitted-level-2);\n",
              "}\n",
              "\n",
              "/* Estimator label */\n",
              "\n",
              "#sk-container-id-2 div.sk-label label {\n",
              "  font-family: monospace;\n",
              "  font-weight: bold;\n",
              "  display: inline-block;\n",
              "  line-height: 1.2em;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-label-container {\n",
              "  text-align: center;\n",
              "}\n",
              "\n",
              "/* Estimator-specific */\n",
              "#sk-container-id-2 div.sk-estimator {\n",
              "  font-family: monospace;\n",
              "  border: 1px dotted var(--sklearn-color-border-box);\n",
              "  border-radius: 0.25em;\n",
              "  box-sizing: border-box;\n",
              "  margin-bottom: 0.5em;\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-0);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-estimator.fitted {\n",
              "  /* fitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-0);\n",
              "}\n",
              "\n",
              "/* on hover */\n",
              "#sk-container-id-2 div.sk-estimator:hover {\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-2);\n",
              "}\n",
              "\n",
              "#sk-container-id-2 div.sk-estimator.fitted:hover {\n",
              "  /* fitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-2);\n",
              "}\n",
              "\n",
              "/* Specification for estimator info (e.g. \"i\" and \"?\") */\n",
              "\n",
              "/* Common style for \"i\" and \"?\" */\n",
              "\n",
              ".sk-estimator-doc-link,\n",
              "a:link.sk-estimator-doc-link,\n",
              "a:visited.sk-estimator-doc-link {\n",
              "  float: right;\n",
              "  font-size: smaller;\n",
              "  line-height: 1em;\n",
              "  font-family: monospace;\n",
              "  background-color: var(--sklearn-color-background);\n",
              "  border-radius: 1em;\n",
              "  height: 1em;\n",
              "  width: 1em;\n",
              "  text-decoration: none !important;\n",
              "  margin-left: 0.5em;\n",
              "  text-align: center;\n",
              "  /* unfitted */\n",
              "  border: var(--sklearn-color-unfitted-level-1) 1pt solid;\n",
              "  color: var(--sklearn-color-unfitted-level-1);\n",
              "}\n",
              "\n",
              ".sk-estimator-doc-link.fitted,\n",
              "a:link.sk-estimator-doc-link.fitted,\n",
              "a:visited.sk-estimator-doc-link.fitted {\n",
              "  /* fitted */\n",
              "  border: var(--sklearn-color-fitted-level-1) 1pt solid;\n",
              "  color: var(--sklearn-color-fitted-level-1);\n",
              "}\n",
              "\n",
              "/* On hover */\n",
              "div.sk-estimator:hover .sk-estimator-doc-link:hover,\n",
              ".sk-estimator-doc-link:hover,\n",
              "div.sk-label-container:hover .sk-estimator-doc-link:hover,\n",
              ".sk-estimator-doc-link:hover {\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-3);\n",
              "  color: var(--sklearn-color-background);\n",
              "  text-decoration: none;\n",
              "}\n",
              "\n",
              "div.sk-estimator.fitted:hover .sk-estimator-doc-link.fitted:hover,\n",
              ".sk-estimator-doc-link.fitted:hover,\n",
              "div.sk-label-container:hover .sk-estimator-doc-link.fitted:hover,\n",
              ".sk-estimator-doc-link.fitted:hover {\n",
              "  /* fitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-3);\n",
              "  color: var(--sklearn-color-background);\n",
              "  text-decoration: none;\n",
              "}\n",
              "\n",
              "/* Span, style for the box shown on hovering the info icon */\n",
              ".sk-estimator-doc-link span {\n",
              "  display: none;\n",
              "  z-index: 9999;\n",
              "  position: relative;\n",
              "  font-weight: normal;\n",
              "  right: .2ex;\n",
              "  padding: .5ex;\n",
              "  margin: .5ex;\n",
              "  width: min-content;\n",
              "  min-width: 20ex;\n",
              "  max-width: 50ex;\n",
              "  color: var(--sklearn-color-text);\n",
              "  box-shadow: 2pt 2pt 4pt #999;\n",
              "  /* unfitted */\n",
              "  background: var(--sklearn-color-unfitted-level-0);\n",
              "  border: .5pt solid var(--sklearn-color-unfitted-level-3);\n",
              "}\n",
              "\n",
              ".sk-estimator-doc-link.fitted span {\n",
              "  /* fitted */\n",
              "  background: var(--sklearn-color-fitted-level-0);\n",
              "  border: var(--sklearn-color-fitted-level-3);\n",
              "}\n",
              "\n",
              ".sk-estimator-doc-link:hover span {\n",
              "  display: block;\n",
              "}\n",
              "\n",
              "/* \"?\"-specific style due to the `<a>` HTML tag */\n",
              "\n",
              "#sk-container-id-2 a.estimator_doc_link {\n",
              "  float: right;\n",
              "  font-size: 1rem;\n",
              "  line-height: 1em;\n",
              "  font-family: monospace;\n",
              "  background-color: var(--sklearn-color-background);\n",
              "  border-radius: 1rem;\n",
              "  height: 1rem;\n",
              "  width: 1rem;\n",
              "  text-decoration: none;\n",
              "  /* unfitted */\n",
              "  color: var(--sklearn-color-unfitted-level-1);\n",
              "  border: var(--sklearn-color-unfitted-level-1) 1pt solid;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 a.estimator_doc_link.fitted {\n",
              "  /* fitted */\n",
              "  border: var(--sklearn-color-fitted-level-1) 1pt solid;\n",
              "  color: var(--sklearn-color-fitted-level-1);\n",
              "}\n",
              "\n",
              "/* On hover */\n",
              "#sk-container-id-2 a.estimator_doc_link:hover {\n",
              "  /* unfitted */\n",
              "  background-color: var(--sklearn-color-unfitted-level-3);\n",
              "  color: var(--sklearn-color-background);\n",
              "  text-decoration: none;\n",
              "}\n",
              "\n",
              "#sk-container-id-2 a.estimator_doc_link.fitted:hover {\n",
              "  /* fitted */\n",
              "  background-color: var(--sklearn-color-fitted-level-3);\n",
              "}\n",
              "</style><div id=\"sk-container-id-2\" class=\"sk-top-container\"><div class=\"sk-text-repr-fallback\"><pre>LogisticRegression()</pre><b>In a Jupyter environment, please rerun this cell to show the HTML representation or trust the notebook. <br />On GitHub, the HTML representation is unable to render, please try loading this page with nbviewer.org.</b></div><div class=\"sk-container\" hidden><div class=\"sk-item\"><div class=\"sk-estimator fitted sk-toggleable\"><input class=\"sk-toggleable__control sk-hidden--visually\" id=\"sk-estimator-id-2\" type=\"checkbox\" checked><label for=\"sk-estimator-id-2\" class=\"sk-toggleable__label fitted sk-toggleable__label-arrow\"><div><div>LogisticRegression</div></div><div><a class=\"sk-estimator-doc-link fitted\" rel=\"noreferrer\" target=\"_blank\" href=\"https://scikit-learn.org/1.6/modules/generated/sklearn.linear_model.LogisticRegression.html\">?<span>Documentation for LogisticRegression</span></a><span class=\"sk-estimator-doc-link fitted\">i<span>Fitted</span></span></div></label><div class=\"sk-toggleable__content fitted\"><pre>LogisticRegression()</pre></div> </div></div></div></div>"
            ]
          },
          "metadata": {},
          "execution_count": 76
        }
      ],
      "source": [
        "from sklearn.linear_model import LogisticRegression\n",
        "\n",
        "model = LogisticRegression()\n",
        "model.fit(X_train, y_train)"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "siQxXGj-YqeJ",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "48431692-5149-4259-b8f4-a35b229e1310"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "              precision    recall  f1-score   support\n",
            "\n",
            "           0       0.00      0.00      0.00      2201\n",
            "           1       0.59      1.00      0.74      3130\n",
            "\n",
            "    accuracy                           0.59      5331\n",
            "   macro avg       0.29      0.50      0.37      5331\n",
            "weighted avg       0.34      0.59      0.43      5331\n",
            "\n"
          ]
        },
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/usr/local/lib/python3.12/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.\n",
            "  _warn_prf(average, modifier, f\"{metric.capitalize()} is\", len(result))\n",
            "/usr/local/lib/python3.12/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.\n",
            "  _warn_prf(average, modifier, f\"{metric.capitalize()} is\", len(result))\n",
            "/usr/local/lib/python3.12/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.\n",
            "  _warn_prf(average, modifier, f\"{metric.capitalize()} is\", len(result))\n"
          ]
        }
      ],
      "source": [
        "from sklearn.metrics import classification_report\n",
        "\n",
        "y_pred = model.predict(X_test)\n",
        "print(classification_report(y_test, y_pred))"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "8C-QNumTaIxj",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "30625a40-85c4-4992-a551-a0ed3af86ac9"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "RF Accuracy: 0.5871318701932096\n"
          ]
        }
      ],
      "source": [
        "from sklearn.ensemble import RandomForestClassifier\n",
        "\n",
        "rf = RandomForestClassifier(n_estimators=100, random_state=42)\n",
        "rf.fit(X_train, y_train)\n",
        "\n",
        "print(\"RF Accuracy:\", rf.score(X_test, y_test))\n"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "oDIwkcg9a-V5",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "41be321a-3af2-45de-eecf-5f4c2592a02d"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Logistic: 0.5871318701932096\n",
            "Random Forest: 0.5871318701932096\n"
          ]
        }
      ],
      "source": [
        "print(\"Logistic:\", model.score(X_test, y_test))\n",
        "print(\"Random Forest:\", rf.score(X_test, y_test))"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "8CLs_kDMc1CR",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "ba7f7081-d1f2-4b24-fe8d-e47b26c9c801"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Index(['GAME_ID', 'HOME_TEAM_ID', 'VISITOR_TEAM_ID', 'HOME_TEAM_WINS'], dtype='object')\n"
          ]
        }
      ],
      "source": [
        "games.columns = games.columns.str.upper()\n",
        "print(games.columns)"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "qZv6j8jPeNDC",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "7421d7e8-85e6-4d80-8f5c-c4f730ebcbb7"
      },
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "[]"
            ]
          },
          "metadata": {},
          "execution_count": 81
        }
      ],
      "source": [
        "[col for col in games.columns if \"PTS\" in col.upper()]"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "J3XVpOIXbrZM"
      },
      "outputs": [],
      "source": [
        "X = games[[\n",
        "    \"HOME_TEAM_ID\",\n",
        "    \"VISITOR_TEAM_ID\",\n",
        "    ]]\n",
        "\n",
        "y = games[\"HOME_TEAM_WINS\"]"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "KpFgr38CfbQf",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "18506cc3-98da-46d7-a106-1d17af1521cf"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Accuracy: 0.5871318701932096\n"
          ]
        }
      ],
      "source": [
        "accuracy = model.score(X_test, y_test)\n",
        "print(\"Accuracy:\", accuracy)"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "LSXhg3E-f73w",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "72b87a0a-b7d6-4cf4-edd2-e69733b2932e"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "[1]\n"
          ]
        },
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/usr/local/lib/python3.12/dist-packages/sklearn/utils/validation.py:2739: UserWarning: X does not have valid feature names, but LogisticRegression was fitted with feature names\n",
            "  warnings.warn(\n"
          ]
        }
      ],
      "source": [
        "sample = [[0,1]] # encoded team IDs\n",
        "print(model.predict(sample))"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "lXbw-VJvg8n3",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "8bc91142-6251-4671-eb99-0dea045deb03"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "[1]\n"
          ]
        }
      ],
      "source": [
        "sample = X_test.iloc[0:1]\n",
        "print(model.predict(sample))"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "8aa8ba9b"
      },
      "outputs": [],
      "source": [
        "# Calculate wins for each team\n",
        "home_team_wins_count = games[games['HOME_TEAM_WINS'] == 1].groupby('HOME_TEAM_ID').size().reset_index(name='WINS')\n",
        "home_team_wins_count.rename(columns={'HOME_TEAM_ID': 'TEAM_ID'}, inplace=True)\n",
        "\n",
        "visitor_team_wins_count = games[games['HOME_TEAM_WINS'] == 0].groupby('VISITOR_TEAM_ID').size().reset_index(name='WINS')\n",
        "visitor_team_wins_count.rename(columns={'VISITOR_TEAM_ID': 'TEAM_ID'}, inplace=True)\n",
        "\n",
        "all_teams_wins = pd.concat([home_team_wins_count, visitor_team_wins_count])\n",
        "total_wins_per_team = all_teams_wins.groupby('TEAM_ID')['WINS'].sum().reset_index()"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "edee27f8"
      },
      "outputs": [],
      "source": [
        "# Calculate total games played by each team\n",
        "home_games_count = games.groupby('HOME_TEAM_ID').size().reset_index(name='GAMES_PLAYED')\n",
        "home_games_count.rename(columns={'HOME_TEAM_ID': 'TEAM_ID'}, inplace=True)\n",
        "\n",
        "visitor_games_count = games.groupby('VISITOR_TEAM_ID').size().reset_index(name='GAMES_PLAYED')\n",
        "visitor_games_count.rename(columns={'VISITOR_TEAM_ID': 'TEAM_ID'}, inplace=True)\n",
        "\n",
        "all_teams_games = pd.concat([home_games_count, visitor_games_count])\n",
        "total_games_per_team = all_teams_games.groupby('TEAM_ID')['GAMES_PLAYED'].sum().reset_index()"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "2d782709"
      },
      "outputs": [],
      "source": [
        "# Merge total wins and total games played\n",
        "team_stats = pd.merge(total_games_per_team, total_wins_per_team, on='TEAM_ID', how='left')\n",
        "team_stats['WINS'] = team_stats['WINS'].fillna(0).astype(int) # Handle teams with 0 wins if any\n",
        "\n",
        "# Calculate win percentage\n",
        "team_stats['WIN_PERCENTAGE'] = (team_stats['WINS'] / team_stats['GAMES_PLAYED']) * 100"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "a49f7d05",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 415
        },
        "outputId": "697ae548-cce1-472c-a4b4-ba20c1814a1b"
      },
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "       TEAM_ID  GAMES_PLAYED  WINS  WIN_PERCENTAGE   NICKNAME\n",
              "22  1610612759          1873  1186       63.320876      Spurs\n",
              "5   1610612742          1822  1040       57.080132  Mavericks\n",
              "11  1610612748          1898  1076       56.691254       Heat\n",
              "7   1610612744          1823  1024       56.171146   Warriors\n",
              "1   1610612738          1888  1059       56.091102    Celtics"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-0e8ed6a8-01af-4e96-9803-b64a40023d7d\" class=\"colab-df-container\">\n",
              "    <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>TEAM_ID</th>\n",
              "      <th>GAMES_PLAYED</th>\n",
              "      <th>WINS</th>\n",
              "      <th>WIN_PERCENTAGE</th>\n",
              "      <th>NICKNAME</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>22</th>\n",
              "      <td>1610612759</td>\n",
              "      <td>1873</td>\n",
              "      <td>1186</td>\n",
              "      <td>63.320876</td>\n",
              "      <td>Spurs</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>5</th>\n",
              "      <td>1610612742</td>\n",
              "      <td>1822</td>\n",
              "      <td>1040</td>\n",
              "      <td>57.080132</td>\n",
              "      <td>Mavericks</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>11</th>\n",
              "      <td>1610612748</td>\n",
              "      <td>1898</td>\n",
              "      <td>1076</td>\n",
              "      <td>56.691254</td>\n",
              "      <td>Heat</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>7</th>\n",
              "      <td>1610612744</td>\n",
              "      <td>1823</td>\n",
              "      <td>1024</td>\n",
              "      <td>56.171146</td>\n",
              "      <td>Warriors</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>1610612738</td>\n",
              "      <td>1888</td>\n",
              "      <td>1059</td>\n",
              "      <td>56.091102</td>\n",
              "      <td>Celtics</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>\n",
              "    <div class=\"colab-df-buttons\">\n",
              "\n",
              "  <div class=\"colab-df-container\">\n",
              "    <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-0e8ed6a8-01af-4e96-9803-b64a40023d7d')\"\n",
              "            title=\"Convert this dataframe to an interactive table.\"\n",
              "            style=\"display:none;\">\n",
              "\n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\">\n",
              "    <path d=\"M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z\"/>\n",
              "  </svg>\n",
              "    </button>\n",
              "\n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    .colab-df-buttons div {\n",
              "      margin-bottom: 4px;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "    <script>\n",
              "      const buttonEl =\n",
              "        document.querySelector('#df-0e8ed6a8-01af-4e96-9803-b64a40023d7d button.colab-df-convert');\n",
              "      buttonEl.style.display =\n",
              "        google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "      async function convertToInteractive(key) {\n",
              "        const element = document.querySelector('#df-0e8ed6a8-01af-4e96-9803-b64a40023d7d');\n",
              "        const dataTable =\n",
              "          await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                    [key], {});\n",
              "        if (!dataTable) return;\n",
              "\n",
              "        const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "          '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "          + ' to learn more about interactive tables.';\n",
              "        element.innerHTML = '';\n",
              "        dataTable['output_type'] = 'display_data';\n",
              "        await google.colab.output.renderOutput(dataTable, element);\n",
              "        const docLink = document.createElement('div');\n",
              "        docLink.innerHTML = docLinkHtml;\n",
              "        element.appendChild(docLink);\n",
              "      }\n",
              "    </script>\n",
              "  </div>\n",
              "\n",
              "\n",
              "    </div>\n",
              "  </div>\n"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "dataframe",
              "summary": "{\n  \"name\": \"display(team_stats\",\n  \"rows\": 5,\n  \"fields\": [\n    {\n      \"column\": \"TEAM_ID\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 8,\n        \"min\": 1610612738,\n        \"max\": 1610612759,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          1610612742,\n          1610612738,\n          1610612748\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"GAMES_PLAYED\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 36,\n        \"min\": 1822,\n        \"max\": 1898,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          1822,\n          1888,\n          1898\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"WINS\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 64,\n        \"min\": 1024,\n        \"max\": 1186,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          1040,\n          1059,\n          1076\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"WIN_PERCENTAGE\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 3.0731074424632214,\n        \"min\": 56.09110169491526,\n        \"max\": 63.32087560064068,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          57.0801317233809,\n          56.09110169491526,\n          56.69125395152792\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"NICKNAME\",\n      \"properties\": {\n        \"dtype\": \"string\",\n        \"num_unique_values\": 5,\n        \"samples\": [\n          \"Mavericks\",\n          \"Celtics\",\n          \"Heat\"\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    }\n  ]\n}"
            }
          },
          "metadata": {}
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "       TEAM_ID  GAMES_PLAYED  WINS  WIN_PERCENTAGE      NICKNAME\n",
              "27  1610612764          1747   755       43.216943       Wizards\n",
              "21  1610612758          1698   703       41.401649         Kings\n",
              "15  1610612752          1688   688       40.758294        Knicks\n",
              "13  1610612750          1695   686       40.471976  Timberwolves\n",
              "29  1610612766          1603   640       39.925140       Hornets"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-b539eb9f-c2ee-43dc-8076-6f48c199e081\" class=\"colab-df-container\">\n",
              "    <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>TEAM_ID</th>\n",
              "      <th>GAMES_PLAYED</th>\n",
              "      <th>WINS</th>\n",
              "      <th>WIN_PERCENTAGE</th>\n",
              "      <th>NICKNAME</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>27</th>\n",
              "      <td>1610612764</td>\n",
              "      <td>1747</td>\n",
              "      <td>755</td>\n",
              "      <td>43.216943</td>\n",
              "      <td>Wizards</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>21</th>\n",
              "      <td>1610612758</td>\n",
              "      <td>1698</td>\n",
              "      <td>703</td>\n",
              "      <td>41.401649</td>\n",
              "      <td>Kings</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>15</th>\n",
              "      <td>1610612752</td>\n",
              "      <td>1688</td>\n",
              "      <td>688</td>\n",
              "      <td>40.758294</td>\n",
              "      <td>Knicks</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>13</th>\n",
              "      <td>1610612750</td>\n",
              "      <td>1695</td>\n",
              "      <td>686</td>\n",
              "      <td>40.471976</td>\n",
              "      <td>Timberwolves</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>29</th>\n",
              "      <td>1610612766</td>\n",
              "      <td>1603</td>\n",
              "      <td>640</td>\n",
              "      <td>39.925140</td>\n",
              "      <td>Hornets</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>\n",
              "    <div class=\"colab-df-buttons\">\n",
              "\n",
              "  <div class=\"colab-df-container\">\n",
              "    <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-b539eb9f-c2ee-43dc-8076-6f48c199e081')\"\n",
              "            title=\"Convert this dataframe to an interactive table.\"\n",
              "            style=\"display:none;\">\n",
              "\n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\">\n",
              "    <path d=\"M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z\"/>\n",
              "  </svg>\n",
              "    </button>\n",
              "\n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    .colab-df-buttons div {\n",
              "      margin-bottom: 4px;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "    <script>\n",
              "      const buttonEl =\n",
              "        document.querySelector('#df-b539eb9f-c2ee-43dc-8076-6f48c199e081 button.colab-df-convert');\n",
              "      buttonEl.style.display =\n",
              "        google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "      async function convertToInteractive(key) {\n",
              "        const element = document.querySelector('#df-b539eb9f-c2ee-43dc-8076-6f48c199e081');\n",
              "        const dataTable =\n",
              "          await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                    [key], {});\n",
              "        if (!dataTable) return;\n",
              "\n",
              "        const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "          '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "          + ' to learn more about interactive tables.';\n",
              "        element.innerHTML = '';\n",
              "        dataTable['output_type'] = 'display_data';\n",
              "        await google.colab.output.renderOutput(dataTable, element);\n",
              "        const docLink = document.createElement('div');\n",
              "        docLink.innerHTML = docLinkHtml;\n",
              "        element.appendChild(docLink);\n",
              "      }\n",
              "    </script>\n",
              "  </div>\n",
              "\n",
              "\n",
              "    </div>\n",
              "  </div>\n"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "dataframe",
              "summary": "{\n  \"name\": \"display(team_stats\",\n  \"rows\": 5,\n  \"fields\": [\n    {\n      \"column\": \"TEAM_ID\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 7,\n        \"min\": 1610612750,\n        \"max\": 1610612766,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          1610612758,\n          1610612766,\n          1610612752\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"GAMES_PLAYED\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 52,\n        \"min\": 1603,\n        \"max\": 1747,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          1698,\n          1603,\n          1688\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"WINS\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 41,\n        \"min\": 640,\n        \"max\": 755,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          703,\n          640,\n          688\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"WIN_PERCENTAGE\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 1.2697339855507321,\n        \"min\": 39.92514036182159,\n        \"max\": 43.2169433314253,\n        \"num_unique_values\": 5,\n        \"samples\": [\n          41.40164899882215,\n          39.92514036182159,\n          40.758293838862556\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"NICKNAME\",\n      \"properties\": {\n        \"dtype\": \"string\",\n        \"num_unique_values\": 5,\n        \"samples\": [\n          \"Kings\",\n          \"Hornets\",\n          \"Knicks\"\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    }\n  ]\n}"
            }
          },
          "metadata": {}
        }
      ],
      "source": [
        "# Merge with teams dataframe to get team names\n",
        "team_names = teams[['TEAM_ID', 'NICKNAME']]\n",
        "team_stats = pd.merge(team_stats, team_names, on='TEAM_ID', how='left')\n",
        "\n",
        "# Sort by win percentage and display\n",
        "team_stats = team_stats.sort_values(by='WIN_PERCENTAGE', ascending=False)\n",
        "display(team_stats.head())\n",
        "display(team_stats.tail())"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "print(games.shape)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "z6Nzuu7aN5UH",
        "outputId": "e51f2b39-c5f7-4c5d-c369-c092eed4f421"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "(26651, 4)\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "print(games.info())"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "cghZ1K7rOCPV",
        "outputId": "f280c374-b6cd-453c-f588-7a995de6eee3"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "<class 'pandas.core.frame.DataFrame'>\n",
            "RangeIndex: 26651 entries, 0 to 26650\n",
            "Data columns (total 4 columns):\n",
            " #   Column           Non-Null Count  Dtype\n",
            "---  ------           --------------  -----\n",
            " 0   GAME_ID          26651 non-null  int64\n",
            " 1   HOME_TEAM_ID     26651 non-null  int64\n",
            " 2   VISITOR_TEAM_ID  26651 non-null  int64\n",
            " 3   HOME_TEAM_WINS   26651 non-null  int64\n",
            "dtypes: int64(4)\n",
            "memory usage: 833.0 KB\n",
            "None\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "print(games.describe())"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "2twdREj6OKbC",
        "outputId": "7366f1cb-3cb8-4928-8e1e-2744e1e77434"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "            GAME_ID  HOME_TEAM_ID  VISITOR_TEAM_ID  HOME_TEAM_WINS\n",
            "count  2.665100e+04  2.665100e+04     2.665100e+04    26651.000000\n",
            "mean   2.175487e+07  1.610613e+09     1.610613e+09        0.587032\n",
            "std    5.570189e+06  8.638670e+00     8.659299e+00        0.492376\n",
            "min    1.030000e+07  1.610613e+09     1.610613e+09        0.000000\n",
            "25%    2.070001e+07  1.610613e+09     1.610613e+09        0.000000\n",
            "50%    2.120076e+07  1.610613e+09     1.610613e+09        1.000000\n",
            "75%    2.180005e+07  1.610613e+09     1.610613e+09        1.000000\n",
            "max    5.210021e+07  1.610613e+09     1.610613e+09        1.000000\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "print(games[\"HOME_TEAM_ID\"].head())"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "bvTL6eLMORGT",
        "outputId": "8bcfab65-fe37-4425-df0d-9268812dbe38"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "0    1610612740\n",
            "1    1610612762\n",
            "2    1610612739\n",
            "3    1610612755\n",
            "4    1610612737\n",
            "Name: HOME_TEAM_ID, dtype: int64\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "import pandas as pd\n",
        "\n",
        "df = pd.read_csv(\"games_details.csv\")\n",
        "print(df.head())"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "KnPhhWJGPD13",
        "outputId": "174d470a-1d41-40f7-8b1e-2203f9eb0efa"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/tmp/ipykernel_974/1010580061.py:3: DtypeWarning: Columns (6) have mixed types. Specify dtype option on import or set low_memory=False.\n",
            "  df = pd.read_csv(\"games_details.csv\")\n"
          ]
        },
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "    GAME_ID     TEAM_ID TEAM_ABBREVIATION    TEAM_CITY  PLAYER_ID  \\\n",
            "0  22200477  1610612759               SAS  San Antonio    1629641   \n",
            "1  22200477  1610612759               SAS  San Antonio    1631110   \n",
            "2  22200477  1610612759               SAS  San Antonio    1627751   \n",
            "3  22200477  1610612759               SAS  San Antonio    1630170   \n",
            "4  22200477  1610612759               SAS  San Antonio    1630200   \n",
            "\n",
            "      PLAYER_NAME NICKNAME START_POSITION COMMENT    MIN  ...  OREB  DREB  \\\n",
            "0  Romeo Langford    Romeo              F     NaN  18:06  ...   1.0   1.0   \n",
            "1   Jeremy Sochan   Jeremy              F     NaN  31:01  ...   6.0   3.0   \n",
            "2    Jakob Poeltl    Jakob              C     NaN  21:42  ...   1.0   3.0   \n",
            "3   Devin Vassell    Devin              G     NaN  30:20  ...   0.0   9.0   \n",
            "4       Tre Jones      Tre              G     NaN  27:44  ...   0.0   2.0   \n",
            "\n",
            "   REB  AST  STL  BLK   TO   PF   PTS  PLUS_MINUS  \n",
            "0  2.0  0.0  1.0  0.0  2.0  5.0   2.0        -2.0  \n",
            "1  9.0  6.0  1.0  0.0  2.0  1.0  23.0       -14.0  \n",
            "2  4.0  1.0  1.0  0.0  2.0  4.0  13.0        -4.0  \n",
            "3  9.0  5.0  3.0  0.0  2.0  1.0  10.0       -18.0  \n",
            "4  2.0  3.0  0.0  0.0  2.0  2.0  19.0         0.0  \n",
            "\n",
            "[5 rows x 29 columns]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "print(df.columns)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "WPveflqEQ-uY",
        "outputId": "c979417d-c653-4143-aa69-b76a97cc3599"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Index(['GAME_ID', 'TEAM_ID', 'TEAM_ABBREVIATION', 'TEAM_CITY', 'PLAYER_ID',\n",
            "       'PLAYER_NAME', 'NICKNAME', 'START_POSITION', 'COMMENT', 'MIN', 'FGM',\n",
            "       'FGA', 'FG_PCT', 'FG3M', 'FG3A', 'FG3_PCT', 'FTM', 'FTA', 'FT_PCT',\n",
            "       'OREB', 'DREB', 'REB', 'AST', 'STL', 'BLK', 'TO', 'PF', 'PTS',\n",
            "       'PLUS_MINUS'],\n",
            "      dtype='object')\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df.columns = df.columns.str.strip()"
      ],
      "metadata": {
        "id": "ri530Xk1mAA9"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "df.info()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "RpZtO8W5qq_K",
        "outputId": "faed4c8c-63c2-4fbf-c07c-8785199f1ccf"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "<class 'pandas.core.frame.DataFrame'>\n",
            "RangeIndex: 668628 entries, 0 to 668627\n",
            "Data columns (total 29 columns):\n",
            " #   Column             Non-Null Count   Dtype  \n",
            "---  ------             --------------   -----  \n",
            " 0   GAME_ID            668628 non-null  int64  \n",
            " 1   TEAM_ID            668628 non-null  int64  \n",
            " 2   TEAM_ABBREVIATION  668628 non-null  object \n",
            " 3   TEAM_CITY          668628 non-null  object \n",
            " 4   PLAYER_ID          668628 non-null  int64  \n",
            " 5   PLAYER_NAME        668628 non-null  object \n",
            " 6   NICKNAME           53037 non-null   object \n",
            " 7   START_POSITION     255765 non-null  object \n",
            " 8   COMMENT            109689 non-null  object \n",
            " 9   MIN                558938 non-null  object \n",
            " 10  FGM                558938 non-null  float64\n",
            " 11  FGA                558938 non-null  float64\n",
            " 12  FG_PCT             558938 non-null  float64\n",
            " 13  FG3M               558938 non-null  float64\n",
            " 14  FG3A               558938 non-null  float64\n",
            " 15  FG3_PCT            558938 non-null  float64\n",
            " 16  FTM                558938 non-null  float64\n",
            " 17  FTA                558938 non-null  float64\n",
            " 18  FT_PCT             558938 non-null  float64\n",
            " 19  OREB               558938 non-null  float64\n",
            " 20  DREB               558938 non-null  float64\n",
            " 21  REB                558938 non-null  float64\n",
            " 22  AST                558938 non-null  float64\n",
            " 23  STL                558938 non-null  float64\n",
            " 24  BLK                558938 non-null  float64\n",
            " 25  TO                 558938 non-null  float64\n",
            " 26  PF                 558938 non-null  float64\n",
            " 27  PTS                558938 non-null  float64\n",
            " 28  PLUS_MINUS         535277 non-null  float64\n",
            "dtypes: float64(19), int64(3), object(7)\n",
            "memory usage: 147.9+ MB\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "d19ded0c",
        "outputId": "6583b262-6f28-4765-a700-22a56c3a1148"
      },
      "source": [
        "second_highest_win_percentage_team = team_stats.iloc[1]\n",
        "print(f\"Team with the second highest win percentage: {second_highest_win_percentage_team['NICKNAME']} with {second_highest_win_percentage_team['WIN_PERCENTAGE']:.2f}% wins.\")"
      ],
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Team with the second highest win percentage: Mavericks with 57.08% wins.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "454d55ca",
        "outputId": "46a36124-3008-41e7-a11e-e61d01789690"
      },
      "source": [
        "highest_win_percentage_team = team_stats.iloc[0]\n",
        "print(f\"Team with the highest win percentage: {highest_win_percentage_team['NICKNAME']} with {highest_win_percentage_team['WIN_PERCENTAGE']:.2f}% wins.\")"
      ],
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Team with the highest win percentage: Spurs with 63.32% wins.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "from google.colab import drive\n",
        "drive.mount('/content/drive')"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "hW89yEkhv0hr",
        "outputId": "c3f74292-b7b9-4974-e732-c55e490c283a"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount(\"/content/drive\", force_remount=True).\n"
          ]
        }
      ]
    }
  ],
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "display_name": "Python 3",
      "name": "python3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "nbformat": 4,
  "nbformat_minor": 0
}📫 How to reach me: hasanbas388@gmail.com
  
-->
