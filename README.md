# CKA-CKAD-bookmarks
My personal bookmarks for the CKA and CKAD exams

The first two actions on the exam are:

Create the following `~./.vimrc`
```
:set sw=2 ts=2 sts=2
:set et
:set autoindent
:set number
```

Setup the `kdo alias`
```
# export alias kdo='kubectl --dry-run=client -oyaml'
```

Saves time typing:

```
# kubectl run --image nginx pod --dry-run=client -oyaml > pod.yml`
# kdo run --image nginx > pod.yml
```

### General takeaways

* I created everything done with imparitive commands as a file and then a `k apply -f`. In practice it saved my a lot of time to be able to do quick edit and tweaks
* `v` get in Vim select mode. `y` is copy. `>` puts an indent on the selection and with `.` you can indent the same text again without selecting.
* Make sure to NOT overwrite an path given in the question. For example save the ETCD snapshot to the homedir and then move it to the given path to avoid saving the snapshot over a file needed for the restore.

### Personal favorite bookmark:

https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands

Gives ready to use examples and easy to search through all the kubectl commands instead of doing --help each time.
