---
title: STAT-Methode - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721073"
---
# <a name="stat-method-ado"></a>Stat-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Ruft Informationen zu einem **Stream** -Objekt ab.

## <a name="syntax"></a>Syntax

Lange *Stream*. STAT (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Rückgabewert

Ein langer Wert, der den Status des Vorgangs angibt.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*StatStg* |Eine STATSTG-Struktur, die mit Informationen zum Datenstrom ausgefüllt wird. Die Implementierung der Stat-Methode, die vom Stream-Objekt in ADO verwendet wird, füllt nicht alle Felder der Struktur aus.|
|*StatFlag* |Gibt an, dass diese Methode einige Member in der STATSTG-Struktur nicht zurückgibt und daher einen Speicherzuweisungsvorgang speichert. Die Werte werden der STATFLAG-Enumeration entnommen.<br/><br/>Die STATFLAG-Enumeration verfügt über zwei Werte:<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Hinweise

Die Version der Stat-Methode, die für das Stream-Objekt in ADO implementiert wurde, füllt die folgenden Felder der STATSTG-Struktur aus:

|Feld|Beschreibung|
|:--------|:----------|
|*pwcsName* |Eine Zeichenfolge mit dem Namen des Stream-Objekts, wenn eine verfügbar ist und der StatFlag-Wert STATFLAG\_NONAME nicht angegeben wurde.|
|*cbSize* |Gibt die Größe des Datenstroms oder des Bytearrays in Byte an.|
|*mtime* |Gibt den Zeitpunkt der letzten Änderung dieses Speichers, Datenstroms oder Bytearrays an.|
|*ctime* |Gibt den Zeitpunkt der Erstellung dieses Speichers, Datenstroms oder Bytearrays an.|
|*atime* |Gibt den Zeitpunkt des letzten Zugriffs auf diesen Speicher, diesen Datenstrom oder dieses Bytearray an.|

Wenn STATFLAG\_NONAME im StatFlag-Parameter angegeben ist, wird der Name des Datenstroms nicht zurückgegeben.

Wenn STATFLAG\_NONAME im StatFlag-Parameter nicht angegeben wurde und kein Name vorhanden ist, für den aktuellen Datenstrom, lautet dieser Wert E\_NOTIMPL.

