---
title: Shape Append-Klausel
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306447"
---
# <a name="shape-append-clause"></a>Shape Append-Klausel


**Gilt für**: Access 2013, Office 2013

The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.

## <a name="syntax"></a>Syntax

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Beschreibung

Die Teile dieser Klausel lauten wie folgt:

- *parent-command*

- Keiner oder einer der Folgenden (Sie können *parent-command* ganz weglassen):
    
  - Ein Anbieterbefehl in geschweiften Klammern ("{}"), der ein **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenprovider ausgegeben, und die Syntax hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.
    
  - Another shape command embedded in parentheses.
    
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
    
  - Another shape command embedded in parentheses.
    
  - Der Name eines vorhandenen geformten **Recordset**-Objekts.
    
  - Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.

- *child-alias*

  - Ein Alias, der auf das untergeordnete **Recordset** -Objekt verweist.

- *parent-column*

  - Eine Spalte im **Recordset**-Objekt, die von *parent-command* zurückgegeben wird.

- *child-column*

  - Eine Spalte im **Recordset**-Objekt, die von *child-command* zurückgegeben wird.

- *param-number*

  - Siehe [Verwenden von parametrisierten Befehlen](operation-of-parameterized-commands.md).

- *chapter-alias*

  - Ein Alias, der auf die dem übergeordneten Element angefügte Kapitelspalte verweist.


> [!NOTE]
> - Die _"Parent-column to child-column"_ -Klausel ist tatsächlich eine Liste, in der jede definierte Beziehung durch ein Komma getrennt ist.
> - Die Klausel hinter dem APPEND-Schlüsselwort ist tatsächlich eine Liste, in der die einzelnen Klauseln durch ein Komma getrennt werden und eine weitere Spalte definiert wird, die der übergeordneten Spalte angefügt werden soll.



## <a name="remarks"></a>Bemerkungen

Wenn Sie Anbieterbefehle aus Benutzereingaben als Teil eines SHAPE-Befehls erstellen, wird der vom Benutzer bereitgestellte Anbieterbefehl von SHAPE als undurchsichtige Zeichenfolge behandelt und originalgetreu dem Anbieter übergeben. Beispielsweise werden im folgenden SHAPE-Befehl

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE führt zwei Befehle aus: wählen \* Sie von T1 aus, \* und wählen Sie aus T2 Beziehung K1 zu K2 aus. Wenn der Benutzer einen Verbundbefehl bereitstellt, der aus mehreren durch Semikolons getrennten Anbieterbefehlen besteht, wird der Unterschied von SHAPE nicht erkannt. Im folgenden SHAPE-Befehl

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

Form führt Auswahl \* aus T1 aus; DROP TABLE T1 and (Select \* from T2 Relate K1 to K2), nicht erkennen, dass DROP TABLE T1 ein separates und in diesem Fall ein gefährlicher, Anbieterbefehl ist. Die Benutzereingabe muss von Anwendungen immer überprüft werden, um derartige potenzielle Hackerangriffe zu verhindern.

Dieser Abschnitt enthält die folgenden Themen:

- [Betrieb von nicht parametrisierten Befehlen](operation-of-non-parameterized-commands.md)

- [Betrieb von parametrisierten Befehlen](operation-of-parameterized-commands.md)

- [Hybrid Befehle](hybrid-commands.md)

- [Dazwischenliegende Shape COMPUTE-Klauseln](intervening-shape-compute-clauses.md)
