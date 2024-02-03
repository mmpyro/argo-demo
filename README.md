# Port forward

```sh
kubectl -n argo port-forward deployment/argo-server 2746:2746
```

```sh
kubectl port-forward -n argo-events svc/webhook-eventsource-svc 12000:12000
```

# Commands

```sh
curl -XPOST http://localhost:12000/example -H 'Content-type: application/json' -d '{"message": "hello Azure", "delay": 15}'
```

```sh
argo submit --from workflowtemplate/workflow-template-submittable
argo submit --from workflowtemplate/workflow-template-submittable --parameter delay=20

```