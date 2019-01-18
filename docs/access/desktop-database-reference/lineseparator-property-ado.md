---
title: LineSeparator-Eigenschaft (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720674"
---
# <a name="lineseparator-property-ado"></a>LineSeparator-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt das binäre Zeichen an, das als Zeilentrennzeichen in [Stream](stream-object-ado.md)-Textobjekten verwendet wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [LineSeparatorsEnum](lineseparatorsenum.md)-Wert fest, der das im **Stream** -Objekt verwendete Linientrennzeichen angibt, oder gibt diesen Wert zurück. Der Standardwert lautet **adCRLF**.

## <a name="remarks"></a>Hinweise

**LineSeparator** wird verwendet, um beim Lesen des Inhalts eines **Stream** -Textobjekts Zeilen zu interpretieren. Zeilen können mit der [SkipLine](skipline-method-ado.md)-Methode übersprungen werden.

**LineSeparator** wird nur bei **Stream**-Textobjekten verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Diese Eigenschaft wird ignoriert, wenn **Type** auf **adTypeBinary** festgelegt ist.

