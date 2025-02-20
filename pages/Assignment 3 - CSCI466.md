## Entities
**City**($$\underline{\text{City}},\underline{\text{State}},\text{Headquarters})$$

**Product**($$\underline{\text{ProductID}},\text{Weight},\text{Color},\text{Description},\text{Dimensions})$$

**Order**($$\underline{\text{OrderNo}},\text{Date},\text{Name}^\dagger)$$
...where $$(\text{Name})$$ identifies the **Client** who placed the order

**Client**($$\underline{\text{Name}},\text{Address},\text{Email})$$

**Warehouse**($$\underline{\text{ID}},\text{Manager},\text{Address},\text{City}^\dagger,\text{State}^\dagger)$$
...where $$(\text{City}, \text{State})$$ identifies a **City** in which the warehouse is located
- ## Relations
  **ProductStoredInCity**$$(\underline{\text{ProductID}}^\dagger, \underline{\text{City}}^\dagger, \underline{\text{State}}^\dagger, \text{Quantity})$$
  ...where $$(\text{City}, \text{State})$$ identifies a **City**
  ...and $$(\text{ProductID})$$ identifies a **Product**
  
  **WarehouseHoldsProduct**$$(\underline{\text{ID}}^\dagger, \underline{\text{ProductID}}^\dagger, Quantity$$
  ...where $$(\text{ID})$$ identifies a **Warehouse**
  ...and $$(\text{ProductID})$$ identifies a **Product**
  
  **ProductInOrder**$$(\underline{\text{ProductID}}^\dagger,\underline{\text{OrderNo}}^\dagger, \text{Quantity})$$
  ...where $$(\text{ProductID})$$ identifies a **Product**
  ...and $$(\text{OrderNo})$$ identifies an **Order**