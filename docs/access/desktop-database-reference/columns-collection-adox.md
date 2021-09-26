---
title: Columns-Auflistung (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c06199be9f5d5145e4fe205a3f42a91cd39f717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612330"
---
# <a name="columns-collection-adox"></a>Columns-Auflistung (ADOX)


**Gilt für**: Access 2013, Office 2013

Enthält alle [Column](column-object-adox.md)-Objekte einer Tabelle, eines Indexes oder eines Schlüssels.

## <a name="remarks"></a>HinwBemerkungeneise

Die [Append](append-method-adox-columns.md)-Methode für eine **Columns** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen einer neuen Spalte zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf eine Spalte in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Spalten, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen einer Spalte aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.


> [!NOTE]
> Es tritt ein Fehler auf, wenn ein **Column**-Objekt an die **Columns**-Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column**-Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.


