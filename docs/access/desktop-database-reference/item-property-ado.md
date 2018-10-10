---
title: Item-Eigenschaft (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472922"
---
# <a name="item-property-ado"></a>Item-Eigenschaft (ADO)

**Betrifft**: Access 2013 | Office 2013

Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.

## <a name="syntax"></a>Syntax

Legen Sie*Objekt* = *Auflistung*. Item (Index)

## <a name="return-value"></a>Rückgabewert

Gibt einen Objektverweis zurück.

## <a name="parameters"></a>Parameter

- *Index*

- Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben. Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf. Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.

Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:

```vb
    collection.Item (Index)
    collection (Index)
```
