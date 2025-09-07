# Formulas Used

## Database

<img src="imgs/01.PNG" alt="Input">
<ol type="1">
  <li><p><B>In</B>: to dynamically calculate the total quantity of each purchased item, I implemented the <code><span class="math inline">SUMIF</span></code> function. This formula checks the list of item names and sums the corresponding quantities only for the specified item.</p></li>
   <B>Formula:</B> <code><span class="math inline">=SUMIF(item_name_range, specific_item, quantity_range)</span></code>
   <br><B>Implementation:</B> <code><span class="math inline">=SUMIF('BUYING 2025'!G:G, B2, 'BUYING 2025'!H:H)</span></code>
   <br>
   <br>
  
  | Argument | Role in This Context |	Example
  | :--- | :--- | :--- |
  | range/item_name_range | 	The list to search through.  | 'BUYING 2025'!G:G |
  | criteria/specitif_item | The specific item to total.  | B2 |
  | sum_range/quantity_range  | The values to add together.  | 'BUYING 2025'!H:H |

  <P><b>Key Insight</b>: The <code><span class="math inline">sum_range</span></code> is essential. Without it, Excel would attempt to sum the text values in the <code><span class="math inline">item_name_range</span></code>, which would result in an error.</P>
  
  <li><b>Cash</b>: Tracks total items sold via cash payments. The value is dynamically calculated using a <code><span class="math inline">SUMIF</span></code> formula that references data in the 'Selling' sheet</li>
   <B>Implementation:</B> <code><span class="math inline">=SUMIF('SELLING'!D:D, B2, 'SELLING'!E:E)</span></code>
   <br>
   <BR>
  <li><b>Credit</b>: Tracks total items sold via credit payments, formula that references data in the 'Credit' sheet</li>
   <B>Implementation:</B> <code><span class="math inline">=SUMIF('CREDIT'!D:D, B2, 'CREDIT'!E:E)</span></code>
   <br>
   <BR>
  <li><b>Final</b> stock of an item. The value is calculated using the formula: =(Initial Stock + in) - (Goods Sold via Cash Sales + Credit Sales)</li>
   <B>Implementation:</B> <code><span class="math inline">=(F2+M2)-(N2-02)</span></code>
   <br> 
</ol>
<BR>

## Transaction

## Selling

## Buying

## Credit

## Loan

## Report
