# Guide d'utilisation de `gsutil` pour le transfert de données vers un bucket GCP

## Installation de Google Cloud SDK et `gsutil`

1. Téléchargez et installez le [Google Cloud SDK](https://cloud.google.com/sdk/docs/install).

2. Assurez-vous d'avoir le `gsutil` installé avec le SDK. Vous pouvez vérifier cela en exécutant la commande suivante dans votre terminal :
    ```bash
    gcloud components install gsutil
    ```

## Authentification avec Google Cloud

1. Connectez-vous à votre compte Google Cloud en utilisant la commande :
    ```bash
    gcloud auth login
    ```

2. Suivez les étapes à l'écran pour autoriser l'accès à votre compte Google Cloud.

## Transfert de données vers un bucket GCP

1. Utilisez la commande suivante pour transférer un dossier local vers le bucket GCP (assurez-vous de remplacer `<local_folder>` par le chemin de votre dossier local) :
    ```bash
    gsutil -m cp -r <local_folder> gs://cdr-opco-2i-20231030-input_folder/
    ```
   - L'option `-m` permet de paralléliser le transfert, accélérant ainsi le processus.

2. Suivez les messages de progression pour surveiller le transfert.

   Félicitations, vous avez maintenant transféré avec succès des données depuis votre serveur local vers le bucket GCP `gs://cdr-opco-2i-20231030-input_folder/` en utilisant `gsutil` !
