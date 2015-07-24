# Grafana
![rhtkua9t_reasonably_small](https://cloud.githubusercontent.com/assets/13198078/8878546/726a7d1e-3223-11e5-88d5-765a51eaa257.png)

## Dashboards

A default dashboard is available which creates a set of panels based on a JavaScript, stored under the public directory here:

  `dashboard/script/instance.js`

The script takes several parameters:

* env - the environment or namespace i.e. collectd, metrics (default: metrics)
* host - the Graphite host to connect to (default: http://localhost:8003)
* i - the instance name. This is the reversed FQDN i.e. uk.sirius-opg.dev.master-01

### Example

https://grafana.develop.sirius-opg.uk/dashboard/script/instance.js?host=https:%2F%2Fgraphite.develop.sirius-opg.uk&i=uk.sirius-opg.develop34.scratch-01&env=metrics


