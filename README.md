# Splunk Caching Dashboard Example
Often customers want to have a dashboard that loads quickly when they use it and Splunk will advise to use scheduled saved searches to pre-cache the results.  This is great, but the customer often has dashboards that are only used once a month, but when they are used they are used by lots of people at the same time.  These customers want the benefits of cached results, but do not want the penalty of having to generate results unnecessarily when the dashboard is not being used.
The technique demonstrated in this app is a happy medium, but is at the expense of dashboard complexity.
The approach used here is to check if cached results exist on panel load, if they do then they are used in the panel, if they don't already exist then the searches run in the dashboard and create the cache, any others that load the dashboard after the cached results are created use that instead.

