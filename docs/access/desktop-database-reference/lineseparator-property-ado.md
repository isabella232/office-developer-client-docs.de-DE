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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289949"
---
# <a name="lineseparator-property-ado"></a>LineSeparator-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Das als Linientrennzeichen in [Stream](stream-object-ado.md)-Textobjekten zu verwendende binäre Zeichen wird angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [LineSeparatorsEnum](lineseparatorsenum.md)-Wert fest, der das im **Stream**-Objekt verwendete Linientrennzeichen angibt, oder gibt diesen Wert zurück. Der Standardwert lautet **adCRLF**.

## <a name="remarks"></a>Bemerkungen

**LineSeparator** wird verwendet, um beim Lesen des Inhalts eines **Stream**-Textobjekts Zeilen zu interpretieren. Zeilen können mit der [SkipLine](skipline-method-ado.md)-Methode übersprungen werden.

**LineSeparator** wird nur bei **Stream**-Textobjekten verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Diese Eigenschaft wird ignoriert, wenn **Type** auf **adTypeBinary** festgelegt ist.

