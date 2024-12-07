# Cross Reference Matrix

| **Stakeholder**         | **URD Section Number** | **URD Topic**                      | **SRS Section Number** | **SRS Topic**               | **Architecture Section** | **Arch Topic**                   | **Design Section Number** | **Design Topic**                | **Test Section Number** | **Test Topics**                 |
|--------------------------|------------------------|-------------------------------------|-------------------------|-----------------------------|---------------------------|----------------------------------|----------------------------|----------------------------------|--------------------------|----------------------------------|
| Shopper                 | 1.1                    | Browse Products                    | 2.1                     | Product Listing Page        | 3.1                       | Product Service, Frontend UI     | 4.1                        | Product Listing UI, API         | 5.1                      | Verify product display          |
| Shopper                 | 1.2                    | Search and Filter Products         | 2.2                     | Search and Filter           | 3.2                       | Search API, Filter Service       | 4.2                        | Search Bar UI, Filter Module     | 5.2                      | Verify search/filter feature    |
| Shopper                 | 1.3                    | Add Products to Cart               | 2.3                     | Cart Management             | 3.3                       | Cart Service                     | 4.3                        | Add to Cart API, Cart UI         | 5.3                      | Verify cart functionality       |
| Shopper                 | 1.4                    | Proceed to Checkout                | 2.4                     | Checkout Process            | 3.4                       | Checkout Service, Payment Gateway| 4.4                        | Checkout UI, Payment Gateway API | 5.4                      | Verify checkout process         |
| Guest User              | 1.5                    | View Products                      | 2.5                     | Product Visibility          | 3.1                       | Product Service, Frontend UI     | 4.1                        | Product Listing UI              | 5.5                      | Verify product access for guests|
| Admin                   | 1.6                    | Manage Products                    | 2.6                     | Product Management Panel    | 3.5                       | Admin Dashboard                  | 4.5                        | Product Management UI, APIs      | 5.6                      | Verify product CRUD operations  |

---

# Non-Functional Requirements (NFRs)

| **NFR ID** | **Requirement Description**          | **SRS Section** | **Architecture Section** | **Design Section** | **Test Section** |
|------------|--------------------------------------|------------------|---------------------------|---------------------|------------------|
| NFR1       | System should handle 5000 concurrent users. | 2.7              | 3.6                       | 4.6                 | 5.7              |
| NFR2       | Application should meet WCAG standards.    | 2.8              | 3.7                       | 4.7                 | 5.8              |
