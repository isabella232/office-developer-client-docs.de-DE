---
title: Name-Eigenschaft (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707983"
---
# <a name="name-property-adox"></a>Name-Eigenschaft (ADOX)

**Betrifft**: Access 2013, Office 2013

Gibt den Namen des Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.

## <a name="remarks"></a>Hinweise

Namen müssen innerhalb einer Auflistung nicht eindeutig sein.

Die **Name** -Eigenschaft verfügt über Lese-/Schreibzugriff für [Column](column-object-adox.md)-, [Group](group-object-adox.md)-, [Key](key-object-adox.md)-, [Index](index-object-adox.md)-, [Table](table-object-adox.md)- und [User](user-object-adox.md)-Objekte. Die **Name** -Eigenschaft ist schreibgeschützt für [Catalog](catalog-object-adox.md)-, [Procedure](procedure-object-adox.md)- und [View](view-object-adox.md)-Objekte.

Für Objekte mit Lese-/Schreibzugriff (**Column**-, **Group**-, **Key**-, **Index**-, **Table**- und **User**-Objekte) ist der Standardwert eine leere Zeichenfolge ("").

> [!NOTE]
> - [!HINWEIS] Diese Eigenschaft ist schreibgeschützt für **Key** -Objekte, die bereits an eine Auflistung angefügt wurden.
> - [!HINWEIS] Diese Eigenschaft ist schreibgeschützt für **Table** -Objekte, die bereits an eine Auflistung angefügt wurden.


