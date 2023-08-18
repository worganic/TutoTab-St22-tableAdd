# WorganicTabV1 / v22 : Table/Add

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 16.1.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.


## Development server json

Run `json-server --watch db.json` for a dev server. Navigate to `http://localhost:3000/`.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Get clone 
> https://github.com/worganic/TutoTab-St22-tableAdd.git
> npm install
> cd .\worganic-tab-v22\
> ng serve

## Project :
v22 - Tableau -> Add

    - On rajoute l'option add :
        \src\app\component\users\users.component.ts
            >> options: any = {...
                'addData': true,// ...
    - On récupère l'option dans table :
        \src\app\shared\component\worg-table\worg-table.component.ts
            >> addData: boolean = false;
            >> this.addData = option['options']['addData'];
    - On rajoute la ligne de add :
        \src\app\shared\component\worg-table\worg-table.component.html
            >> <!-- row addData -->...
    - On ajoute le bouton addData dans la ligne de titre :
        \src\app\shared\component\worg-table\worg-table.component.html
            >> <!-- row title -->...
                <div *ngIf="column.column == 'delete' && optionAdd && !add">...</div>
    - 
        \src\app\shared\component\worg-table\worg-table.component.ts
            >> addData: boolean = false;
    - On met à jour la fct buttonFct avec addValid :
        \src\app\shared\component\worg-table\worg-table.component.ts
            >> if(action == 'editValid' || action == 'addValid'){
    - On ajoute l'option addValid à users :
        \src\app\component\users\users.component.ts
            >> if(data['action']== "addValid"){...
    - On ajoute le service :
        \src\app\shared\services\users.service.ts
            >> addUser(element: any) {...
    - On supprime l'element qui ne doit pas être enregistré (isExpand) :
        \src\app\shared\component\worg-table\worg-table.component.ts
            >> delete element.isExpand;


## Problème à résoudre :
    

## Infos plus :
   
## Update

## Historique :
Avant -> v21 - Tableau -> Button -> Edit -> selected
Après -> v23 - Tableau -> multiple
## Ressource :
    - Suppresion element d'un object :
    https://www.journaldunet.fr/web-tech/developpement/1441137-angular-comment-retirer-un-item-d-un-tableau-array-stocke/#:~:text=Pour%20supprimer%20un%20%C3%A9l%C3%A9ment%20d'un%20tableau%2C%20vous%20devez%20faire,que%20l'on%20souhaite%20supprimer.&text=On%20peut%20%C3%A9galement%20pr%C3%A9ciser%20en,que%20l'on%20souhaite%20supprimer.

## Abouts
created by Johann Loreau
create at 2023/08/17
Le project évolura suivant les remarques et conseils des visiteurs.