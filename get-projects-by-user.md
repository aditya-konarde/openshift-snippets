# Get a list of all OpenShift projects created by a specific user: 

`$USER='NAME'`
`oc get projects -o jsonpath='{"Project Name: "}{range .items[*].metadata}{.name}{" "}{.annotations.openshift\.io/requester}{" \n"}' | grep $USER | awk {'print $1'}`
