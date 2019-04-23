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
# <a name="position-property-ado"></a>Position-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Die aktuelle Position in einem [Stream](stream-object-ado.md)-Objekt wird angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.

## <a name="remarks"></a>Bemerkungen

Die aktuelle Position kann an einen Punkt am Ende des Datenstroms verschoben werden. Wenn Sie die aktuelle Position nach dem Ende des Datenstroms angeben, wird die [Größe](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) des **Stream**-Objekts entsprechend erhöht. Alle auf diese Art hinzugefügten neuen Bytes sind Null.

> [!NOTE]
> [!HINWEIS] **Position** wird immer in Bytes gemessen. Multiplizieren Sie bei einem Textdatenstrom, der Multibyte-Zeichensätze verwendet, zum Ermitteln der Zeichennummer die Position mit der Zeichengröße. Bei einem Doppelbyte-Zeichensatz z. B. befindet sich das erste Zeichen auf Position 0, das zweite Zeichen auf Position 2, das dritte Zeichen auf Position 4 usw.

Negative Werte können nicht verwendet werden, um die Position in einem **Stream** -Objekt zu ändern. Nur positive Zahlen können für **Position** verwendet werden.

For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.

