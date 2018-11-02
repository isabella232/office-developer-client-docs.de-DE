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
ms.openlocfilehash: afa9bf22db7ec29399cef99e697a616369c9db21
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929146"
---
# <a name="recordset2filter-property-dao"></a>Recordset2.Filter-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der die in einem nachfolgend geöffneten **Recordset** -Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur Microsoft Access-Arbeitsbereich). Lese-/Schreibzugriff **String**.

## <a name="syntax"></a>Syntax

*Ausdruck* . Filter

*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.

Verwenden Sie die **Filter** -Eigenschaft, um einen Filter auf ein Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt anwenden.

Mit der **Filter** -Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset** -Objekt basierend auf einem vorhandenen **Recordset** -Objekt geöffnet wird.

Verwenden Sie das US-Datumsformat (Monat-Tag-Jahr) Wenn Sie Felder mit Datumsangaben filtern, auch wenn Sie nicht die US-Version von Microsoft Access-Datenbankmodul verwenden (in diesem Fall Sie alle Datumsangaben durch Verketten von Zeichenfolgen, beispielsweise StrMonth zusammensetzen müssen & "-" & StrDay & "-" & erstellen). Andernfalls können die Daten nicht gefiltert werden, wie erwartet.

In vielen Fällen geht es schneller, ein neues **Recordset** -Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.

Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Ganzzahl-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrFilter = "PRICE \> " & LngPrice, und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Öffnen Sie das nächste **Recordset-Objekt**. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.

