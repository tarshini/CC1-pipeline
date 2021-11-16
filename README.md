# CC1-pipeline

Partie #1

1. destination_s3_bucket.tf et kinesis_datastream.tf sont les resources manquantes
2. et 3. voir captures d'écran 
4. elle permet d’écrire dans des flux de Amazon Kinesis Data Streams à l'aide de Kinesis Agent
5. il permet l’installation des composantes dans la VM EC2 pour l’exécution de l’aplication
6. son role est de collecter et formater les logs afin de les envoyer à kinesis data stream 
7. voir captures d'écran

Partie #2

1.	Ingestion : récupérer les données – Kinesis Datastream va les lire 
2.	Stockage : Lieu de réception des fichiers – Kinesis Firehorse va achenminer les données vers le bucket - demande au service s3 de stocker dans une bucket le stream de destination
3.	Transformation : les données sont intégréezs via datastream et Kinesis data Analytics va les transformer  
4.	Exposition : via des requêtes sql nous avons accès aux données transformées

Schema :

Fichier python <- kinesis agent <-> kinesis datastream <-> kinesis data anamytics -> kinesis firehorse -> bucket S3
