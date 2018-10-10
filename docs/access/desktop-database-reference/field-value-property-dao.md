---
title: Field.Value Property (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 946ce8ec4219229e047d1bef5c3ff6de403eb7c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473455"
---
# <a name="fieldvalue-property-dao"></a>Field.Value Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt den Wert eines Objekts fest oder gibt ihn zurück. **Variant**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Wert

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung eines Rückgabewerts ist ein Variant-Datentyp, der als für den Datentyp geeigneter Wert ausgewertet wird, wie in der Type-Eigenschaft des Objekts angegeben.

Im Allgemeinen wird die **Value**-Eigenschaft verwendet, um Daten in **Recordset**-Objekten abzufragen und zu ändern.

Die **Value**-Eigenschaft ist die Standardeigenschaft der Objekte **Field**, **Parameter** und **Property**. Aus diesem Grund können Sie den Wert dieser Objekte direkt festlegen oder zurückgeben, ohne die **Value**-Eigenschaft anzugeben.

Der Versuch, die **Value**-Eigenschaft in einem unzulässigen Kontext festzulegen oder zurückzugeben (z. B. die **Value**-Eigenschaft eines **Field**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts), verursacht einen auffangbaren Fehler.


> [!NOTE]
> <P>Beim Lesen von Dezimalwerten aus einer Microsoft SQL Server-Datenbank werden die Werte im Microsoft Access-Arbeitsbereich in wissenschaftlicher Schreibweise formatiert. Im ODBCDirect-Arbeitsbereich werden sie dagegen als normale Dezimalwerte angezeigt.</P>


