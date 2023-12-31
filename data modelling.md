# Data Modeling Using Star and Snowflake Schemas

## Introduction

Before diving into data modeling, it's crucial to grasp the foundational concepts of fact and dimension tables, which are instrumental in structuring and organizing data.

### Fact Tables

Fact tables deal with quantitative and measurable data. They serve as repositories for essential facts or numerical metrics of a business process. Fact tables also establish connections to dimension tables through foreign keys, creating well-defined relationships.

Fact tables can be categorized into three primary types:

1. **Transaction Fact Tables:** These tables capture data related to individual transactions, such as sales orders, invoices, and payments. They provide detailed information about specific events.

2. **Periodic Snapshot Fact Tables:** Periodic snapshot fact tables store data representing the state of a business at a particular point in time. Examples include customer balances, product inventory, and website traffic statistics. These tables offer a snapshot of the business's condition at regular intervals.

3. **Accumulating Snapshot Fact Tables:** These tables record data depicting the evolution of a business process over time. They are used to track cumulative metrics, like total sales, customer churn rates, or website engagement levels.

For instance, consider the scenario of configuring a custom computer online and placing an order. The order date and order amount could be recorded in a snapshot table by the manufacturer, serving as an example of data stored in a fact table.
![image](https://github.com/Zain-ul-Abdin45/literate-octo-system/assets/47116254/3586eab2-9832-47e5-8123-dd75648f4422)



### Dimension Tables

Dimension tables provide context and categorization for facts. They contain attributes that help answer business questions and provide a framework for organizing data. These attributes can include names of people, product details, locations, and date/timestamp information.

Key features of dimension tables:

- They categorize and describe various aspects of facts or variables.
- Dimension tables use foreign keys to establish relationships with fact tables, allowing facts to be associated with their corresponding dimensions.

Examples of dimension tables include:

- **Product Table:** Containing attributes like make, model, color, and size for products.
- **Employee Table:** Including information such as employee names, titles, and departments.
- **Geographical Table:** Providing details about geographical locations, including country, state, city, and region.

In summary, fact tables store quantifiable data related to business processes, while dimension tables provide context and structure to these facts by categorizing and describing various attributes. Together, they form the basis for creating effective data models, such as star and snowflake schemas, to facilitate efficient data analysis and reporting in a business environment.

![image](https://github.com/Zain-ul-Abdin45/literate-octo-system/assets/47116254/ca9ae788-89ec-4666-9a2c-4c077bdd21d6)


# Star Schema

In a **Star Schema**, dimensions radiate from a central fact table. This design is commonly employed in the creation of specialized data warehouses known as "data marts."

![image](https://github.com/Zain-ul-Abdin45/literate-octo-system/assets/47116254/c98bd65f-6f47-4d44-a347-38850c410810)


## Snowflake Schema

**Snowflake schemas** represent a generalization of star schemas and can be thought of as normalized star schemas. Normalization involves separating the levels or hierarchies of a dimension table into separate child tables.

![image](https://github.com/Zain-ul-Abdin45/literate-octo-system/assets/47116254/a23a57dc-14f7-44d1-a0c7-043d3f35877d)

## Design Considerations

When designing a data schema, several crucial considerations come into play:

1. **Selecting the Business Process:** Begin by selecting the specific business process you intend to model. This could involve areas such as Sales, Manufacturing, or Supply Chain.

2. **Choosing the Level of Detail:** Determine the appropriate level of detail for your data. This decision impacts the granularity of your fact and dimension tables.

3. **Identifying Dimensions:** Identify and define the dimensions that provide context and categorization for your data. Dimensions may include aspects like time, location, products, and more.

4. **Identifying the Facts:** Pinpoint the key metrics or facts that represent the numerical aspects of your business process. These facts will be stored in the central fact table.

These considerations form the foundation for creating effective data schemas, such as star and snowflake schemas, which are essential for efficient data analysis and reporting in various business domains.
