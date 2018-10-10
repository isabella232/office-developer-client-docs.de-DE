---
title: Append-Methode (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474383"
---
# <a name="append-method-adox-views"></a>Append-Methode (ADOX Views)


**Betrifft**: Access 2013 | Office 2013


Erstellt ein neues [View](view-object-adox.md)-Objekt und fügt es an die [Views](views-collection-adox.md)-Auflistung an.

## <a name="syntax"></a>Syntax

*Ansichten*. Fügen Sie*Namen*, *Befehl*

## <a name="parameters"></a>Parameter

  - *Name*

  - Ein **String** -Wert, der den Namen der zu erstellenden Sicht angibt.

  - *Command*

  - Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende Sicht darstellt.

## <a name="remarks"></a>Hinweise

Erstellt eine neue Sicht in der Datenquelle mit dem Namen und Attributen, die im **Command** -Objekt angegeben sind.

Wenn der vom Benutzer angegebene Befehlstext keine Sicht, sondern eine Prozedur darstellt, ist das Verhalten vom Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.


> [!NOTE]
> <P>Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die <STRONG>Append</STRONG> -Methode der <STRONG>Views</STRONG> -Auflistung angeben einer <STRONG>Ansicht</STRONG> , sondern eine <STRONG>Prozedur</STRONG> in <EM>der Befehlsparameter</EM> ansetzt. Das <STRONG>Procedure</STRONG> -Objekt wird der Datenquelle und der <STRONG>Views</STRONG> -Auflistung hinzugefügt. Wenn die <STRONG>Procedures</STRONG> - und die <STRONG>Views</STRONG> -Auflistung nach Ausführung von <STRONG>Append</STRONG> aktualisiert wurden, wird das <STRONG>Procedure</STRONG> -Objekt nicht mehr in der <STRONG>Views</STRONG> -Auflistung, sondern in der <STRONG>Procedures</STRONG> -Auflistung angezeigt.</P>


