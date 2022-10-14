# Cours Linux 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Linux - TP 2 : 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Exercice 1 : Permissions
* **Question 1:** Créer le fichier toto dans le répertoire tp1droits à l’aide de touch. Vous pouvez voir les droits de ce fichier en utilisant la commande ls -l.

![image](https://user-images.githubusercontent.com/91763346/195916374-880a43c9-ff98-4eb1-a25e-708050db456f.png)

* **Question 2 :** Changez ces droits du répertoire tp1droits en rwxr-x--x en utilisant la notation octale.

![image](https://user-images.githubusercontent.com/91763346/195916522-4759bb29-8316-452b-9071-5386e7a6a845.png)

* **Question 3 :**  Changez les droits en -wx-w---x en utilisant la notation symbolique.

![image](https://user-images.githubusercontent.com/91763346/195916886-00fc70f3-c8ac-42ce-9d1e-81c42667217a.png)


* **Question 4 :**  Créez un fichier (non répertoire) tp1 dans le répertoire tp1droits.

![image](https://user-images.githubusercontent.com/91763346/195917035-126fedf2-465d-4524-ab74-791dc8922968.png)


* **Question 5 :**  À l’aide de la commande ls vérifiez la taille du fichier tp1.

![image](https://user-images.githubusercontent.com/91763346/195917035-126fedf2-465d-4524-ab74-791dc8922968.png)

* **Question 6 :**  Changez les droits de tp1droits en --xr-x--- en utilisant la notation octale.

![image](https://user-images.githubusercontent.com/91763346/195917456-eafdb9db-ec7c-455f-bf2d-c683a1eed7b6.png)


* **Question 7 :**  Créez un fichier tp1bis dans le répertoire tp1droits. Quel est le résultat ? Pourquoi ?

![image](https://user-images.githubusercontent.com/91763346/195917644-3e004fc3-3116-4670-82ee-0b609d395baf.png)

On n'arrive pas a créér le fichier car on n'a pas le droit d'écrire (w).

* **Question 8 :**  Changez les droits en rw----r-- en utilisant la notation symbolique.

![image](https://user-images.githubusercontent.com/91763346/195918018-3aee1da4-0de5-4f57-8658-696e132aefee.png)


* **Question 9 :**  Essayez d’accéder au répertoire tp1droits à l’aide de la commande cd. Quel est le résultat ? Pourquoi ?

![image](https://user-images.githubusercontent.com/91763346/195918263-04c195fb-deb8-40a4-b601-33e58008f660.png)

On n'arrive pas a accéder le répertoire **t1pdroits** car il nous manque le droit d'éxecution (X).
Il faut aussi noter que en Linux si on n'a pas le droit "x" on ne peut ni écrire dessous ni l'accéder meme si on a le "w" / "r".



* **Question 10 :**  Sans changer les droits d’accès à tp1droits créez un fichier tp2ter dans le répertoire
tp1droits. La création du fichier a-t-elle réussi ? Pourquoi ?

![image](https://user-images.githubusercontent.com/91763346/195918956-f196b1bc-39e3-470f-95ad-95f87f10412a.png)

Il faut aussi noter que en Linux si on n'a pas le droit "x" on ne peut ni écrire dessous ni l'accéder meme si on a le "w" / "r".
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Exercice 2 : Utilisation du système de fichiers LINUX

* **Question 1:**  Positionnez-vous sous votre répertoire de connexion.

Pour notre cas, j'ai choisit de créer un nouveau  répertoire à la place d'utiliser mon répertoire de connexion.

![image](https://user-images.githubusercontent.com/91763346/195919373-42339d70-d545-4fb8-a10f-420f062bf3ae.png)

* **Question 2:**  Créez sous votre répertoire de connexion deux répertoires de noms tp et TMP.

![image](https://user-images.githubusercontent.com/91763346/195919373-42339d70-d545-4fb8-a10f-420f062bf3ae.png)

* **Question 3:**  Copiez les fichiers passwd, group et hosts du répertoire /etc sous votre répertoire de connexion.

![image](https://user-images.githubusercontent.com/91763346/195919992-e5de2016-aaf5-48bd-abe9-73ffa6438d46.png)

on utilise la commande 
``` 
cp /etc/passwd . 
```

* **Question 4:**  Dupliquez passwd sous votre répertoire de connexion, sous le nom password.

![image](https://user-images.githubusercontent.com/91763346/195920220-338c5f7e-18fb-4a70-8c40-aea62927fc10.png)

* **Question 5:**  Déplacez hosts sous tp en le renommant en hotes.

![image](https://user-images.githubusercontent.com/91763346/195920335-50d3ec90-d504-4183-84d0-29221d2562de.png)


* **Question 6:**  Détruisez le fichier password.

![image](https://user-images.githubusercontent.com/91763346/195920455-00e949fa-2e78-4efe-8ac9-b3d5f2411403.png)

* **Question 7:**  Essayez de détruire le répertoire tp avec rmdir Justifiez le message d’erreur obtenu.

![image](https://user-images.githubusercontent.com/91763346/195920603-3b1707b7-443b-41dc-8d3c-79273a3edd17.png)

On ne peut pas effacer le répertoire tp car il contient des fichiers. on peut utiliser. Pour le forcer on peut utiliser rm -rf .

* **Question 8:**  Déplacez group et hotes vers TMP.

```
  >$ mv hotes ./tmp
  >$ mv group ./tmp
```

* **Question 9:**  Détruisez le répertoire tp.

![image](https://user-images.githubusercontent.com/91763346/195921765-ef9123c9-00aa-4b41-a840-1f7b6d1d9c34.png)

Pour pouvoir détruire le répertoire tp, on a déplacer son contenu vers tmp.

* **Question 10:**  Renommez le répertoire TMP en tmp.

![image](https://user-images.githubusercontent.com/91763346/195922040-47f15c62-2d39-458d-899d-f196a8c8ac08.png)

* **Question 11:**  Affichez le contenu des fichiers hotes et passwd page par page.

![image](https://user-images.githubusercontent.com/91763346/195922365-30b937f0-3b61-43fd-909a-eeb410e142f6.png)

![image](https://user-images.githubusercontent.com/91763346/195922553-75a322a6-0311-4e85-b9f9-958d48b4b618.png)

* **Question 12:**  Observez la différence d’affichage de ls -l tmp et de ls -ld tmp.

![image](https://user-images.githubusercontent.com/91763346/195922886-a9db200d-be68-4324-8664-9c82305c5651.png)

```
 . >$ ls -l tmp affiche les détails sur le contenu du /tmp.
 . >$ ls -ld tmp affiche les détails sur /tmp.
```
* **Question 13:**  Donnez la date de dernière modification du répertoire tmp.

![image](https://user-images.githubusercontent.com/91763346/195923285-7612b027-178d-4b67-8e6f-f0efc3dbac02.png)

* **Question 14:**  Donnez la taille du fichier hotes.

![image](https://user-images.githubusercontent.com/91763346/195923493-584f4f50-ecb8-4f76-801a-1061962b7af9.png)


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Exercice 3 :  man, la commande la plus importante de toutes



* **Question 1:**   Tester les commandes suivantes, commenter les résultats obtenus.

![image](https://user-images.githubusercontent.com/91763346/195923743-c8e84c8d-1b56-4a1a-bf83-248d4dd8fa4f.png)

![image](https://user-images.githubusercontent.com/91763346/195923816-d5e8fb23-2921-45ad-b8f6-6c8f53744abf.png)

* **Question 2:**   Voir la page de manuel de touch. À quoi sert ce programme, si ce n’est à créer des fichiers vides ? À quoi sert l’option -c ? La tester.

```
Update the access and modification times of each FILE to the
       current time.

       A FILE argument that does not exist is created empty, unless -c
       or -h is supplied.

       A FILE argument string of - is handled specially and causes touch
       to change the times of the file associated with standard output.

       Mandatory arguments to long options are mandatory for short
       options too.
```

l'argument -c nous aide a ne pas créer un fichier si on utilise touch, mais juste de mettre a jour le timestamp.

* **Question 3:**   Voir la page de manuel de touch. À quoi sert ce programme, si ce n’est à créer des fichiers vides ? À quoi sert l’option -c ? La tester.

*deja répondu*

* **Question 4:**   Voir la page de manuel de touch. À quoi sert ce programme, si ce n’est à créer des fichiers vides ? À quoi sert l’option -c ? La tester.

```
DESCRIPTION        
       man is the system's manual pager.  Each page argument given to man is normally the name of a program, utility or function.  The manual page associated with each of these arguments is then found and displayed.  A section, if provided, will direct man to look only in that section of the manual.  The default action is to
       search in all of the available sections following a pre-defined order (see DEFAULTS), and to show only the first page found, even if page exists in several sections.

       The table below shows the section numbers of the manual followed
       by the types of pages they contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
       7   Miscellaneous (including macro packages and conventions),
           e.g. man(7), groff(7)
       8   System administration commands (usually only for root)
       9   Kernel routines [Non standard]

       A manual page consists of several sections.
```
![image](https://user-images.githubusercontent.com/91763346/195925969-7d610eb0-2a2f-48ac-bbf3-3a932609f935.png)

![image](https://user-images.githubusercontent.com/91763346/195926032-cd66ec2b-2d18-4338-b1f5-1ef04c973456.png)

