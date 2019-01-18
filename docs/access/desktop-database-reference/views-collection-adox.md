---
title: Views-Auflistung (ADOX)
TOCTitle: Views collection (ADOX)
ms:assetid: 8d0f9517-4be1-be9c-d4cd-6d50cd5a8983
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249618(v=office.15)
ms:contentKeyID: 48546246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ce9986d486eb76046216aabbce6352280042910
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719498"
---
# <a name="views-collection-adox"></a>Views-Auflistung (ADOX)


**Betrifft**: Access 2013, Office 2013

Enthält alle [View](view-object-adox.md)-Objekte eines Katalogs.

## <a name="remarks"></a>Hinweise

Die [Append](append-method-adox-views.md)-Methode für eine **Views** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen einer neuen Sicht zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf eine Sicht in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Sichten, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen einer Sicht aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

