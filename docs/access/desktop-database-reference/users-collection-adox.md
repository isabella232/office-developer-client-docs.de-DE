---
title: Users-Auflistung (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3d91af56dc37cf8719a241a35046d663f7c9d57
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998071"
---
# <a name="users-collection-adox"></a>Users-Auflistung (ADOX)

**Betrifft**: Access 2013, Office 2013

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
> [!HINWEIS] Bevor ein **User** -Objekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **User** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Users** -Auflistung des **Catalog** -Objekts vorhanden sein.

