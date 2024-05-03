# Use Case Inventory

## Purpose

The use case inventory artifact is a full inventory of any documented use cases for the target-state solution.  The use cases are more detailed than the key use cases and may be defined to several layers of decomposition and detail depending on the complexity of the system.  The primary reason for defining detailed uses cases is to define the behavior of the system down to the API-level of detail and the primary audience for this artifact are architects and lead engineers responsible for driving the implementation of the target-state solution.  This artifact will be used as input in the creation of both the [Interface Definitions](/detailed/InterfaceDefinitions.md) artifact and the [Sequence Diagrams](/detailed/SequenceDiagrams.md) artifact in the [Detailed View](/detailed/) of this organizer.  The artifacts in the use case inventory are at the `sea` level of abstraction.

## Electivity

This artifact is considered:  **Optional**

## Use Case Inventory for Online Banking

The use case inventory for the online banking system is shown below.  It summarizes the uses case that the Interface Definitions artifact specifies.

### UC-02.01 -- Retrieve All Accounts

* **Actor**: Authenticated User
* **Description**: The user wants to retrieve a list of all accounts associated with their profile.
* **Preconditions**: User must be authenticated.
* **Basic Flow**:
  1. User sends a request to retrieve all accounts.
  2. System retrieves and returns a list of all accounts.
* **Alternate Flow**: None.
* **Postconditions**: User receives a list of all their accounts.

### UC-02.02 -- Retrieve Account Details

* **Actor**: Authenticated User
* **Description**: The user wants to retrieve detailed information about a specific account.
* **Preconditions**: User must be authenticated.
* **Basic Flow**:
  1. User provides the account ID for the account they want to retrieve details for.
  2. System retrieves and returns details for the specified account.
* **Alternate Flow**: If the account ID provided does not exist, system returns a 404 error (Account not found).
* **Postconditions**: User receives detailed information about the specified account if it exists.

### UC-02.03 -- Update Account Details

* **Actor**: Authenticated User
* **Description**: The user wants to update details for a specific account.
* **Preconditions**: User must be authenticated.
* **Basic Flow**:
  1. User provides the account ID for the account they want to update.
  2. User submits the updated account details.
  3. System updates the account details based on the provided information.
* **Alternate Flow**: If the account ID provided does not exist, system returns a 404 error (Account not found).
* **Postconditions**: Account details are successfully updated if the account exists.
