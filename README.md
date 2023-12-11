#install istio by istioctl : https://devocean.sk.com/blog/techBoardDetail.do?ID=163655

# Helm 저장소 구성
helm repo add istio https://istio-release.storage.googleapis.com/charts
helm repo update

# istio crds 설치
helm install istio-base istio/base -n istio-system --set defaultRevision=default

#istiod 설치
helm install istiod istio/istiod -n istio-system --wait





블로그 리스트
istioctl 설치 : https://devocean.sk.com/blog/techBoardDetail.do?ID=163655
istio 기본 설정 : https://gruuuuu.github.io/cloud/service-mesh-istio/
악분 블로그 : https://malwareanalysis.tistory.com/307#2.-ingress-gateway
nginx + istio : https://medium.com/@bob.s.walters/using-istio-with-nginx-ingress-for-a-b-service-shifting-7b39596db2fe
canary 배포 : https://devocean.sk.com/search/techBoardDetail.do?ID=164747&boardType=&query=istio&searchData=&page=&subIndex=&idList=,
https://medium.com/@domi.stoehr/canary-deployments-on-kubernetes-without-service-mesh-425b7e4cc862

현재 페이지 http://20.200.243.40/productpage

* istio로 하고 싶은 것
- canary 배포 및 특정 그룹만 테스트 진행
- azure dns와 연동

