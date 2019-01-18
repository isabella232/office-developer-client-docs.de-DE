---
title: SkipLine-Methode (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718777"
---
# <a name="skipline-method-ado"></a>SkipLine-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Überspringt beim Lesen eine Textdatenstroms eine gesamte Zeile.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. SkipLine

## <a name="remarks"></a>Hinweise

Alle Zeichen bis zum nächsten Linientrennzeichen (einschließlich dieses Zeichens) werden übersprungen. In der Standardeinstellung weist [LineSeparator](lineseparator-property-ado.md) den Wert **adCRLF** auf. Wenn Sie versuchen, eine Zeile nach [EOS](eos-property-ado.md) zu überspringen, verbleibt die aktuelle Position bei **EOS**.

Die **SkipLine**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) lautet **adTypeText**).

