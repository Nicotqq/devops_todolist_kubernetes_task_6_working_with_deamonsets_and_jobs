# Deployment Instructions

## Deploy

```bash
kubectl apply -f daemonset.yml
kubectl apply -f cronjob.yml
```

## Check resources

```bash
kubectl get daemonset -n todoapp
kubectl get cronjob -n todoapp
kubectl get jobs -n todoapp
kubectl get pods -n todoapp -o wide
```

## DaemonSet logs

```bash
kubectl logs -n todoapp -l app=todoapp
```

Follow logs:

```bash
kubectl logs -n todoapp -l app=todoapp -f
```

## CronJob logs

```bash
kubectl get jobs -n todoapp
kubectl get pods -n todoapp
```

## Check resources

```bash
kubectl describe daemonset todoapp-daemonset -n todoapp
kubectl describe cronjob todoapp-cronjob -n todoapp
```

## Cleanup

```bash
kubectl delete -f daemonset.yml
kubectl delete -f cronjob.yml
```
