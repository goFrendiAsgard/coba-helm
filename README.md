# Apa ini

Bukan apa-apa, cuma coba belajar helm saja. Artikel:

* https://wkrzywiec.medium.com/deployment-of-multiple-apps-on-kubernetes-cluster-walkthrough-e05d37ed63d1
* https://wkrzywiec.medium.com/how-to-deploy-application-on-kubernetes-with-helm-39f545ad33b8
* https://medium.com/swlh/how-to-declaratively-run-helm-charts-using-helmfile-ac78572e6088

# Bagaimana menjalankan ini

Lihat `do.sh`

```
kubectl config view
kubectl config use-context docker-desktop
helmfile repos
helmfile sync
```

# Kasih penjelasan dikit dong

helmfile (lihat `helmfile.yaml`) memungkinkanmu untuk deploy beberapa chart dengan satu perintah saja: `helmfile sync`.

Di sini, ada 3 charts yang di dipakai:

* `stable/nginx-ingress` dari repo external untuk `ingress-backend`
* `./charts/ingress` untuk `ingress-controller`
* `./charts/app` untuk `fibo` dan `myservice`

Untuk lebih jelasnya baca tiga artikel medium di atas.