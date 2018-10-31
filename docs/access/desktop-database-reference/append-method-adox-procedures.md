---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195cb08fb0b195b63cdddaa848554f24d028b498
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861876"
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
> Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die **Append** -Methode der **Procedures** -Auflistung angeben einer **Ansicht** , sondern eine **Prozedur** in *der Befehlsparameter* ansetzt. Das **View** -Objekt wird der Datenquelle und der **Procedures** -Auflistung hinzugefügt. Wenn die **Procedures** - und die **Views** -Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **View** -Objekt nicht mehr in der **Procedures** -Auflistung, sondern in der **Views** -Auflistung angezeigt.


