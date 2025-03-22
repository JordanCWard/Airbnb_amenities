# **Denver Airbnb Amenity Analysis**

## **Overview**  
- Founded in 2008, Airbnb is a San Francisco-based company specializing in short- and long-term homestays.  
- Guests have diverse accommodation needs, from pet-friendly options to child-friendly amenities like cribs.  
- This case study aims to identify market inefficiencies within the Denver Airbnb market, providing insights for real estate investors.  

- [Tableau Dashboard
](https://public.tableau.com/views/AirbnbAmenitiesinDenver/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
 
---

## **Neighborhood Analysis**  

- Denver consists of **78 distinct neighborhoods** with **5,378 Airbnb listings**.  
- **Highest Listing Volume:**  
  - Five Points leads with **452** active listings.  
- **Lowest Listing Volume:**  
  - Sun Valley has only **one** Airbnb listing.  
- **Pricing Overview:**  
  - **Average Nightly Rate:** $252.72  
  - **Most Affordable Neighborhood:** Kennedy - **$78.33 per night**  
  - **Most Expensive Neighborhood:** Cheesman Park - **$1,038.86 per night**  

---

## **Amenity Analysis**

- Denver Airbnb listings collectively offer **2,301 unique amenities**.  
- After data refinement, **137 distinct amenities** were selected for analysis.  

#### **Most Common Amenities:**  
- 🏠 **Washing Machine** – Found in **7,748** listings  
- 🚗 **Free Parking** – Available in **6,875** listings  
- 📶 **Wi-Fi** – Provided in **5,405** listings  

#### **Least Common Amenities:**  
- These amenities appear in only **one** listing each:  
  - Paid resort access  
  - Toiletries  
  - Complimentary continental breakfast  
  - Game room  
  - Garden  

---

## **Best Deals on Amenities**  

- Some neighborhoods offer significant savings when booking listings with specific amenities:

  - **🏡 Backyard (Cheesman Park):**  
    - Listings with backyards cost **$788.60 less** than the average Cheesman Park rental.  

  - **🔥 BBQ Grill (Sunnyside):**  
    - Listings with BBQ grills are **$360.93 cheaper** than the neighborhood average.  

  - **🐶 Pet-Friendly (Whittier):**  
    - Pet-friendly listings provide **$222.52 in savings** compared to the neighborhood average.  

  - **❄️ Window Air Conditioning (Lincoln Park):**  
    - Listings with window A/C units cost **$361.90 less** than the average Lincoln Park rental.  

> *Note:* Amenity-based pricing is influenced by additional factors such as square footage and the number of bedrooms.

---

## **Data Cleaning Process**  
### **Steps Taken for Data Preparation**  
- The dataset was processed using **BigQuery** and **SQL** as primary tools.  

1. **Isolated Key Columns** – Extracted the amenities column and listing IDs.  
2. **Data Transformation** – Amenities, initially stored as a single field, were split into multiple columns.  
3. **Standardization** – Similar amenities were consolidated using the `REPLACE` function, reducing unique amenities from **2,801 to 137**.  
4. **Selection Criteria** – **31 key amenities** were chosen for further analysis based on popularity and added value.  
5. **CSV Export** – The cleaned data was exported to a CSV file.  

### **Example Data Entry (Row #14 - Cherry Creek)**  
| Neighborhood  | Listings | Avg Price/Night | Bathtub Count | Bathtub Avg Price | Price Difference |  
|--------------|----------|----------------|--------------|----------------|-----------------|  
| Cherry Creek | 65       | $276.65        | 39           | $185.38        | -$91.26         |  

> Listings where the price difference was **≥ $0** were removed from further analysis.  

---

# Source
Data was utilized from [Inside Airbnb](https://insideairbnb.com/get-the-data/) for analysis.
Data is sourced from the Denver, Colorado, United States section, from the dataset dated June 30, 2023.
The data covers the period from 4-1-23 to 6-30-23.


