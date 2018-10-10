---
title: Columns-Auflistung (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475461"
---
# <a name="columns-collection-adox"></a>Columns-Auflistung (ADOX)


**Betrifft**: Access 2013 | Office 2013

Enthält alle [Column](column-object-adox.md)-Objekte einer Tabelle, eines Indexes oder eines Schlüssels.

## <a name="remarks"></a>Hinweise

Die [Append](append-method-adox-columns.md)-Methode für eine **Columns** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen einer neuen Spalte zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf eine Spalte in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Spalten, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen einer Spalte aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.


> [!NOTE]
> <P>[!HINWEIS] Es tritt ein Fehler auf, wenn ein <STRONG>Column</STRONG> -Objekt an die <STRONG>Columns</STRONG> -Auflistung eines <A href="index-object-adox.md">Index</A>-Objekts angefügt wird und das <STRONG>Column</STRONG> -Objekt nicht in einem <A href="table-object-adox.md">Table</A>-Objekt vorhanden ist, das bereits an die <A href="tables-collection-adox.md">Tables</A>-Auflistung angefügt wurde.</P>


