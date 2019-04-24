---
title: Recordset2. Filter-Eigenschaft (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307329"
---
# <a name="recordset2filter-property-dao"></a>Recordset2. Filter-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der feststellt, welche Datensätze in einem nachfolgend geöffneten **Recordset**-Objekt einbezogen werden, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Filter

*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.

Verwenden Sie die **Filter**-Eigenschaft zum Anwenden eines Filters auf ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only".

Mit der **Filter**-Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset**-Objekt basierend auf einem vorhandenen **Recordset**-Objekt geöffnet wird.

Verwenden Sie das US-Datumsformat (Monat-Tag-Jahr) beim Filtern von Feldern, die Datumsangaben enthalten, auch wenn Sie nicht die US-Version des Microsoft Access-Datenbankmoduls verwenden (in diesem Fall müssen Sie Datumsangaben durch Verketten von Zeichenfolgen zusammensetzen, beispielsweise strMonth & "-" _ aMP_ strDay & "-" & strYear). Andernfalls werden die Daten möglicherweise nicht wie erwartet gefiltert.

In vielen Fällen ist es schneller, ein neues **Recordset**-Objekt zu öffnen, indem Sie eine SQL-Anweisung mit einer WHERE-Klausel verwenden.

Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strFilter \> = "Price" & lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Sie versuchen, Öffnen Sie das nächste **Recordset**-Objekt. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.

