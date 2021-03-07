# install PosgtreSQL 
1. https://www.docker.com/ 
2. https://docs.docker.com/compose/
3. https://helm.sh/
4. https://postgrespro.ru/docs/postgrespro/13/installation-bin
5. https://www.postgresql.org/download/windows/
6. https://postgrespro.ru/docs/postgrespro/13/binary-installation-on-windows#GUI-INSTALLATION-WIN
7. https://postgrespro.ru/docs/postgrespro/13/binary-installation-on-windows#WIN-CLI-INSTALLATION
8. https://www.postgresql.org/download/macosx/
9. https://brew.sh/
10. https://postgrespro.ru/docs/postgrespro/13/binary-installation-on-linux
11. https://releases.ubuntu.com/20.04/
12. https://dbeaver.io/
13. https://github.com/AbdulYadi/postgresql-private
14. https://cloud.google.com/



-- deploy VM on Google Comute Engine
gcloud beta compute --project=calm-tendril-290110 instances create postgres13 --zone=us-central1-a --machine-type=e2-medium --subnet=default --network-tier=PREMIUM --maintenance-policy=MIGRATE --service-account=322426944095-compute@developer.gserviceaccount.com --scopes=https://www.googleapis.com/auth/devstorage.read_only,https://www.googleapis.com/auth/logging.write,https://www.googleapis.com/auth/monitoring.write,https://www.googleapis.com/auth/servicecontrol,https://www.googleapis.com/auth/service.management.readonly,https://www.googleapis.com/auth/trace.append --image=ubuntu-2004-focal-v20200907  --image-project=ubuntu-os-cloud --boot-disk-size=10GB --boot-disk-type=pd-ssd --boot-disk-device-name=postgres13 --no-shielded-secure-boot --shielded-vtpm --shielded-integrity-monitoring --reservation-affinity=any