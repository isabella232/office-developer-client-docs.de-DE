---
title: Keys-Auflistung (ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 82718af6378b13c4b0350dca84a84f06afd682de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626344"
---
# <a name="keys-collection-adox"></a>Keys-Auflistung (ADOX)


**Gilt für**: Access 2013, Office 2013

Enthält alle [Key](key-object-adox.md)-Objekte einer Tabelle.

## <a name="remarks"></a>Bemerkungen

Die [Append](append-method-adox-keys.md)-Methode für eine **Keys** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen eines neuen Schlüssels zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf einen Schlüssel in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Schlüssel, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen eines Schlüssels aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung mit der [Refresh](refresh-method-ado.md)-Methode, um das Schema widerzuspiegeln.

