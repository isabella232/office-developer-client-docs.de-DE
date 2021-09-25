---
title: Position-Eigenschaft (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dca9eac0014b6c80a498f70474c2715e1c17959c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562475"
---
# <a name="position-property-ado"></a>Position-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Die aktuelle Position in einem [Stream](stream-object-ado.md)-Objekt wird angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.

## <a name="remarks"></a>HinwBemerkungeneise

Die aktuelle Position kann an einen Punkt am Ende des Datenstroms verschoben werden. Wenn Sie die aktuelle Position nach dem Ende des Datenstroms angeben, wird die [Größe](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) des **Stream**-Objekts entsprechend erhöht. Alle auf diese Art hinzugefügten neuen Bytes sind Null.

> [!NOTE]
> [!HINWEIS] **Position** wird immer in Bytes gemessen. Multiplizieren Sie bei einem Textdatenstrom, der Multibyte-Zeichensätze verwendet, zum Ermitteln der Zeichennummer die Position mit der Zeichengröße. Bei einem Doppelbyte-Zeichensatz z. B. befindet sich das erste Zeichen auf Position 0, das zweite Zeichen auf Position 2, das dritte Zeichen auf Position 4 usw.

Negative Werte können nicht verwendet werden, um die Position in einem **Stream** -Objekt zu ändern. Nur positive Zahlen können für **Position** verwendet werden.

For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.

