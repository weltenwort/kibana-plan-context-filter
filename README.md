# Filters in the Kibana Context View

## Problem Statement

Centralized logging with Elasticsearch and Kibana is particularly valuable for 
large amounts of log data from numerous sources. For large amounts of log 
entries however, the current context view loses most of its usefulness, because 
log entries not related to the anchor entry swamp the relevant entries in the 
context.

## Discussion

The concept of the context view is to loosen the potentially very narrow 
filters used to find a particular event in the Discover view to allow for a 
broader inspection of the "relevant" events in the system immediately leading 
up to (or following) the event. This misleadingly suggests that the latter set 
of filters is a subset of the former, which might not even be the case in most 
circumstances. Another, maybe less misleading formulation would be that we want 
to provide a way for the user to tell Kibana what makes up the "relevant 
context" for the event so Kibana. So far the context view only uses adjacency 
in time as a criterion.

To summarize some observations about the two sets of filters:

* The set of filters to find the anchor document and the set of filters 
  defining the context might be disjunct. (See Use Case 1 as an example.)
* In addition to adjacency in time, the context might be defined by more than 
  one criterion (e.g. server + process name).
* Some problems might require investigation from different angles (i.e. 
  different definitions of "context").

## Abstract Formulation

It should be possible to limit the entries shown in the context view to those
"relevant" to the event the user is inspecting. This translates to the ability
to apply filters to the context view that are different from the filters used
to identify the original log entry.

## Possible Solutions

* [Solution 1](./solution-candidates/candidate-1.md): Apply a subset of filters 
  from Discover when switching
* [Solution 2](./solution-candidates/candidate-2.md): Create a filter based on 
  a field selected by the user when switching
* [Solution 3](./solution-candidates/candidate-3.md): Create a filter based on 
  fields selected by the user after switching
* [Solution 4](./solution-candidates/candidate-4.md): Create a filter based on 
  preconfigured settings

## Example Use Cases

* [Use Case 1](./use-cases/use-case-1.md): Error identification and investigation
