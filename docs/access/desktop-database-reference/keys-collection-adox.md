---
title: Keys-Auflistung (ADOX)
TOCTitle: Keys Collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 837a81058a7d5ba871069a5d8534e870194ba92f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473049"
---
# <a name="keys-collection-adox"></a>Keys-Auflistung (ADOX)


**Betrifft**: Access 2013 | Office 2013

Enthält alle [Key](key-object-adox.md)-Objekte einer Tabelle.

## <a name="remarks"></a>Hinweise

Die [Append](append-method-adox-keys.md)-Methode für eine **Keys** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen eines neuen Schlüssels zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf einen Schlüssel in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Schlüssel, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen eines Schlüssels aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

