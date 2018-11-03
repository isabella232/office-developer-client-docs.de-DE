---
title: Field2.Value-Eigenschaft (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7c17992daff5064b41507f5c2a1b2781476095a
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936875"
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


