---
title: Field2.Value-Eigenschaft (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707766"
---
# <a name="field2value-property-dao"></a>Field2.Value-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt den Wert eines Objekts fest oder gibt ihn zurück. **Variant**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Wert

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung eines Rückgabewerts ist ein Variant-Datentyp, der als für den Datentyp geeigneter Wert ausgewertet wird, wie in der Type-Eigenschaft des Objekts angegeben.

In der Regel werden mit der **Value**-Eigenschaft Daten in **Recordset**-Objekten abgerufen und geändert.

Die **Value**-Eigenschaft ist die Standardeigenschaft der Objekte **Field2**, **Parameter** und **Property**. Sie können deshalb den Wert dieser Objekte festlegen oder zurückgeben, indem Sie direkt auf das Objekt verweisen, anstatt die **Value**-Eigenschaft anzugeben.

Wenn Sie versuchen, die **Value**-Eigenschaft in einem ungeeigneten Kontext festzulegen oder zurückzugeben (z. B. die **Value**-Eigenschaft eines **Field2**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts), tritt ein abfangbarer Fehler auf.


> [!NOTE]
> Dezimale Werte werden beim Lesen aus einer Microsoft SQL Server-Datenbank in einem Microsoft Access-Arbeitsbereich mit einer wissenschaftlichen Schreibweise formatiert, in einem ODBCDirect-Arbeitsbereich werden sie jedoch als normale Dezimalwerte angezeigt.


