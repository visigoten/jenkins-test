node {
   stage ('ocrun') {
     echo 'Ejecutando comando oc run...'  
     sh 'oc run pyvcloud  --env "ANSIBLE_PLAYBOOK=main-test.yml" --attach=True --leave-stdin-open=True --restart=Never --image=docker-registry.default.svc:5000/ansible/pyvcloud-testv5'
     echo 'Eliminando el pod: pyvcloud'
     sh 'oc delete pod/pyvcloud'
   }
}
