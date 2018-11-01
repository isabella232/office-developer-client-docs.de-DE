---
title: Position-Eigenschaft (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab1111cdbc0e5a319f1f3431477854c6d38eff20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875406"
---
# <a name="position-property-ado"></a><span data-ttu-id="8b227-102">Position-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b227-102">Position property (ADO)</span></span>


<span data-ttu-id="8b227-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b227-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b227-104">Gibt die aktuelle Position in einem [Stream](stream-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8b227-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8b227-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8b227-105">Settings and return values</span></span>

<span data-ttu-id="8b227-p101">Legt einen Long-Wert fest, der den Offset der aktuellen Position vom Anfang des Datenstroms in Bytes angibt, oder gibt den Wert zurück. Der Standardwert lautet 0 und stellt das erste Byte im Datenstrom dar.</span><span class="sxs-lookup"><span data-stu-id="8b227-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b227-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b227-108">Remarks</span></span>

<span data-ttu-id="8b227-p102">Die aktuelle Position kann an einen Punkt am Ende des Datenstroms verschoben werden. Wenn Sie die aktuelle Position nach dem Ende des Datenstroms angeben, wird die [Größe](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) des **Stream** -Objekts entsprechend erhöht. Alle auf diese Art hinzugefügten neuen Bytes sind Null.</span><span class="sxs-lookup"><span data-stu-id="8b227-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8b227-p103">[!HINWEIS] <STRONG>Position</STRONG> wird immer in Bytes gemessen. Multiplizieren Sie bei einem Textdatenstrom, der Multibyte-Zeichensätze verwendet, zum Ermitteln der Zeichennummer die Position mit der Zeichengröße. Bei einem Doppelbyte-Zeichensatz z. B. befindet sich das erste Zeichen auf Position 0, das zweite Zeichen auf Position 2, das dritte Zeichen auf Position 4 usw.</span><span class="sxs-lookup"><span data-stu-id="8b227-p103"><STRONG>Position</STRONG> always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="8b227-p104">Negative Werte können nicht verwendet werden, um die Position in einem **Stream** -Objekt zu ändern. Nur positive Zahlen können für **Position** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b227-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="8b227-117">Bei schreibgeschützten **Stream** -Objekten gibt ADO keinen Fehler zurück, wenn **Position** auf einen Wert größer als die **Größe** des **Datenstroms**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8b227-117">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**.</span></span> <span data-ttu-id="8b227-118">Dies nicht ändern Sie die Größe des **Datenstroms**oder ändern Sie den Inhalt des **Streams** keinerlei.</span><span class="sxs-lookup"><span data-stu-id="8b227-118">This does not change the size of the **Stream**, or alter the **Stream** contents in any way.</span></span> <span data-ttu-id="8b227-119">Allerdings sollte dies vermieden werden, da es eine ohne Bedeutung **Position** Wert ergibt.</span><span class="sxs-lookup"><span data-stu-id="8b227-119">However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

