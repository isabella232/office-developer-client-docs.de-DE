---
title: Append-Methode (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b6dd5ffc50e487cb00022fdd96708bea713ed006
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607325"
---
# <a name="append-method-adox-views"></a>Append-Methode (ADOX Views)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues [View](view-object-adox.md)-Objekt und fügt es an die [Views](views-collection-adox.md)-Auflistung an.

## <a name="syntax"></a>Syntax

*Views*. Append *Name*, *Command*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **String** -Wert, der den Namen der zu erstellenden Sicht angibt.|
|*Command* |Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende Sicht darstellt.|

## <a name="remarks"></a>HinwBemerkungeneise

Erstellt eine neue Sicht in der Datenquelle mit dem Namen und Attributen, die im **Command**-Objekt angegeben sind.

Wenn der vom Benutzer angegebene Befehlstext keine Sicht, sondern eine Prozedur darstellt, ist das Verhalten vom Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.

> [!NOTE]
> Beim Verwenden des OLE DB-Anbieters für Microsoft Jet und der **Append**-Methode der **Views**-Auflistung können Sie im *Command*-Parameter ein **Procedure**-Objekt statt eines **View**-Objekts angeben. Das **Procedure**-Objekt wird der Datenquelle und der **Views**-Auflistung hinzugefügt. Wenn die **Procedures**- und die **Views**-Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **Procedure**-Objekt nicht mehr in der **Views**-Auflistung, sondern in der **Procedures**-Auflistung angezeigt.


