---
title: Append-Klausel für Formen
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6460572f44e79fe4bdb30d1ca33810d610da9721
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473157"
---
# <a name="shape-append-clause"></a>Append-Klausel für Formen


**Betrifft**: Access 2013 | Office 2013

Mit der APPEND-Klausel des Shape-Befehls werden einem Recordset-Objekt Spalten angefügt. Bei diesen Spalten handelt es sich oft um Kapitelspalten, die auf ein untergeordnetes Recordset-Objekt verweisen.

## <a name="syntax"></a>Syntax

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Beschreibung

Die Teile dieser Klausel lauten wie folgt:

- *parent-command*

- NULL oder eins der folgenden (Sie können die *Parent-Command* ganz weglassen):
    
  - Ein Anbieterbefehl in geschweiften Klammern ("{}"), der ein **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenprovider ausgegeben, und die Syntax hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.
    
  - Ein weiterer in Klammern eingebetteter Shape-Befehl.
    
  - Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.

- *parent-alias*

  - Ein optionaler Alias, das auf das übergeordnete **Recordset** -Objekt verweist.

- *column-list*

  - Mindestens eines der Folgenden:
    
    - Eine Aggregatspalte.
    
    - Eine berechnete Spalte.
    
    - Eine neue Spalte, die mit der NEW-Klausel erstellt wird.
    
    - Eine Kapitelspalte. Eine Kapitelspaltendefinition wird in Klammern ("()") eingeschlossen. Siehe nachstehende Syntax:


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- *child-recordset*

  - Ein Anbieterbefehl in geschweiften Klammern ("{}"), der ein **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenprovider ausgegeben, und die Syntax hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.
    
  - Ein weiterer in Klammern eingebetteter Shape-Befehl.
    
  - Der Name eines vorhandenen geformten **Recordset** -Objekts.
    
  - Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.

- *child-alias*

  - Ein Alias, der auf das untergeordnete **Recordset** -Objekt verweist.

- *parent-column*

  - Eine Spalte im **Recordset-Objekt** zurückgegeben wird, durch die *Parent-Command.*

- *child-column*

  - Eine Spalte im **Recordset**-Objekt, die von *child-command* zurückgegeben wird.

- *param-number*

  - Siehe [Verwenden von parametrisierten Befehlen](operation-of-parameterized-commands.md).

- *chapter-alias*

  - Ein Alias, der auf die dem übergeordneten Element angefügte Kapitelspalte verweist.


> [!NOTE]
> - Die Klausel _"Parent-Column TO untergeordnete Spalte"_ ist tatsächlich eine Liste, in der einzelnen definierten Beziehungen durch ein Komma getrennt.
> - [!HINWEIS] Die Klausel hinter dem APPEND-Schlüsselwort ist tatsächlich eine Liste, in der die einzelnen Klauseln durch ein Komma getrennt werden und eine weitere Spalte definiert wird, die der übergeordneten Spalte angefügt werden soll.



## <a name="remarks"></a>Hinweise

Wenn Sie Anbieterbefehle aus Benutzereingaben als Teil eines SHAPE-Befehls erstellen, wird der vom Benutzer bereitgestellte Anbieterbefehl von SHAPE als undurchsichtige Zeichenfolge behandelt und originalgetreu dem Anbieter übergeben. Beispielsweise werden im folgenden SHAPE-Befehl

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

Shapes werden zwei Befehle ausgeführt: Wählen Sie \* von t1 und (Wählen Sie \* aus t2 verknüpfen k1 TO K2). Wenn der Benutzer einen Verbundbefehl bereitstellt, der aus mehreren durch Semikolons getrennten Anbieterbefehlen besteht, wird der Unterschied von SHAPE nicht erkannt. Im folgenden SHAPE-Befehl

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE führt SELECT- \* von t1; Drop t1-Tabelle und (Wählen Sie \* aus t2 verknüpfen k1 TO K2), ohne zu realisieren Drop Tabelle t1 ist eine Separate und in diesem Anbieterbefehl Groß-/Kleinschreibung, gefährlicher,. Die Benutzereingabe muss von Anwendungen immer überprüft werden, um derartige potenzielle Hackerangriffe zu verhindern.

