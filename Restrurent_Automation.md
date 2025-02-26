
# **2(a) Process Customer Order**  

### **Primary Actors:**  
- Customer  
- Sales Clerk  

### **Pre-Condition:**  
- The restaurant is open, and the system is functioning properly.  

### **Mainline Scenario:**  
1. The customer places an order (in-person, via phone, or online).  
2. The sales clerk enters the order into the system, including item details, quantities, and special requests.  
3. The system checks the inventory for ingredient availability.  
4. If all ingredients are available, the system calculates the total order cost.  
5. The system prints the order details for the kitchen staff to begin preparation.  
6. The sales clerk receives payment from the customer.  
7. The system records the sale and updates the inventory.  
8. The system prints a receipt for the customer.  

### **Alternate Scenarios:**  

#### **Scenario 1: Invalid Item Code Entered (Occurs after Step 2)**  
- The system displays an error message.  
- The sales clerk re-enters the item code or searches for the correct item.  
- The process returns to Step 2.  

#### **Scenario 2: Item Not Available (Occurs after Step 3)**  
- The system displays a message indicating the item is out of stock.  
- The sales clerk informs the customer.  
- The customer can either remove or substitute the item (returning to Step 3) or cancel the order (ending the process).  

#### **Scenario 3: Ingredient Not Available (Occurs after Step 3)**  
- The system alerts that an essential ingredient is low or out of stock.  
- The sales clerk informs the customer that the item cannot be prepared.  
- The customer can either remove or substitute the item (returning to Step 3) or cancel the order (ending the process).  

#### **Scenario 4: Discount/Coupon Applied (Occurs after Step 4)**  
- The sales clerk applies a discount or coupon.  
- The system recalculates the total order amount.  
- The process returns to Step 6.  

#### **Scenario 5: Order Modification (Occurs before Step 6)**  
- The customer requests changes to the order.  
- The system updates the order and recalculates the total.  
- The process returns to the appropriate step based on the type of modification.  

#### **Scenario 6: Payment Error (Occurs after Step 6)**  
- The payment is declined due to insufficient funds or technical issues.  
- The sales clerk tries another payment method or cancels the order.  

---

# **2(b) Restock Inventory**  

### **Primary Actors:**  
- System  
- Manager  

### **Pre-Condition:**  
- The system is operational, and inventory levels are being tracked.  

### **Mainline Scenario:**  
1. The system automatically monitors ingredient inventory levels daily.  
2. When the stock of an ingredient falls below the predefined threshold, the system generates a purchase order.  
3. The purchase order includes ingredient details, quantity, and supplier information.  
4. The system sends the purchase order to the supplier.  
5. The supplier delivers the ordered ingredients.  
6. The manager verifies the delivery against the purchase order and invoice.  
7. The manager enters the invoice details into the system.  
8. The system updates the inventory to reflect the newly received stock.  
9. If sufficient cash balance is available, the system prints a check against the invoice for payment.  

### **Alternate Scenarios:**  

#### **Scenario 1: Manual Restock Request (Occurs after Step 1)**  
- The manager identifies the need for a restock despite stock levels not yet reaching the threshold.  
- The manager manually initiates the restock process in the system.  
- The process continues from Step 3.  

#### **Scenario 2: Threshold Value Adjustment (Occurs after Step 1)**  
- The manager decides to adjust the stock threshold value for an ingredient.  
- The system updates the threshold value accordingly.  
- The process returns to Step 1 for continued inventory monitoring.  

#### **Scenario 3: Supplier Unable to Fulfill Order (Occurs after Step 4)**  
- The supplier informs the restaurant that an ingredient is unavailable.  
- The system automatically searches for an alternative supplier.  
- The process continues from Step 4 with the new supplier.  

#### **Scenario 4: Incorrect Delivery (Occurs after Step 5)**  
- The delivered quantity differs from the purchase order.  
- The manager adjusts the invoice data accordingly.  
- If the discrepancy is significant, a return process is initiated, and a credit is issued.  
- The process continues from Step 8.  

#### **Scenario 5: Damaged Goods (Occurs after Step 5)**  
- The manager identifies that some delivered goods are damaged.  
- The damaged items are returned to the supplier, and a credit is issued.  
- The system updates the inventory to reflect the reduced stock.  
- The process continues from Step 8.  

#### **Scenario 6: Insufficient Cash Balance (Occurs after Step 9)**  
- The system alerts the manager about insufficient funds for invoice payment.  
- The manager arranges an alternative payment method.  
- The process is completed successfully.  
