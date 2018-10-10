---
title: Position-Eigenschaft (ADO)
TOCTitle: Position Property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a06810fe339bd9b0b24137e178517c062962c096
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474171"
---
# <a name="position-property-ado"></a>Position-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die aktuelle Position in einem [Stream](stream-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen Long-Wert fest, der den Offset der aktuellen Position vom Anfang des Datenstroms in Bytes angibt, oder gibt den Wert zurück. Der Standardwert lautet 0 und stellt das erste Byte im Datenstrom dar.

## <a name="remarks"></a>Hinweise

Die aktuelle Position kann an einen Punkt am Ende des Datenstroms verschoben werden. Wenn Sie die aktuelle Position nach dem Ende des Datenstroms angeben, wird die [Größe](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) des **Stream** -Objekts entsprechend erhöht. Alle auf diese Art hinzugefügten neuen Bytes sind Null.


> [!NOTE]
> <P>[!HINWEIS] <STRONG>Position</STRONG> wird immer in Bytes gemessen. Multiplizieren Sie bei einem Textdatenstrom, der Multibyte-Zeichensätze verwendet, zum Ermitteln der Zeichennummer die Position mit der Zeichengröße. Bei einem Doppelbyte-Zeichensatz z. B. befindet sich das erste Zeichen auf Position 0, das zweite Zeichen auf Position 2, das dritte Zeichen auf Position 4 usw.</P>



Negative Werte können nicht verwendet werden, um die Position in einem **Stream** -Objekt zu ändern. Nur positive Zahlen können für **Position** verwendet werden.

Bei schreibgeschützten **Stream** -Objekten gibt ADO keinen Fehler zurück, wenn **Position** auf einen Wert größer als die **Größe** des **Datenstroms**festgelegt ist. Dies nicht ändern Sie die Größe des **Datenstroms**oder ändern Sie den Inhalt des **Streams** keinerlei. Allerdings sollte dies vermieden werden, da es eine ohne Bedeutung **Position** Wert ergibt.

