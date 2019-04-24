---
title: Stat-Methode – ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308549"
---
# <a name="stat-method-ado"></a>Stat-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft Informationen zu einem **Stream**-Objekt ab.

## <a name="syntax"></a>Syntax

Long- *Stream*. Stat (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Rückgabewert

Ein langer Wert, der den Status des Vorgangs angibt.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*StatStg* |A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.|
|*StatFlag* |Gibt an, dass diese Methode einige Member in der STATSTG-Struktur nicht zurückgibt und daher einen Speicherzuweisungsvorgang speichert. Die Werte werden der STATFLAG-Enumeration entnommen.<br/><br/>Die STATFLAG-Aufzählung hat zwei Werte:<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Bemerkungen

Die Version der Stat-Methode, die für das Stream-Objekt in ADO implementiert wurde, füllt die folgenden Felder der STATSTG-Struktur aus:

|Feld|Beschreibung|
|:--------|:----------|
|*pwcsName* |Eine Zeichenfolge mit dem Namen des Streams, sofern vorhanden, und der StatFlag-Wert STATFLAG\_Noname wurde nicht angegeben.|
|*cbSize* |Gibt die Größe des Datenstroms oder des Bytearrays in Byte an.|
|*mtime* |Gibt den Zeitpunkt der letzten Änderung dieses Speichers, Datenstroms oder Bytearrays an.|
|*ctime* |Gibt den Zeitpunkt der Erstellung dieses Speichers, Datenstroms oder Bytearrays an.|
|*atime* |Gibt den Zeitpunkt des letzten Zugriffs auf diesen Speicher, diesen Datenstrom oder dieses Bytearray an.|

Wenn STATFLAG\_Noname im STATFLAG-Parameter angegeben ist, wird der Name des Streams nicht zurückgegeben.

Wenn STATFLAG\_Noname nicht im STATFLAG-Parameter angegeben wurde und kein Name für den aktuellen Stream verfügbar ist, ist dieser Wert E\_NOTIMPL.

