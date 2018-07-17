# Lists all the Pods and their respective images currently in use

# Across all namespaces:
`oc get pods --all-namespaces -o jsonpath="{range .items[*]}{.metadata.name}{\" \"}{.spec.containers[*].image}{\"\n\"}{end}"`

# For a single namespace:
`oc get pods -n namespace_name -o jsonpath="{range .items[*]}{.metadata.name}{\" \"}{.spec.containers[*].image}{\"\n\"}{end}"`
