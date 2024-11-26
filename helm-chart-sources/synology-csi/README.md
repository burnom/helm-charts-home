To install this chart please first create a secret named exactly as .Values.clientInfoSecretName

    kubectl create namespace synology-csi
    kubectl create secret -n synology-csi generic client-info-secret --from-file=config/client-info.yml
