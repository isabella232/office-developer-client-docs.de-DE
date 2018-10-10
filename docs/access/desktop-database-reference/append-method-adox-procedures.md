---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473002"
---
# <a name="append-method-adox-procedures"></a>Append-Methode (ADOX Procedures)


**Betrifft**: Access 2013 | Office 2013


Fügt der [Procedures](procedure-object-adox.md)-Auflistung ein neues [Procedure](procedures-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Verfahren*. Fügen Sie*Namen*, *Befehl*

## <a name="parameters"></a>Parameter

  - *Name*

  - Ein **String** -Wert, der den Namen der zu erstellenden und anzufügenden Prozedur angibt.

  - *Command*

  - Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende und anzufügende Prozedur darstellt.

## <a name="remarks"></a>Hinweise

Erstellt eine neue Prozedur in der Datenquelle mit dem Namen und den Attributen, die im **Command** -Objekt angegeben sind.

Wenn der vom Benutzer angegebene Befehlstext eine Sicht statt einer Prozedur darstellt, ist das Verhalten vom jeweils verwendeten Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.


> [!NOTE]
> <P>Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die <STRONG>Append</STRONG> -Methode der <STRONG>Procedures</STRONG> -Auflistung angeben einer <STRONG>Ansicht</STRONG> , sondern eine <STRONG>Prozedur</STRONG> in <EM>der Befehlsparameter</EM> ansetzt. Das <STRONG>View</STRONG> -Objekt wird der Datenquelle und der <STRONG>Procedures</STRONG> -Auflistung hinzugefügt. Wenn die <STRONG>Procedures</STRONG> - und die <STRONG>Views</STRONG> -Auflistung nach Ausführung von <STRONG>Append</STRONG> aktualisiert wurden, wird das <STRONG>View</STRONG> -Objekt nicht mehr in der <STRONG>Procedures</STRONG> -Auflistung, sondern in der <STRONG>Views</STRONG> -Auflistung angezeigt.</P>


