---
title: Recordset2.Filter-Eigenschaft (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 757aec47564e6462bf543e408825367ef26b775c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605981"
---
# <a name="recordset2filter-property-dao"></a>Recordset2.Filter-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der feststellt, welche Datensätze in einem nachfolgend geöffneten **Recordset**-Objekt einbezogen werden, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*expression* .Filter

*Ausdruck* Ein Ausdruck, der ein **Recordset2-Objekt** zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.

Verwenden Sie die **Filter**-Eigenschaft zum Anwenden eines Filters auf ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only".

Mit der **Filter**-Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset**-Objekt basierend auf einem vorhandenen **Recordset**-Objekt geöffnet wird.

Verwenden Sie beim Filtern von Feldern mit Datumsangaben das US-amerikanische Datumsformat (Monat-Tag-Jahr), selbst wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten (in diesem Fall müssen Sie alle Datumsangaben durch Verketten von Zeichenfolgen bilden, z. B. strMonth & "-" & strDay & "-" & strYear). Andernfalls werden die Daten möglicherweise nicht wie erwartet gefiltert.

In vielen Fällen geht es schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.

Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Wert verkettet ist, bei dem es sich nicht um eine Ganzzahl handelt, und die Systemparameter ein anderes als das US-amerikanische Dezimaltrennzeichen festlegen, wie etwa ein Komma (Beispiel: strFilter = "PRICE \> " & lngPrice und lngPrice = 125,50), tritt ein Fehler auf, wenn Sie versuchen, das nächste **Recordset**-Objekt zu öffnen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.

