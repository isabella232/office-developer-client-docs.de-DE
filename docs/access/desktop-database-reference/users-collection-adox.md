---
title: Users-Auflistung (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d68dc2dd368523e8ca3dd04a06008cea9bef337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473111"
---
# <a name="users-collection-adox"></a>Users-Auflistung (ADOX)


**Betrifft**: Access 2013 | Office 2013

Enthält alle gespeicherten [User](user-object-adox.md)-Objekte eines Katalogs oder einer Gruppe.

## <a name="remarks"></a>Hinweise

Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.

Die [Append](append-method-adox-users.md)-Methode für eine **Users** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen eines neuen Benutzers zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf einen Benutzer in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Benutzer, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen eines Benutzers aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.


> [!NOTE]
> <P>[!HINWEIS] Bevor ein <STRONG>User</STRONG> -Objekt an die <STRONG>Users</STRONG> -Auflistung eines <STRONG>Group</STRONG> -Objekts angefügt wird, muss ein <STRONG>User</STRONG> -Objekt mit demselben <A href="name-property-adox.md">Namen</A> wie das anzufügende Objekt bereits in der <STRONG>Users</STRONG> -Auflistung des <STRONG>Catalog</STRONG> -Objekts vorhanden sein.</P>


