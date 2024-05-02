# Interface Definitions

## Purpose

The purpose of the interface definitions is to specify the external interfaces that the system implements.  The interface definitions are intended to specify the structure of the interfaces for developers using a contract-first development approach.  The artifacts in the interface definitions are at the `fish` level of abstraction.

## Electivity

This section is considered:  **Mandatory, if Detailed View is included**

## Online Banking API Interface Definition

<div style="width:100%; text-align: center; border-style: solid;">
<br/>

```yaml
openapi: 3.0.0
info:
  title: Online Banking API
  description: This API provides access to basic banking operations for online banking services.
  version: 1.0.0
servers:
  - url: https://api.examplebank.com/v1
paths:
  /accounts:
    get:
      summary: Retrieve all accounts
      description: Retrieves a list of all accounts associated with the authenticated user.
      responses:
        '200':
          description: A list of accounts.
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Account'
  /accounts/{accountId}:
    get:
      summary: Retrieve account details
      description: Retrieves details for a specific account.
      parameters:
        - name: accountId
          in: path
          description: ID of the account to retrieve.
          required: true
          schema:
            type: integer
      responses:
        '200':
          description: Account details retrieved successfully.
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Account'
        '404':
          description: Account not found.
    patch:
      summary: Update account details
      description: Update details for a specific account.
      parameters:
        - name: accountId
          in: path
          description: ID of the account to update.
          required: true
          schema:
            type: integer
      requestBody:
        required: true
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/AccountUpdate'
      responses:
        '200':
          description: Account details updated successfully.
        '404':
          description: Account not found.
components:
  schemas:
    Account:
      type: object
      properties:
        id:
          type: integer
        account_number:
          type: string
        balance:
          type: number
      required:
        - id
        - account_number
        - balance
    AccountUpdate:
      type: object
      properties:
        balance:
          type: number
      required:
        - balance
```

<br/>
</div>

## More Information on Interface Definitions

There are two primary types of interface definitions: human interface storyboards and API specifications.  Human interface storyboards are used to describe the interactions between the system and the user.  API specifications are used to describe the interactions between the system and other systems.  For human inteface specifications, tools like [Figma](https://www.figma.com/) can be used.  For API specifications, they should be defined using an API specification standard such as [OpenAPI](https://swagger.io/specification/).  The artifacts in the interface definitions are at the `fish` level of abstraction and are meant for developers primarily.
