---
title: SortOrder-Eigenschaft (ADOX)
TOCTitle: SortOrder Property (ADOX)
ms:assetid: c2b8c84d-acc4-9929-fff5-9a088abbfcf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249951(v=office.15)
ms:contentKeyID: 48547557
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 56898fc20d1d06a7be6e237d5054d0b9f0907ea6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473495"
---
# <a name="sortorder-property-adox"></a>SortOrder-Eigenschaft (ADOX)


**Betrifft**: Access 2013 | Office 2013

Gibt die Sortierfolge für die Spalte (nur Indexspalten) an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest bzw. gibt diesen zurück. Der Wert kann eine der [SortOrderEnum](sortorderenum.md)-Konstanten sein. Der Standardwert lautet **adSortAscending**.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur auf [Column](column-object-adox.md)-Objekte in der [Columns](columns-collection-adox.md)-Auflistung eines [Index](index-object-adox.md)-Objekts angewendet .

