# K8S-demo
Implementation of webapp with mongodb in k8s using minikube
                                                            Minikube-projet


Error:
W1019 18:19:54.812895   11060 main.go:291] Unable to resolve the current Docker CLI context "default": context "default": context not found: open C:\Users\anas\.docker\contexts\meta\37a8eec1ce19687d132fe29051dca629d164e2c4958ba141d5f4133a33f0688f\meta.json: Le chemin d’accès spécifié est introuvable.
* minikube v1.31.2 sur Microsoft Windows 10 Pro 10.0.19045.3570 Build 19045.3570
Answer:
Le message d'erreur indique que le contexte Docker actuel, "default", est introuvable. Cela peut être dû à plusieurs raisons, notamment :
Le contexte n'a pas été créé.
Le contexte a été supprimé.
Le chemin d'accès au contexte est incorrect.
Dans ce cas, le chemin d'accès au contexte est C:\Users\anas.docker\contexts\meta\37a8eec1ce19687d132fe29051dca629d164e2c4958ba141d5f4133a33f0688f\meta.json. Si ce chemin d'accès est correct, vous pouvez essayer de créer ou de restaurer le contexte.
Pour créer un nouveau contexte, exécutez la commande suivante :
docker context create <nom-du-contexte>
Par exemple, pour créer un contexte nommé "my-context", exécutez la commande suivante :
docker context create my-context
Pour restaurer un contexte existant, exécutez la commande suivante :
docker context load <chemin-vers-le-contexte>
Par exemple, pour restaurer un contexte nommé "my-context" qui se trouve dans le répertoire C:\Users\anas.docker\contexts, exécutez la commande suivante :
docker context load C:\Users\anas\.docker\contexts\my-context.json
Une fois que vous avez créé ou restauré le contexte, vous pouvez l'activer en exécutant la commande suivante :
docker context use <nom-du-contexte>
Par exemple, pour activer le contexte nommé "my-context", exécutez la commande suivante :
docker context use my-context
Si vous avez suivi ces étapes et que vous obtenez toujours le même message d'erreur, vous pouvez contacter le support Docker pour obtenir de l'aide.
En plus de la solution ci-dessus, vous pouvez également essayer les solutions suivantes :
Vérifier que Docker est installé et en cours d'exécution.
Redémarrer Docker.
Redémarrer votre ordinateur.
J'espère que cela vous aidera!

Setup minikube on widows using powershell:

![image](https://github.com/Dmtry32/K8S-demo/assets/88732558/caa01673-2ebc-4e2f-a2f3-0e4f31cd6fda)








Projet: Impelementation of webapp with mogodb database that iclude creation of 4 file 
Steps: every configuration file has 3 part 
-metadata 
-specification that hold all kind of configuration  that we need to apply 
-status atomatically and aded by K8S




![image](https://github.com/Dmtry32/K8S-demo/assets/88732558/a566db7c-99d9-4921-b9c5-f5d41e7282d2)


Create a externel configuration in k8s cluster


![image](https://github.com/Dmtry32/K8S-demo/assets/88732558/098bd1d4-931d-46d5-97df-18a9159bf479)




access to web apllication using browser 


![image](https://github.com/Dmtry32/K8S-demo/assets/88732558/7cb1f469-8d25-481a-8cff-845f3c1ade46)


