---
title: Indexes-Auflistung (ADOX)
TOCTitle: Indexes Collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3dbc32da7580aa4e4c222c20131cda2adefdb50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472671"
---
# <a name="indexes-collection-adox"></a>Indexes-Auflistung (ADOX)


**Betrifft**: Access 2013 | Office 2013

Enthält alle [Index](index-object-adox.md)-Objekte einer Tabelle.

## <a name="remarks"></a>Hinweise

Die [Append](append-method-adox-indexes.md)-Methode für eine **Indexes** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen eines neuen Indexes zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf einen Index in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Indizes, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen eines Indexes aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

