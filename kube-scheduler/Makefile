VERSION?=latest

all:
	cp ../_output/release-stage/server/linux-amd64/kubernetes/server/bin/kube-scheduler ./
	docker build . -t kube-scheduler -t asia.gcr.io/olli-iviet/kube-scheduler:1.14.10-$(VERSION)
		docker push asia.gcr.io/olli-iviet/kube-scheduler:1.14.10-$(VERSION)
