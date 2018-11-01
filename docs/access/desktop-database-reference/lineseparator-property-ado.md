---
title: LineSeparator-Eigenschaft (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 831b6377ade43b3be04ed21add20fbd10e48ac2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882504"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="7d1d9-102">LineSeparator-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="7d1d9-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="7d1d9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d1d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d1d9-104">Gibt das binäre Zeichen an, das als Zeilentrennzeichen in [Stream](stream-object-ado.md)-Textobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d1d9-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7d1d9-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7d1d9-105">Settings and return values</span></span>

<span data-ttu-id="7d1d9-p101">Legt einen [LineSeparatorsEnum](lineseparatorsenum.md)-Wert fest, der das im **Stream** -Objekt verwendete Linientrennzeichen angibt, oder gibt diesen Wert zurück. Der Standardwert lautet **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="7d1d9-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d1d9-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d1d9-108">Remarks</span></span>

<span data-ttu-id="7d1d9-p102">**LineSeparator** wird verwendet, um beim Lesen des Inhalts eines **Stream** -Textobjekts Zeilen zu interpretieren. Zeilen können mit der [SkipLine](skipline-method-ado.md)-Methode übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="7d1d9-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="7d1d9-p103">**LineSeparator** wird nur bei **Stream**-Textobjekten verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Diese Eigenschaft wird ignoriert, wenn **Type** auf **adTypeBinary** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7d1d9-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

