---
title: Find-Methode – ActiveX Data Objects (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f1ba79981e59ad18bad6be2046a020b32dd2101c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602542"
---
# <a name="find-method-ado"></a>Find-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Durchsucht ein [Recordset](recordset-object-ado.md)-Objekt nach der Zeile, die den angegebenen Kriterien entspricht. Optional können die Suchrichtung, die Startzeile und der Versatz von der Startzeile aus gesehen angegeben werden. Stimmen die Kriterien überein, wird die aktuelle Zeilenposition bei dem gefundenen Datensatz festgelegt. Andernfalls wird die Startposition auf das Ende (oder den Anfang) des **Recordset**-Objekts festgelegt.

## <a name="syntax"></a>Syntax

Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Kriterium* |Ein **String** -Wert mit einer Anweisung, die den Spaltennamen, den Vergleichsoperator und den für die Suche zu verwendenden Wert angibt.|
|*SkipRows* |Optional. Ein **Long -Wert,** dessen Standardwert Null ist, der den Zeilenversatz von der aktuellen Zeile oder *der Startmarke* angibt, um die Suche zu beginnen. Standardmäßig beginnt die Suche bei der aktuellen Zeile.|
|*SearchDirection* |Optional. A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**. An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.|
|*Start* |Optional. Eine **Variant** -Textmarke, die als Startposition für die Suche fungiert.|

## <a name="remarks"></a>HinwBemerkungeneise

Es kann nur ein einzelner Spaltennamen für *Criteria* angegeben werden. Diese Methode unterstützt keine Suchen über mehrere Spalten.

Der Vergleichsoperator in *Criteria* kann " **\>** (größer als), "** \<**" (less than), "=" (equal), "\> =" (größer als oder gleich), \<=" (less than or equal), "\<\> " " (ungleich) oder "like" (Mustervergleich) sein.

Der Wert in *Kriterien* kann eine Zeichenfolge, eine Gleitkommazahl oder ein Datum sein. Zeichenfolgenwerte werden durch einfache Anführungszeichen oder \# " (Nummernzeichen)-Markierungen getrennt (z. B. "state = 'WA'" oder "state = \# WA \# "). Datumswerte werden mit \# " " (Nummernzeichen)-Markierungen getrennt (z. B. \_ "Startdatum \> \# 7/22/97") und können \# Stunden, Minuten und Sekunden enthalten, um Zeitstempel anzugeben, sollten jedoch keine Millisekunden enthalten, andernfalls treten Fehler auf.

Ist der Vergleichsoperator "like", kann der Zeichenfolgenwert ein Sternchen (\*) enthalten, um nach einem oder mehreren Vorkommen eines beliebigen Zeichens oder einer beliebigen Teilzeichenfolge zu suchen. Bei einer Suche nach "state like 'M\*'" werden beispielsweise Maine und Massachusetts gefunden. Sie können auch führende und nachfolgende Sternchen verwenden, um nach einer Teilzeichenfolge innerhalb eines Werts zu suchen. Bei einer Suche nach "state like '\*as\*'" werden Alaska, Arkansas und Massachusetts gefunden.

Sternchen können, wie oben dargestellt, nur am Ende oder nur am Anfang und am Ende einer \* -Zeichenfolge verwendet werden. Sie können das Sternchen nicht als führenden Platzhalter ('\*r') verwenden. In diesem Fall tritt ein Fehler auf.

> [!NOTE]
> [!HINWEIS] Wird vor dem Aufrufen von **Find** keine aktuelle Zeilenposition festgelegt, tritt ein Fehler auf. Vor dem Aufrufen von [Find](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) sollte eine beliebige Methode aufgerufen werden, die Zeilenpositionen festlegt (z. B. **MoveFirst**).

> [!NOTE]
> [!HINWEIS] Wenn Sie die **Find** -Methode für einen Datensatz aufrufen und sich die aktuelle Position in der Datensatzgruppe beim letzten Datensatz oder am Ende der Datei (End of File, EOF) befindet, bleibt die Suche erfolglos. Sie müssen die **MoveFirst** -Methode aufrufen, um die aktuelle Position bzw. den Cursor auf den Anfang der Datensatzgruppe festzulegen.


