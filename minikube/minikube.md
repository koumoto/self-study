# minikubeのインストール

## kubectlをインストール

`curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.0/bin/windows/amd64/kubectl.exe`

- パスを通す

## chocolateをインストール

- 管理者権限で実行

## minikubeのインストール
- choco install minikube(管理者権限)

- minikube start
失敗

### バーチャルボックスをインストール
- minikube start
失敗

### hyper-Vを有効化
- Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
失敗

### hyper-V　コンソール画面から変更
https://qiita.com/ohhara_shiojiri/items/801a24a2c94ff93be82d

- 再起動

管理者権限で
- `minikube start --vm-driver=hyperv`
動いた!!!
virtualbox hyper-v 両方入ってるとこのオプションが必要?

`kubectl version`で動いていることを確認

`kubectl get componentstatuses`

シングルノードで動いている

```
NAME                 STATUS    MESSAGE             ERROR
controller-manager   Healthy   ok
scheduler            Healthy   ok
etcd-0               Healthy   {"health":"true"}
```

`kubectl get nodes`

```
NAME       STATUS   ROLES    AGE     VERSION
minikube   Ready    master   5m12s   v1.15.2
```
`kubectl describe node minikube`
