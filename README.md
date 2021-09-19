1. Create cluster
    ```
    eksctl create cluster -f cluster.yaml
    ```

2. Enable Flux in the EKSctl cluster
    ```
    eksctl enable flux -f cluster.yaml
    ```


kubectl -n flux-system create secret generic discord-url \
--from-literal=address=https://discord.com/api/webhooks/889109343868452934/50WbD3TYBy1C8A7gZ9NmbGQ7H-W5TWjEymmh2QK-T5Zyk3VVNCROpB6xjewNTh9uGysD    s