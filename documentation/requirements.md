# System Requirements

## Goals

- **Streamline Warehouse Operations**  
  Reduce manual effort and streamline the stock in, sorting, and stock out processes.

- **Enhance Data Accuracy**  
  Improve the accuracy of stock level data for the warehouse, including overall stock level as well as individual stock levels.


## Functional Requirements

1. **Stock In Process**
   - The system must have a 'stock in' form which will read from the scales when stock arrives at the warehouse and record the weight of the stock accurately.
   - The system must have a 'stock in' collection screen which displays each instance of stock being added to the warehouse.

2. **Sorting Process**
   - The system must have a 'sorting' form which reads directly from the scales and allows the sorting team to record weight/item/crate/quantity while sorting food into crates. 
   - The form must allow users to print labels/barcodes containing information about the sorted crate.

3. **Stock Out Process**
   - The system must allow users to create replenishment sheets on the system using a 'create a replen' form.
   - The system must have a replenishment collection screen which displays all replens in tabular form.
   - The system must allow users to complete replens by selecting a replen from the collection screen, items on the replen will be marked off as volunteers scan the barcodes of corresponding crates.

4. **Stock Level Management**
   - The system must accurately record stock levels for each stock item.
   - The system must allow users to be able to view stock levels for each stock item.
   - The system must have a settings/configuration module that allows users to view/edit values such as crate type and stock type.

5. **Data Exportation**
   - The system must allow exports of records.

6. **Authentication**
   - The system must have sign in/sign out functionality.
   - The system must have different levels of user access/authorisation.


## Non-Functional Requirements

1. **Performance**
   - The system must respond to user interactions promptly under normal load conditions.
   - Stock level updates should be reflected in real-time across all users' screens.
   - The system should be capable of handling concurrent requests from multiple users without significant performance degradation.

2. **Scalability**
   - The system should scale seamlessly to accommodate an increase in the number of users and data volume over time.
   - It should support multiple concurrent users during peak hours without experiencing performance issues.

3. **Reliability**
   - The system must have automated backup and recovery mechanisms to ensure data integrity and minimize downtime in case of system failures.

4. **Security**
   - User authentication must be enforced using strong encryption methods (e.g., bcrypt) to protect sensitive information.
   - Access control mechanisms should be in place to ensure that only authorized users can view, modify, or delete stock-related data.
   - The system must comply with industry-standard security protocols (e.g., SSL/TLS) for secure communication over the network.

5. **Usability**
   - The user interface should be intuitive and easy to navigate, requiring minimal training for new users.
   - Error messages should be descriptive and provide guidance on how to resolve issues effectively.
   - The system should support accessibility features (e.g., screen readers, keyboard navigation) to accommodate users with disabilities.

6. **Availability**
   - The system should be available 24/7, with planned maintenance windows communicated to users in advance.

7. **Data Integrity**
   - Data backups should be performed regularly and stored securely to prevent loss in the event of data corruption or deletion.

8. **Compliance**
   - The system must comply with relevant data protection regulations (e.g., GDPR, HIPAA) and industry standards.
   - Audit trails should be maintained to track user actions and changes to sensitive data for compliance and accountability purposes.

9. **Interoperability**
   - The system should integrate seamlessly with external hardware (e.g., barcode scanners, weighing scales).


## Constraints

1. **Training Requirement**
   - The warehouse volunteers will require comprehensive training to ensure they understand and use the system effectively, particularly concerning the 'sorting process' functionalities.

2. **Hardware Compatibility**
   - The system will require compatible weighing scales and barcode scanners that can seamlessly integrate with the software application to facilitate accurate data input and processing.

3. **Network Reliability**
   - A reliable internet connection is necessary for the system to operate effectively, ensuring real-time data updates, and uninterrupted access to the application.
