# Hands-on With Intel Gaudi 3

These instructions will apply only for the duration of the Supercomputing 2025 conference.

## Connecting to Intel Gaudi 3

This assumes you are using a Linux or WSL shell.

1. During the tutorial, you should have received a paper with three `export` commands for `LOCAL_PORT`, `SERVER`, and `CARD`. Enter those commands in your shell. A password will also be disclosed to you.

2. Create an `ssh` tunnel with the following command. You will be asked **twice** to enter the password:
```
ssh -J milind@198.175.75.73:8005 -L $LOCAL_PORT:192.168.1.$SERVER:$CARD scintel@192.168.1.$SERVER
```

2. Visit the following URL in your browser. **Substitute $LOCAL_PORT with the value on your paper.**

```
http://localhost:$LOCAL_PORT/notebooks/Gaudi.ipynb
```

You should see a Jupyter notebook that executes an HPC workload on Gaudi 3.
