# sales-information-system-V1
To support work efficiency, I've designed a simple information system using spreadsheets to aid in data processing. This system is customized to meet my requirements as an administrator at my present company.

## The formula used in this system
- IFS
- Sumif
- Vlookup
- Pivot Tabel
- Appscript

## This information system contains several sheets
1. Database
2. Transaction
3. Selling
4. Buying
5. Credit
6. Loan
7. Report
8. Fixed Report

### Let's break down this system
<b> 1. Database </b>
      <br>
     <img src="imgs/01.PNG" alt="Input">
     <p>Databases are one of the most important components of an information system. The database at my company contains items, each with several identifying attributes. The company uses two different Taxpayer Identification Numbers (NPWP), which is why each item must be assigned an ownership category, unless the article is non-VAT.</p>
<br>The main categories for identifying an item are:
1. VAT or non-VAT status: Determines if the item is subject to Value Added Tax.
2. Ownership (Taxpayer Identification Number): Specifies which company entity (NPWP) owns the article.
3. Service Fee: The amount the company pays to the mechanic for the article.
    <p>The purpose of having two ownership categories is for tax reporting; it allows the company to calculate how much tax must be paid for each Taxpayer Identification Number. (The specific reason for using two numbers is confidential company information).</p>
<br>This database also handles stock counting. The key columns for tracking inventory are:
- In: Items purchased or received into stock.
- Cash: Items sold with a cash payment.
- Credit: Items sold with a credit payment.
- Final Stock: The remaining inventory.
<p>The 'In', 'Cash', and 'Credit' columns use the SUMIF function to calculate their values, while the 'Final Stock' column uses a simple formula. </p> 
<br>
<b> 2. Transaction</b>
    <br>
    <img src="imgs/02.PNG" alt="Input">
    <p> Transaction Sheet" is the main data input feature. It is used to record sold items, purchased items, and items sold on credit. This sheet utilizes several formulas and features:p>
  <ol type="1"> 
      <li> Data Validation (Drop-down List): Provides a selectable list of names or items from a predefined range.</li>
      <li> VLOOKUP: Automatically retrieves corresponding values (e.g., item price, ID) based on the selected item.</li>
      <li> Google Apps Script: Powers custom buttons to automate actions:</li>
    <ul>
      <li>"Add" Button: Saves the current item's data to a specific sheet (e.g., "Selling" or "Buying") and then clears the input fields </li>
      <li>"Save" Button: Performs the same save function as the "Add" button but clears all input fields, except the date </li>
    </ul>
  </ol>
  <br>
<b> 3. Selling</b>
     <br>
     <p>The Selling Sheet is used to record tire sales data that has been input in the Transaction Sheet. Although it serves as a storage sheet, it also contains calculation formulas. These include:</p>

  <ul>
    <li>VLOOKUP to retrieve item information such as cost price, tax details, and ownership.</li>
    <li>Profit calculation by subtracting the cost price from the selling price.</li>
    <li>IF function to differentiate profit calculations between items categorized as "TIRE" and "SERVICE"</li>
  </ul>
  <br>
<b> 4. Buying</b>
     <br>
    <p>This sheet is similar to the Selling sheet, as it records purchased items input from the Transaction Sheet. However, it includes an additional 'Due Date' column. Since not all purchases are paid for immediately in cash, the due date is calculated by adding the distributor's granted payment term (in days) to the purchase date. I manually input the number of days for each distributor, as this term varies between suppliers.</p>
<br>
<b>5. Credit</b>
  <p>This sheet has many similarities with the Selling Sheet. The difference is that this sheet includes a customer name column to simplify accounts receivable reporting, making it easy to identify parties that have debt with the company.</p>
<br>
<b>6. Loan</b>
  <br>
    <img src="imgs/06.PNG" alt="Input">
  <br>
  <p>This sheet contains a pivot table that summarizes the total debt based on date, distributor, and invoice number.</p>
<b>7. Report</b>
  <p>This sheet contains a daily sales report table that uses the SUMIF formula, along with the total amount of wheel alignment service fees to be paid to the mechanic. The report also separates company capital, profit, and revenue from the wheel alignment service.</p>
<br>
<b>8. Report</b>
  <p>This sheet is similar to the Report sheet. However, the figures in the Report sheet often contain precise values (e.g., "Rp 43.445") because they are calculated directly from the selling price minus the cost price. The owner requested that all amounts be rounded. Therefore, I created a new sheet specifically to round values to the nearest multiple of 5,000, for example, Rp 43.445 becomes Rp 45,000.</p>

### Detail
<ul>
  <li>Link detail formula:  <a href="https://github.com/vini-indriyani/sales-information-system-V1/blob/main/Formula.md">LINK</a></li>
  <li>Link spreasheet file: <a href="https://docs.google.com/spreadsheets/d/1nN5QMxnURaHM3PqVMtd_Ujc825Ct4DVWMhn3jmxHl_k/edit?gid=928908800#gid=928908800">LINK</a></li>
</ul>
