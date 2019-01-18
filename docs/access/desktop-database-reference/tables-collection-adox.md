---
title: Tables-Auflistung (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716172"
---
# <a name="tables-collection-adox"></a>Tables-Auflistung (ADOX)


**Betrifft**: Access 2013, Office 2013

Enthält alle [Table](table-object-adox.md)-Objekte eines Katalogs.

## <a name="remarks"></a>Hinweise

Die [Append](append-method-adox-tables.md)-Methode für eine **Tables** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen einer neuen Tabelle zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf eine Tabelle in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Tabellen, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen einer Tabelle aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

Einige Anbieter geben möglicherweise andere Schemaobjekte in der Tables-Auflistung zurück, z. B. eine Sicht. Bestimmte ADOX-Auflistungen können daher Verweise auf dasselbe Objekt enthalten. Wenn Sie das Objekt aus einer Auflistung löschen, wird diese Änderung in einer anderen Auflistung, die auf das gelöschte Objekt verweist, erst sichtbar, wenn für diese Auflistung die Refresh-Methode aufgerufen wird. Mit dem OLE DB-Anbieter für Microsoft Jet werden beispielsweise Sichten zusammen mit der Tables-Auflistung zurückgegeben. Wenn Sie eine Sicht löschen, müssen Sie die Tables-Auflistung zunächst aktualisieren, damit die Änderung für diese Auflistung angezeigt wird.

