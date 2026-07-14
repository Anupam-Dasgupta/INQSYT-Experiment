### Observations for Add, Delete, and Manage Addresses

- **Intent Additions**: Added `add_address`, `edit_address`, `delete_address`, and `set_default_address` as they represent the core address management capabilities documented on this page.
- **Excluded Details**:
  - The redirect to "Change Your Order Information" for shipping address changes on open orders is excluded as it is an external reference with its own dedicated help page.
  - The redirect to "Create Your List" for wish list address changes is excluded as it is an external reference.
  - The payment card confirmation prompt for new/edited addresses is a transactional constraint/note rather than a standalone customer intent.
  - The deletion constraint (cannot delete address with pending Subscribe and Save orders) is a condition of the `delete_address` action itself.
