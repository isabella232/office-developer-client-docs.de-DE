---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297081"
---
# <a name="append-method-adox-procedures"></a>Append-Methode (ADOX Procedures)

**Gilt für**: Access 2013, Office 2013

Fügt der [Procedures](procedures-collection-adox.md)-Auflistung ein neues [Procedure](procedure-object-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Verfahren*. Append*Name*, *Command*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **String** -Wert, der den Namen der zu erstellenden und anzufügenden Prozedur angibt.|
|*Command* |Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende und anzufügende Prozedur darstellt.|

## <a name="remarks"></a>Bemerkungen

Erstellt eine neue Prozedur in der Datenquelle mit dem Namen und den Attributen, die im **Command**-Objekt angegeben sind.

Wenn der vom Benutzer angegebene Befehlstext eine Sicht statt einer Prozedur darstellt, ist das Verhalten vom jeweils verwendeten Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.

> [!NOTE]
> Bei Verwendung des OLE DB-Anbieters für Microsoft Jet und der **Append**-Methode der **Procedures**-Auflistung können Sie im *Command*-Parameter ein **View**-Objekt statt eines **Procedure**-Objekts angeben. Das **View**-Objekt wird der Datenquelle und der **Procedures**-Auflistung hinzugefügt. Wenn die **Procedures**- und die **Views**-Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **View**-Objekt nicht mehr in der **Procedures**-Auflistung, sondern in der **Views**-Auflistung angezeigt.


