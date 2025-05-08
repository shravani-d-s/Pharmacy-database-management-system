
# Pharmacy Management System (C Project)

This project is a **Pharmacy Management System** implemented in **C**, designed to manage and track medications, suppliers, batches, and sales using **B-Trees** for efficient storage and retrieval.

##  Features

- Add, update, search, and delete medications.
- Track medication batches with expiry dates.
- Add, update, search, and delete suppliers.
- B-Tree and B-Tree-String based indexing:
  - Medications by ID
  - Medications by name
  - Expiry dates
  - Suppliers by ID
- Sales tracking and automatic stock updates.
- Expiry date and reorder level alerts.
- Top 10 suppliers by turnover and unique medications.
- Save and load data from file for persistence.

##  Data Structures

- **B-Trees** for indexing medications and suppliers.
- **Structs** to represent `Medications`, `Batches`, and `Suppliers`.
- **Heap Sort** used to identify top suppliers.

##  Files

- `pharmacy.c`: Complete source code.
- `medications_data.txt`: Generated at runtime to persist data.

##  How to Use

1. **Compile** using a C compiler:
   ```bash
   gcc pharmacy.c -o pharmacy
   ```

2. **Run** the program:
   ```bash
   ./pharmacy
   ```

3. Follow the steps to interact with the system.

##  Requirements

- GCC or any standard C compiler
- Standard C library headers (`stdio.h`, `stdlib.h`, `string.h`)

---

##  Function Overview

###  Medication Management

- `addMedicationGeneral(...)` – Adds a new medication and batch, links to suppliers.
- `updateMedication(medID)` – Updates price and quantity for a medication's batch.
- `deleteMedication(...)` – Deletes a specific batch or the entire medication.
- `searchMedication()` – Offers search by medID, name, or supplier.
- `stockAlerts(...)` – Triggers low stock warnings based on reorder levels.
- `checkexpirydate(...)` – Lists expired and soon-to-expire batches.
- `sortMedicationByExpiry(...)` – Filters medications between two expiry dates.
- `salesTracking(...)` – Deducts sold stock, prioritizing earlier expiry.

###  Supplier Management

- `supplierManagement()` – Main menu for add, update, delete, and search.
- `addsupplier()` – Adds a supplier and links to batch.
- `deleteSupplier(...)` – Removes a supplier and its associations.
- `updateSupplier(...)` – Updates supplier's contact and quantity supplied.
- `searchbysupplier()` – Lists medications supplied by a specific supplier.

###  Analytics

- `top10Allrounders()` – Top 10 suppliers by number of unique medications.
- `top10largestturnover()` – Top 10 suppliers by total turnover (price × quantity).

###  File Operations

- `saveMedicationsToFile()` – Saves all data to a file.
- `loadMedicationsFromFile()` – Loads data from file.

---

##  License

This project is open source and available under the MIT License.
