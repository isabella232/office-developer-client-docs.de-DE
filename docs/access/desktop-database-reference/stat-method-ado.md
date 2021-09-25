---
title: Stat-Methode – ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1eb003f761ae886bbcc57a573da5772d5b0c4945
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589085"
---
# <a name="stat-method-ado"></a>Stat-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft Informationen zu einem **Stream**-Objekt ab.

## <a name="syntax"></a>Syntax

Long *stream*. Stat(*StatStg*, *StatFlag*)

## <a name="return-value"></a>Rückgabewert

Ein langer Wert, der den Status des Vorgangs angibt.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Statstg* |A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.|
|*StatFlag* |Gibt an, dass diese Methode einige Member in der STATSTG-Struktur nicht zurückgibt und daher einen Speicherzuweisungsvorgang speichert. Die Werte werden der STATFLAG-Enumeration entnommen.<br/><br/>Die STATFLAG-Aufzählung hat zwei Werte:<br/>- STATFLAG_DEFAULT: 0<br/>- STATFLAG_NONAME: 1 |


## <a name="remarks"></a>HinwBemerkungeneise

Die Version der Stat-Methode, die für das Stream-Objekt in ADO implementiert wurde, füllt die folgenden Felder der STATSTG-Struktur aus:

|Feld|Beschreibung|
|:--------|:----------|
|*pwcsName* |Eine Zeichenfolge mit dem Namen des Datenstroms, sofern verfügbar, und der StatFlag-Wert STATFLAG \_ NONAME wurde nicht angegeben.|
|*cbSize* |Gibt die Größe des Datenstroms oder des Bytearrays in Byte an.|
|*mtime* |Gibt den Zeitpunkt der letzten Änderung dieses Speichers, Datenstroms oder Bytearrays an.|
|*ctime* |Gibt den Zeitpunkt der Erstellung dieses Speichers, Datenstroms oder Bytearrays an.|
|*atime* |Gibt den Zeitpunkt des letzten Zugriffs auf diesen Speicher, diesen Datenstrom oder dieses Bytearray an.|

Wenn STATFLAG \_ NONAME im StatFlag-Parameter angegeben ist, wird der Name des Datenstroms nicht zurückgegeben.

Wenn STATFLAG \_ NONAME nicht im StatFlag-Parameter angegeben wurde und kein Name für den aktuellen Datenstrom verfügbar ist, ist dieser Wert E \_ NOTIMPL.

