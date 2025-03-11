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
| n_tickets | ... |
| n_customers | ... |
| n_tickets_success | ... |
| n_customers | ... |
| n_tickets | ... |
| n_customers | ... |

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
        ![decrease 13% (2)](https://github.com/user-attachments/assets/8bfb8447-8b6f-4f15-91cf-a9f8a120111e)
        **Figure 2:** Analysis of Target Customer Demographics
      </div>
    </td>
  </tr>
</table>

#### 4.1.2. Behavior

<table>
  <tr>
    <td width="30%">
      
Customers watch movies throughout the week, but the most preferred time is on weekends. On weekdays (Monday to Friday), they usually go to the cinema after work to unwind with the latest films. On weekends (Saturday and Sunday), they have more flexible schedules. They might watch movies around noon before engaging in other leisure activities or choose a late-night screening as their final entertainment of the day.
    </td>
    <td width="70%">
      <div align="center">
        ![decrease 13% (4)](https://github.com/user-attachments/assets/3ca3d98e-fbce-4740-91e5-9f1e4f90fdfc)
        **Figure 3:** Analysis of Target Customer Behaviors
      </div>
    </td>
  </tr>
</table>

### 4.2. Factors Affecting the Customer Journey

#### 4.2.1. Ticket Booking Platform

<table>
  <tr>
    <td width="35%">
      
Along with mobile's dominance, iOS devices are the most commonly used for ticket booking. Over time, this trend has become more evident as the share of Android and other devices continues to decline. However, a system issue has emerged, with 45% of bookings failing to identify the device used - a problem that only appeared in 2022 but now accounts for nearly half of the total bookings over four years. Identifying the most-used devices will help the company allocate resources effectively when implementing product development strategies to enhance the booking experience.
    </td>
    <td width="75%">
      <div align="center">
        ![decrease 13%](https://github.com/user-attachments/assets/c65b7c88-c2fb-433e-bc39-677eb4208d26)
        **Figure 4:** Analysis of Ticket Booking Platform
      </div>
    </td>
  </tr>
</table>

#### 4.2.2. Booking Device

Along with mobile's dominance, iOS devices are the most commonly used for ticket booking. Over time, this trend has become more evident as the share of Android and other devices continues to decline. However, a system issue has emerged, with 45% of bookings failing to identify the device used—a problem that only appeared in 2022 but now accounts for nearly half of the total bookings over four years. Identifying the most-used devices will help the company allocate resources effectively when implementing product development strategies to enhance the booking experience.
<div align="center">

  ![decrease 13% (1)](https://github.com/user-attachments/assets/ce9b7dd0-ba30-4559-bb76-fdae1d4b6a6a)

  **Figure 5:** Analysis of Booking Device
  
</div>

#### 4.2.3. Movie Selection Factor

Customers do not exhibit strong preferences for specific movie genres but tend to follow trends. At different times, theaters attract large audiences with blockbuster films such as Avengers: Endgame, Avatar: The Way of Water, Face-off: 48h, and Extremely Easy Job. Both Hollywood and Vietnamese films are well-received upon release. Therefore, prioritizing trend-driven, highly anticipated, and widely publicized movies will maximize audience turnout.

<div align="center">

  ![image](https://github.com/user-attachments/assets/6f03d091-db15-4031-a006-898e9e748290)

  **Figure 6:** Trends in movies over time
  
</div>

#### 4.2.4. Movie Ticket Pricing

For customers, watching movies is a common leisure activity, so their spending on tickets remains relatively low, typically ranging from $4 to $10. Actual ticket prices are even lower, from $2 to $7. Marketing strategies—especially those related to pricing and promotions—must consider customer price sensitivity. The goal is to determine an optimal price point that attracts customers while ensuring revenue and profit targets are met.

<div align="center">

  ![decrease 13% (2)](https://github.com/user-attachments/assets/0ca940d3-20b0-4c53-87cf-42e3e26e6bfe)

  **Figure 7:** Original_price & Final_price Distribution
  
</div>

#### 4.2.5. Promotional Programs

<table>
  <tr>
    <td width="40%">
      
Over the past four years, 60% of moviegoers have come from promotional campaigns. Before 2022, the ratio of customers who purchased discounted vs. non-discounted tickets was relatively balanced. However, after the pandemic, the company intensified promotions to encourage customers to return to theaters.

Among all promotional strategies, direct discounts have been the most popular. This is likely because they apply instantly to ticket prices without requiring extra steps like redeeming "reward points" or collecting "vouchers." Since most customers only watch movies once or twice a month, loyalty programs and voucher hunting—common in daily consumer spending—may not be as effective.

In 2022, the direct discount strategy successfully brought back a significant number of customers post-pandemic. This approach should be considered for future marketing efforts.
    </td>
    <td width="60%">
      <div align="center">
        ![decrease 13% (3)](https://github.com/user-attachments/assets/9eaa332b-818d-486a-9c51-47128971ebd2)
        **Figure 8:** Analysis of Promotional Programs
      </div>
    </td>
  </tr>
</table>

#### 4.2.6. Payment Methods

Over the past four years, the primary payment methods have been bank accounts (31%) and money in app (48%). Before 2022, these two methods were nearly equal in popularity. However, over time, customers have increasingly shifted towards in-app payments.

This shift could be a positive sign, as it reduces reliance on third-party partners. However, it may also be due to frequent errors in bank account transactions, prompting customers to switch payment methods (see section …).

Since payment is the final stage of the movie ticket booking journey, any issues at this stage can result in lost revenue and potentially losing the customer altogether. Addressing payment-related problems is crucial to ensuring a seamless booking experience.

<div align="center">

  ![decrease 13% (4)](https://github.com/user-attachments/assets/ce9e7b05-eaae-46e6-b93b-e1b245bb6a24)

  **Figure 9:** Analysis of Payment Methods
  
</div>

#### 4.3.1. Customer Ticket Booking Experience

<table>
  <tr>
    <td width="65%">
      
Over the past four years, the cinema has attracted 119,477 customers, but 19,166 customers (16%) have never successfully booked a ticket. Additionally, 13,701 customers (11%) have a 100% failure rate in booking and may have abandoned the brand entirely.
    </td>
    <td width="35%">
      <div align="center">
        ![image](https://github.com/user-attachments/assets/51179d18-5e59-47e6-84a3-bac340f82fd2)
        **Figure 10:** Distribution of successful booking rates by n_customers
      </div>
    </td>
  </tr>
</table>

The primary reasons for booking failures stem from external factors, including customer-related issues and payment partner errors. These issues have persisted for four years without significant improvement. In 2022, when the number of ticket bookings surged, the number of booking failures also increased, showing no signs of resolution.

<div align="center">

  ![decrease 13% (4)](https://github.com/user-attachments/assets/eeedf424-5916-4704-b211-71a51e820fb7)
  
  **Figure 11:** Analysis of customer booking errors

</div>

**Customer-Related Issues**

Most errors originate from customers themselves, including:

- Insufficient funds in the account.
- Unverified accounts that do not meet payment requirements.
- Incorrect password entry when logging in.
- Expired payment sessions due to prolonged checkout time.

These may be business rules set by the company, making them difficult to modify for customer convenience.

**Payment Partner Issues**

A significant number of booking failures result from banking partner errors, primarily failed transactions due to banks. To address this, the company should strengthen partnerships with banks to improve payment reliability, enhance the booking experience, and retain more customers.

<div align="center">
  
  ![image](https://github.com/user-attachments/assets/df0b159b-d243-4ae8-85b2-84382e06fa33)
  
  **Figure 12:** Trends in n_tickets_fail across external errors by description

</div>
