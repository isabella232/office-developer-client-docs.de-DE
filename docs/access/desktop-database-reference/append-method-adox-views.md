---
title: Append-Methode (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716153"
---
# <a name="append-method-adox-views"></a>Append-Methode (ADOX Views)

**Betrifft**: Access 2013, Office 2013

Erstellt ein neues [View](view-object-adox.md)-Objekt und fügt es an die [Views](views-collection-adox.md)-Auflistung an.

## <a name="syntax"></a>Syntax

*Ansichten*. Fügen Sie*Namen*, *Befehl*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **String** -Wert, der den Namen der zu erstellenden Sicht angibt.|
|*Command* |Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende Sicht darstellt.|

## <a name="remarks"></a>Hinweise

Erstellt eine neue Sicht in der Datenquelle mit dem Namen und Attributen, die im **Command** -Objekt angegeben sind.

Wenn der vom Benutzer angegebene Befehlstext keine Sicht, sondern eine Prozedur darstellt, ist das Verhalten vom Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.

> [!NOTE]
> Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die **Append** -Methode der **Views** -Auflistung angeben einer **Ansicht** , sondern eine **Prozedur** in *der Befehlsparameter* ansetzt. Das **Procedure** -Objekt wird der Datenquelle und der **Views** -Auflistung hinzugefügt. Wenn die **Procedures** - und die **Views** -Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **Procedure** -Objekt nicht mehr in der **Views** -Auflistung, sondern in der **Procedures** -Auflistung angezeigt.


