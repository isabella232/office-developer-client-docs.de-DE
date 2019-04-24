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
# <a name="lineseparator-property-ado"></a><span data-ttu-id="d2ee5-102">LineSeparator-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2ee5-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="d2ee5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2ee5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2ee5-104">Das als Linientrennzeichen in [Stream](stream-object-ado.md)-Textobjekten zu verwendende binäre Zeichen wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="d2ee5-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d2ee5-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d2ee5-105">Settings and return values</span></span>

<span data-ttu-id="d2ee5-106">Legt einen [LineSeparatorsEnum](lineseparatorsenum.md)-Wert fest, der das im **Stream**-Objekt verwendete Linientrennzeichen angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2ee5-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="d2ee5-107">Der Standardwert lautet **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="d2ee5-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2ee5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2ee5-108">Remarks</span></span>

<span data-ttu-id="d2ee5-p102">**LineSeparator** wird verwendet, um beim Lesen des Inhalts eines **Stream**-Textobjekts Zeilen zu interpretieren. Zeilen können mit der [SkipLine](skipline-method-ado.md)-Methode übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="d2ee5-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="d2ee5-111">**LineSeparator** wird nur bei **Stream**-Textobjekten verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="d2ee5-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="d2ee5-112">Diese Eigenschaft wird ignoriert, wenn **Type** auf **adTypeBinary** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2ee5-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>

