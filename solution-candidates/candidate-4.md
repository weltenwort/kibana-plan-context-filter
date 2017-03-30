# Solution 4: Create a filter based on preconfigured settings

## Outline

1. The user configures sets of filters for the index pattern that defined 
   contexts.
2. The user creates a set of filters and a query to identify the anchor event.
3. The user clicks the UI element to switch to the context view with a specific 
   preconfigured set of filters.
4. The context view is filtered by the preconfigured set of filters.

## Discussion

* **PRO**: The context can be defined via multiple filters.
* **PRO**: The context is immediately "useful".
* **CON**: The concept of sets of filters that can be preconfigured is new to 
  Kibana and would require significant design and implementation effort.
