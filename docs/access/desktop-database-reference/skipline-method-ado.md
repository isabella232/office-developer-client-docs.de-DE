---
title: SkipLine-Methode (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d22aca01c468813f280472281719822a7d884988
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923924"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="0cf06-102">SkipLine-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0cf06-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="0cf06-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cf06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0cf06-104">Überspringt beim Lesen eine Textdatenstroms eine gesamte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cf06-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf06-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cf06-105">Syntax</span></span>

<span data-ttu-id="0cf06-106">*Stream-Objekt*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="0cf06-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf06-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0cf06-107">Remarks</span></span>

<span data-ttu-id="0cf06-p101">Alle Zeichen bis zum nächsten Linientrennzeichen (einschließlich dieses Zeichens) werden übersprungen. In der Standardeinstellung weist [LineSeparator](lineseparator-property-ado.md) den Wert **adCRLF** auf. Wenn Sie versuchen, eine Zeile nach [EOS](eos-property-ado.md) zu überspringen, verbleibt die aktuelle Position bei **EOS**.</span><span class="sxs-lookup"><span data-stu-id="0cf06-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="0cf06-111">Die **SkipLine**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) lautet **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="0cf06-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

