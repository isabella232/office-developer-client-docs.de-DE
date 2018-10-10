---
title: SkipLine-Methode (ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28cb222a3ed0e5497e03efbb7394081c96b4d4ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474371"
---
# <a name="skipline-method-ado"></a>SkipLine-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013

Überspringt beim Lesen eine Textdatenstroms eine gesamte Zeile.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. SkipLine

## <a name="remarks"></a>Hinweise

Alle Zeichen bis zum nächsten Linientrennzeichen (einschließlich dieses Zeichens) werden übersprungen. In der Standardeinstellung weist [LineSeparator](lineseparator-property-ado.md) den Wert **adCRLF** auf. Wenn Sie versuchen, eine Zeile nach [EOS](eos-property-ado.md) zu überspringen, verbleibt die aktuelle Position bei **EOS**.

Die **SkipLine**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) lautet **adTypeText**).

