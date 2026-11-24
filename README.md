
# SecureBank Dynamic Email Newsletter | Salesforce Marketing Cloud & AMPscript

## Project Overview

A personalized monthly financial newsletter developed for SecureBank, a fictional financial institution.

Built in Salesforce Marketing Cloud (SFMC) using HTML and AMPscript, this project demonstrates dynamic content retrieval, customer preference-based personalization, conditional messaging, and reusable newsletter templates.

## Business Scenario

SecureBank wants to deliver relevant financial information to customers based on their interests while reducing the manual effort required to update monthly newsletters.

Instead of creating separate email templates for different customer segments, the campaign uses one dynamic template to retrieve articles, images, descriptions, and links from a Data Extension.

The newsletter is designed to be sent on the 7th day of each month.

### Supported Customer Preferences

- Home Loans
- Credit Cards
- Long Term Investment
- Short Term Investment
- Term Deposits

Each customer receives three articles relevant to their preference category.

## AMPscript Features Demonstrated

### 1. Personalization

- Dynamic first-name greetings
- Personalized email subject lines
- Name formatting using Trim() and ProperCase()
- Fallback handling for missing first names
- Dynamic month display using Now() and FormatDate()

### 2. Conditional Messaging

- IF / ELSEIF / ELSE / ENDIF statements
- Category-specific introductory messages
- Customer preference-based content selection
- Validation of available newsletter records

### 3. Data Extension Lookups

- LookupRows() to retrieve newsletter content
- RowCount() to validate matching records
- Row() to retrieve the selected record
- Field() to retrieve individual article attributes

### 4. Dynamic Content

- Three personalized articles per customer
- Dynamic article titles and descriptions
- Dynamic article images
- Customer preference-specific introductory messaging
- Dynamic article links using RedirectTo()

### 5. Error Handling

- RaiseError() when matching newsletter content is unavailable
- Prevention of sending a newsletter without the required content record

## Data Extensions

### 1. Newsletter_Audience

Stores customer information and financial preference categories.

**Fields:**
- CustomerID
- FirstName
- LastName
- Email
- PreferenceCategory

### 2. Newsletter_Content_Data

Stores the newsletter content managed and updated by marketers each month.

**Fields:**
- Category
- Article1Title
- Article1Description
- Article1Link
- Article1ImageURL
- Article2Title
- Article2Description
- Article2Link
- Article2ImageURL
- Article3Title
- Article3Description
- Article3Link
- Article3ImageURL

The customer's PreferenceCategory is matched with the Category field in Newsletter_Content_Data to retrieve relevant newsletter content.

## Newsletter Campaign

### Dynamic Monthly Newsletter

**Planned Timing:** 7th day of each month

**Purpose:** Deliver relevant financial articles and encourage customers to explore SecureBank products and services.

**Key Features:**

- Personalized greeting and subject line
- Automatically generated current month
- Five preference-based content categories
- Three dynamically retrieved articles
- Dynamic article images, descriptions, and links
- Error handling for missing content records
- Reusable email template for monthly content updates

## Preview and Testing

The newsletter was previewed in Salesforce Marketing Cloud using sample customer records.

Testing focused on:

- First-name formatting and fallback handling
- Dynamic month generation
- Preference-based article retrieval
- Category-specific introductory messaging
- Dynamic article titles and descriptions
- Personalized article links

### Sample Personalization Results

| Customer | Preference Category | Newsletter Content |
|---|---|---|
| John | Home Loans | Loan rates, loan tips, refinancing |
| Sarah | Credit Cards | Credit card offers, rewards, card management |
| Missing First Name | Long Term Investment | Investment planning, strategies, diversification |

The sample previews demonstrate how the same email template can display different financial content depending on the customer's preference.

## Project Files

- `01-Dynamic-Email-Newsletter.html` — AMPscript personalization logic and HTML newsletter template

## Tools and Technologies

- Salesforce Marketing Cloud (SFMC)
- Email Studio
- AMPscript
- HTML
- Data Extensions
- GitHub

## Project Note

This project was completed as part of the AMPscript Academy Capstone 4 assignment.

SecureBank is a fictional financial institution. Customer records, website addresses, and article content are used for educational and portfolio demonstration purposes.

The project demonstrates dynamic newsletter content and preview testing rather than a deployed monthly automation or live campaign performance.

