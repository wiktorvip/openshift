# openshift


```
oc extract secret/alertmanager-main --confirm -n openshift-monitoring

Edit alertmanager.yaml 

oc create secret generic alertmanager-main --from-file=alertmanager.yaml=alertmanager.yaml -n openshift-monitoring --dry-run=client -o yaml | oc replace -f -

oc delete pod -l alertmanager=main -n openshift-monitoring

```