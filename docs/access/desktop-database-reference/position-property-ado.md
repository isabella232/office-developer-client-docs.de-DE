---
title: Position-Eigenschaft (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a47cc394cf0bb1c6f5a3d707c1885d0abef0f0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287524"
---
# <a name="position-property-ado"></a><span data-ttu-id="2a83e-102">Position-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a83e-102">Position property (ADO)</span></span>

<span data-ttu-id="2a83e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a83e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a83e-104">Die aktuelle Position in einem [Stream](stream-object-ado.md)-Objekt wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="2a83e-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2a83e-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2a83e-105">Settings and return values</span></span>

<span data-ttu-id="2a83e-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span><span class="sxs-lookup"><span data-stu-id="2a83e-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a83e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a83e-108">Remarks</span></span>

<span data-ttu-id="2a83e-p102">Die aktuelle Position kann an einen Punkt am Ende des Datenstroms verschoben werden. Wenn Sie die aktuelle Position nach dem Ende des Datenstroms angeben, wird die [Größe](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) des **Stream**-Objekts entsprechend erhöht. Alle auf diese Art hinzugefügten neuen Bytes sind Null.</span><span class="sxs-lookup"><span data-stu-id="2a83e-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>

> [!NOTE]
> <span data-ttu-id="2a83e-p103">[!HINWEIS] **Position** wird immer in Bytes gemessen. Multiplizieren Sie bei einem Textdatenstrom, der Multibyte-Zeichensätze verwendet, zum Ermitteln der Zeichennummer die Position mit der Zeichengröße. Bei einem Doppelbyte-Zeichensatz z. B. befindet sich das erste Zeichen auf Position 0, das zweite Zeichen auf Position 2, das dritte Zeichen auf Position 4 usw.</span><span class="sxs-lookup"><span data-stu-id="2a83e-p103">**Position** always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span>

<span data-ttu-id="2a83e-p104">Negative Werte können nicht verwendet werden, um die Position in einem **Stream** -Objekt zu ändern. Nur positive Zahlen können für **Position** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a83e-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="2a83e-p105">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.</span><span class="sxs-lookup"><span data-stu-id="2a83e-p105">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

