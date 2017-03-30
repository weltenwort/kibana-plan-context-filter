# Solution 1: Apply a subset of filter from Discover after switching

## Outline

1. The user creates a set of filters and a query to identify the anchor event.
2. The user clicks the UI element to switch to the context view.
3. The context view is shown asking the user to select a subset of the 
   previously applied filters to apply them to the context view.

## Discussion

* **PRO**: Asking the user for a set of filters to apply is a concept already 
  used when filtering in visualizations.
* **PRO**: The context can be defined via multiple filters.
* **CON**: The set of filters in Discover might not contain the filters 
  required to establish a "context", either because the user used the query bar 
  to narrow down the Discover result set or because the criteria just don't 
  overlap.
* **CON**: The context view requires retroactive setup to be "useful".
