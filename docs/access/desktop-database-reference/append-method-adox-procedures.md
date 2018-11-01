---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef11c9d45cc5b34b5ef7b1cf762dfd6f3e4c1d64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873047"
---
# <a name="append-method-adox-procedures"></a>Append-Methode (ADOX Procedures)


**Betrifft**: Access 2013, Office 2013


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
> Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die **Append** -Methode der **Procedures** -Auflistung angeben einer **Ansicht** , sondern eine **Prozedur** in *der Befehlsparameter* ansetzt. Das **View** -Objekt wird der Datenquelle und der **Procedures** -Auflistung hinzugefügt. Wenn die **Procedures** - und die **Views** -Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **View** -Objekt nicht mehr in der **Procedures** -Auflistung, sondern in der **Views** -Auflistung angezeigt.


