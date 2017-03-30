# Solution 3: Create a filter based on fields selected by the user after 
switching

## Outline

1. The user creates a set of filters and a query to identify the anchor event.
2. The user clicks the UI element to switch to the context view.
3. The context view is unfiltered.
4. The user expand one of the documents and clicks the filter icons for the 
   fields required to establish the context.

## Discussion

* **PRO**: Actions for individual fields in the expanded details of a row is a 
  concept already established in the document table.
* **PRO**: The context can be defined via multiple filters.
* **CON**: The context view requires retroactive setup to be "useful".
