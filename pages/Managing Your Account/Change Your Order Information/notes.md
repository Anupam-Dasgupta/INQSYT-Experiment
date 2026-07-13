### Observations for Change Your Order Information

- **Intent Additions**: Added `change_order_information` because updating order details (quantity, address, payment method) before dispatch is the primary action explicitly supported by the page.
- **Intent Rejections**: The user rejected adding `change_third_party_seller_order` and `modify_fresh_delivery`. Since these are redirection links pointing to distinct/separate sub-services (contacting third-party sellers, Fresh delivery modify pages), they are treated as external references rather than direct intents supported by the page's native workflow.
