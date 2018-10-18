---
title: Name-Eigenschaft (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604050"
---
# <a name="name-property-adox"></a>Name-Eigenschaft (ADOX)


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen des Objekts an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.

## <a name="remarks"></a>Hinweise

Namen müssen innerhalb einer Auflistung nicht eindeutig sein.

Die **Name** -Eigenschaft verfügt über Lese-/Schreibzugriff für [Column](column-object-adox.md)-, [Group](group-object-adox.md)-, [Key](key-object-adox.md)-, [Index](index-object-adox.md)-, [Table](table-object-adox.md)- und [User](user-object-adox.md)-Objekte. Die **Name** -Eigenschaft ist schreibgeschützt für [Catalog](catalog-object-adox.md)-, [Procedure](procedure-object-adox.md)- und [View](view-object-adox.md)-Objekte.

Für Objekte mit Lese-/Schreibzugriff (**Column**-, **Group**-, **Key**-, **Index**-, **Table**- und **User**-Objekte) ist der Standardwert eine leere Zeichenfolge ("").


> [!NOTE]
> <P>[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für <STRONG>Key</STRONG> -Objekte, die bereits an eine Auflistung angefügt wurden.</P>




> [!NOTE]
> <P>[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für <STRONG>Table</STRONG> -Objekte, die bereits an eine Auflistung angefügt wurden.</P>


