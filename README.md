# Movie Ticket Analysis

## 1. Project Background

### 1.1. Situation

Assume you are in the role of **an Analyst** in the **product development department** of the company. To help increase the volume of orders and customers purchasing movie tickets online, you need to analyze the data of customers' booking history over the past years. From there, provide **informative insights about customer behavior and corresponding recommendations**.

### 1.2. Objective

- Analyze and identify the target customer profile.
- Examine the key factors influencing the customer’s ticket booking journey.
- Propose solutions to enhance the cinema chain's revenue.

## 2. Data Structure and Related Metrics

### 2.1. Data Structure

Movie ticket database as seen below consists of five tables: _ticket_history, customer, device_detail, campaign & status_detail_, with a total row count of **154,725 records**.

![image](https://github.com/user-attachments/assets/b74f7338-a181-4747-928f-43141b2119dc)

Before starting the analysis, various quality control checks were conducted to ensure data integrity and to familiarize myself with the dataset. The Python code used for inspection and quality checks can be found here.

### 2.2. Data Metrics and Definitions

During the analysis process, various terms have been defined to ensure consistency in information and facilitate analysis. Below is a summary of all the terms used.

| Cột 1 | Cột 2 |
|-------|-------|
| Nội dung 1 | Nội dung 2 |
| Thêm thông tin | Tiếp tục nội dung |

## 3. Executive Summary

### 3.1. Customer Persona

- **Target Customers:** individuals aged 26-35. This group has been in the workforce for some time and is entering a more stable phase of life. They view movie-watching as a form of weekend entertainment or a way to unwind after long workdays.
- **Potential Customers:** Individuals aged 18-25. For this group, going to the movies is more of a social or dating activity rather than a way to relax after work.

### 3.2. Factors Influencing the Customer Journey

- **Booking Platform:** Customers prefer booking tickets through a mobile app for convenience and ease of use.
- **Device Used for Booking:** iOS is the most commonly used mobile operating system among customers.
- **Movies Available in Theaters:** Blockbuster movies and those that go viral on social media attract the most attention.
- **Ticket Pricing:** Customers are willing to pay between $3 and $7 for a movie ticket.
- **Promotional Offers & Discounts:** Direct discounts are the most preferred type of promotion among customers.
- **Payment Methods:** Bank account transfers and in-app mobile payments are the two most convenient payment methods for customers.

By understanding these key touchpoints in the customer’s ticket booking journey, businesses can make informed decisions to enhance user experience and optimize revenue potential.

### 3.3. Customer Experience

- **Ticket Booking Experience:** The payment stage is a major pain point in the booking process. The second most important payment method, bank account transfers, has technical issues, causing transaction failures. As a result, over 11% of customers abandon the brand due to this inconvenience.
- **In-Theater Experience:** The quality of service provided at theaters is not meeting customer expectations. This is reflected in the low customer retention rate, with less than 5% of customers returning monthly to watch movies.

### 3.4. Recommendations

Based on the analysis, the company should focus on the following areas to drive business growth:

- **Enhance Product Quality (Booking Platform):** Improve the booking platform to ensure a seamless and reliable experience, particularly in the payment process.
- **Improve Service Quality:** Focus on enhancing the in-theater experience to increase customer retention rates.
- **Develop Effective Customer Acquisition Campaigns:** Prioritize marketing initiatives with proven high effectiveness to attract more customers.
- **Upgrade the Company’s Data Infrastructure:** Strengthen data systems to ensure higher data quality for better decision-making.

### 3.5. Constraints

The dataset covers the period from January 2019 to December 2022. As a result, customer behavior trends during these years were significantly impacted by COVID-19, making it difficult to establish accurate patterns. The pandemic began in 2019, reached its peak in 2020 and 2021, and only started recovering in 2022. Since movie-watching is an on-time activity, this period experienced considerable disruption (See **Figure 1**).

<div align="center">

  ![image](https://github.com/user-attachments/assets/55f80fc4-730f-4861-8e76-954bc662e533)

  **Figure 1:** Monthly trend of n_tickets
  
</div>

## 4. Insight Deep-Dive

### 4.1. Customer Persona

#### 4.1.1. Demographic (Age & Gender)

<table>
  <tr>
    <td width="50%">
      
**Target Customers:**
The majority of customers belong to Gen Z and Gen Y, particularly those at the tail end of Gen Z and the early years of Gen Y (ages 26–35). This age group has been working for some time and is entering a stable phase of life. As a result, they represent the company's primary target customers, accounting for 55% of total ticket purchases.

**Potential Customers:**
Additionally, mid-to-late Gen Z customers (ages 18–25) are worth considering, as they make up 20% of the customer base. In the future, this group will become a major part of the workforce and a key consumer segment.

**Gender Distribution:**
Based on purchase data, buying behavior between male and female customers appears to be similar. Therefore, the company does not need to segment these two groups separately at this stage.
    </td>
    <td width="50%">
      <div align="center">
        ![decrease 13%](https://github.com/user-attachments/assets/d258ca1a-266b-4cf7-b3dd-186c3af7ca50)
        **Figure 2:** Analysis of Target Customer Demographics
      </div>
    </td>
  </tr>
</table>
