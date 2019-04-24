---
title: Sortierreihenfolge-Eigenschaft (ADOX)
TOCTitle: SortOrder property (ADOX)
ms:assetid: c2b8c84d-acc4-9929-fff5-9a088abbfcf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249951(v=office.15)
ms:contentKeyID: 48547557
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 735e72e8ed4f06c887ff790209529787e38142a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306440"
---
# <a name="sortorder-property-adox"></a>Sortierreihenfolge-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt die Sortierfolge für die Spalte (nur Indexspalten) an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long**-Wert fest bzw. gibt diesen zurück. Der Wert kann eine der [SortOrderEnum](sortorderenum.md)-Konstanten sein. Der Standardwert lautet **adSortAscending**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur auf [Column](column-object-adox.md)-Objekte in der [Columns](columns-collection-adox.md)-Auflistung eines [Index](index-object-adox.md)-Objekts angewendet .

