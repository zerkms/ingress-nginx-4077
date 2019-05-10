How to use it
=============

1. Deploy all manifests
1. Run

        while true; do; echo -n `date +"[%m-%d %H:%M:%S]"`; r=$RANDOM; curl -s -o /dev/null -w "%{http_code}" -H "Host: ingress-nginx-4077" <ingress-ip>/\?$r; echo " $r"; sleep 0.1; done;

1. Change the `FOO` environment variable value in the deployment and redeploy
1. See that it was some 502s
