---
title: Find-Methode - ActiveX Data Objects (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ff66a39de070759e0ad31b441e4be5735d87516
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936611"
---
# <a name="find-method-ado"></a>Find-Methode (ADO)


**Betrifft**: Access 2013, Office 2013


Durchsucht ein [Recordset](recordset-object-ado.md)-Objekt nach der Zeile, die den angegebenen Kriterien entspricht. Optional können die Suchrichtung, die Startzeile und der Versatz von der Startzeile aus gesehen angegeben werden. Stimmen die Kriterien überein, wird die aktuelle Zeilenposition bei dem gefundenen Datensatz festgelegt. Andernfalls wird die Startposition auf das Ende (oder den Anfang) des **Recordset** -Objekts festgelegt.

## <a name="syntax"></a>Syntax

Hier finden Sie (*Kriterien*, *SkipRows*, *SearchDirection*, *Starten*)

## <a name="parameters"></a>Parameter

  - *Criteria*

  - Ein **String** -Wert mit einer Anweisung, die den Spaltennamen, den Vergleichsoperator und den für die Suche zu verwendenden Wert angibt.

  - *SkipRows*

  - Optionale *.* Ein **Long** -Wert, dessen Standardwert 0 (null) ist,, der angibt, den Zeilenoffset aus der aktuellen Zeile oder die Textmarke *Starten ist* , um die Suche zu starten. Standardmäßig beginnt die Suche bei der aktuellen Zeile.

  - *SearchDirection*

  - Optionale *.* Ein [SearchDirectionEnum](searchdirectionenum.md) -Wert, der angibt, ob die Suche auf der aktuellen Zeile oder die nächste verfügbare Zeile in der Richtung der Suche beginnen soll. Eine Suche nicht erfolgreiche beendet am Ende des **Recordset-Objekt** , wenn der Wert **AdSearchForward**ist. Eine Suche nicht erfolgreiche beendet am Anfang des **Recordset-Objekt** , wenn der Wert **AdSearchBackward**ist.

  - *Start*

  - Optional. Eine **Variant** -Textmarke, die als Startposition für die Suche fungiert.

## <a name="remarks"></a>Hinweise

Es kann nur ein einzelner Spaltennamen für *Criteria* angegeben werden. Diese Methode unterstützt keine Suchen über mehrere Spalten.

Der Vergleichsoperator in *Kriterien* möglicherweise "**\>**"(größer als),"**\<**"(kleiner als), "=" (gleich),"\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich), "\<\>" (nicht gleich) oder "like" (Mustervergleich).

Der Wert in *Kriterien* möglicherweise eine Zeichenfolge, eine Gleitkommazahl oder ein Datum. String-Werte werden in einfache Anführungszeichen getrennt oder "\#" (Nummernzeichen) markiert (beispielsweise "State = 'WA'" oder "Zustand = \#WA\#"). Datumswerte sind mit getrennt "\#" (Nummernzeichen) markiert (beispielsweise "starten\_Datum \> \#7/22/97\#") und kann enthalten Stunden, Minuten und Sekunden an, dass Zeitstempel aber darf keine Millisekunden oder kommt es zu Fehlern .

Ist der Vergleichsoperator "like", kann der Zeichenfolgenwert ein Sternchen (\*) enthalten, um nach einem oder mehreren Vorkommen eines beliebigen Zeichens oder einer beliebigen Teilzeichenfolge zu suchen. Bei einer Suche nach "state like 'M\*'" werden beispielsweise Maine und Massachusetts gefunden. Sie können auch führende und nachfolgende Sternchen verwenden, um nach einer Teilzeichenfolge innerhalb eines Werts zu suchen. Bei einer Suche nach "state like '\*as\*'" werden Alaska, Arkansas und Massachusetts gefunden.

Sternchen können, wie oben dargestellt, nur am Ende oder nur am Anfang und am Ende einer \* -Zeichenfolge verwendet werden. Sie können das Sternchen nicht als führenden Platzhalter ('\*r') verwenden. In diesem Fall tritt ein Fehler auf.


> [!NOTE]
> [!HINWEIS] Wird vor dem Aufrufen von **Find** keine aktuelle Zeilenposition festgelegt, tritt ein Fehler auf. Vor dem Aufrufen von [Find](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) sollte eine beliebige Methode aufgerufen werden, die Zeilenpositionen festlegt (z. B. **MoveFirst**).

> [!NOTE]
> [!HINWEIS] Wenn Sie die **Find** -Methode für einen Datensatz aufrufen und sich die aktuelle Position in der Datensatzgruppe beim letzten Datensatz oder am Ende der Datei (End of File, EOF) befindet, bleibt die Suche erfolglos. Sie müssen die **MoveFirst** -Methode aufrufen, um die aktuelle Position bzw. den Cursor auf den Anfang der Datensatzgruppe festzulegen.


