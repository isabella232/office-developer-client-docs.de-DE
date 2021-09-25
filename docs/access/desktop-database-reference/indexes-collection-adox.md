---
title: Indexes-Auflistung (ADOX)
TOCTitle: Indexes collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 007d6803138a02bdfac5da55abbc3c990404dad3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602374"
---
# <a name="indexes-collection-adox"></a>Indexes-Auflistung (ADOX)


**Gilt für**: Access 2013, Office 2013

Enthält alle [Index](index-object-adox.md)-Objekte einer Tabelle.

## <a name="remarks"></a>HinwBemerkungeneise

Die [Append](append-method-adox-indexes.md)-Methode für eine **Indexes** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

  - Hinzufügen eines neuen Indexes zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

  - Zugreifen auf einen Index in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben der Anzahl der Indizes, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Entfernen eines Indexes aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

  - Aktualisieren der Objekte in der Auflistung mit der [Refresh](refresh-method-ado.md)-Methode, um das Schema widerzuspiegeln.

