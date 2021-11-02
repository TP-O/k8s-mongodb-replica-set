# MongoDB Replica Set with Kubernetes

## QuickStart
Clone the source code.

```bash
$ git clone git@github.com:devops-config/k8s-mongodb-replica-set.git

$ cp ./k8s-mongodb-replica-set/keyfile/* ./k8s-mongodb-replica-set/
```

### Keyfile Security
Generate a key.
```bash
$ openssl rand -base64 756

<< 'EXAMPLE-OUTPUT'
ON+rfCAVesB0+NaW/DaVO/OOzFXH4l6kKV/IQ7k2zwf1EQkWt/7xWJKJEVhbUhO/
rWlH/7n9JDK0Mh5AziuejWj70QDq5QCmb/T5/+ZUlhT5g5r9xIeKy2x3gFcfEbw0
TZ/wfb0U/o7+s/wgcOUJnuzVhxx65BREDfqYPnJB7rQTe+9o/xXI4yXddu/oTQtD
eIHJKUJc0KhxXymcf02zsqbw38n7z54DCL+J9i0okVE2MWbDEwYfIPHNk+U8fSR8
W3Asie3dWArAoC06y3jKRGcCqEZZk5RHmg1zCEpsok7sp92x+8Xa91RTpJXtzuv7
E08o5yZ6/aJriJnZRaeYky7QNb2z+u9xRMII1+T/ha/c91VRNCgLWNNAsYxp8JzC
vAjLSHWQccaBhZrkJfwyumAzHMQoQN4qmrLw36UdeN8no9ip+dsJZLRkAivdxvUI
4lUuVEOZsHyT9K1bSfOaGf+xkKLazLrdCyqzArAGzd7nHy0Ry9+8P86WMV6FbHbo
LzEXtWqa4Rav5Xh9nIUBcvoP34uVThAPeNyyqSbrujknnWeH8umtaDi/nc/zr9dX
zm12j6haJXeLootet8yS5bS89Utl6Li4Darj/mDIsSx3rQ7YSZEIC0LrDF6o44d4
8PtD/TsU+e1CQbZyvjtiNqoB6wSOj8wE8N9kSc8BepETkRlT2CmIvKfKhqSmSseQ
D4HaIthynSzL1TSGTzMZXd2CsMQBTyPv5k5n983JYm7VNipxNqj9Y1rmGIrPcRlI
kD+kfdzBykQcZrJLFmEzXu7ob0/tFMTTBrgJHpNs3k6o7bk6lyLBzvc9GK+cTqCM
bzOdqgshMZHTHJhhsj6JdujLObwZx8hURgmQCRlEG/FhV19nbwhgpoPE2+uy68J/
OHyKul4r6i9gnxQsxEVI3ktNGvbszvVxUc+n3hQlNLA8quEEbt6LMAUmm0Caz3UV
udpuXzsBozqP2CS+FtLjKeEW/W3q7m7mROG7nN8ah1dSZLqI
EXAMPLE-OUTPUT
```

Copy the above command's output then paste it to `data.keyFile` in the file `4-mongo-security.yml`.

Apply the configurations.
```bash
$ kubectl apply -f ./k8s-mongodb-replica-set/
```

### X.509 Certificate
Updating...

## References:
- [https://www.spectrocloud.com/blog/kustomize-your-way-to-mongodb-replicaset/](https://www.spectrocloud.com/blog/kustomize-your-way-to-mongodb-replicaset/)
- [https://docs.mongodb.com/manual/tutorial/configure-x509-client-authentication/#std-label-x509-client-authentication](https://docs.mongodb.com/manual/tutorial/configure-x509-client-authentication/#std-label-x509-client-authentication)
- [https://goteleport.com/blog/securing-mongodb/](https://goteleport.com/blog/securing-mongodb/)
