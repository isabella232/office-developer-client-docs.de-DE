---
title: Skip-Methode (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314560"
---
# <a name="skipline-method-ado"></a>Skip-Methode (ADO)


**Gilt für**: Access 2013, Office 2013

Überspringt beim Lesen eine Textdatenstroms eine gesamte Zeile.

## <a name="syntax"></a>Syntax

*Stream*. SkipLine

## <a name="remarks"></a>Bemerkungen

Alle Zeichen bis zum nächsten Linientrennzeichen (einschließlich dieses Zeichens) werden übersprungen. In der Standardeinstellung weist [LineSeparator](lineseparator-property-ado.md) den Wert **adCRLF** auf. Wenn Sie versuchen, eine Zeile nach [EOS](eos-property-ado.md) zu überspringen, verbleibt die aktuelle Position bei **EOS**.

Die **SkipLine**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) lautet **adTypeText**).

