---
title: Name-Eigenschaft (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f067c16c2c7d8d584d6900bff6212b469c3b7fe4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602199"
---
# <a name="name-property-adox"></a>Name-Eigenschaft (ADOX)

**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.

## <a name="remarks"></a>HinwBemerkungeneise

Namen müssen innerhalb einer Auflistung nicht eindeutig sein.

Die **Name** -Eigenschaft verfügt über Lese-/Schreibzugriff für [Column](column-object-adox.md)-, [Group](group-object-adox.md)-, [Key](key-object-adox.md)-, [Index](index-object-adox.md)-, [Table](table-object-adox.md)- und [User](user-object-adox.md)-Objekte. Die **Name** -Eigenschaft ist schreibgeschützt für [Catalog](catalog-object-adox.md)-, [Procedure](procedure-object-adox.md)- und [View](view-object-adox.md)-Objekte.

Für Objekte mit Lese-/Schreibzugriff (**Column**-, **Group**-, **Key**-, **Index**-, **Table**- und **User**-Objekte) ist der Standardwert eine leere Zeichenfolge ("").

> [!NOTE]
> - Diese Eigenschaft ist schreibgeschützt für **Key**-Objekte, die bereits an eine Auflistung angefügt wurden.
> - [!HINWEIS] Diese Eigenschaft ist schreibgeschützt für **Table** -Objekte, die bereits an eine Auflistung angefügt wurden.


