---
title: Item-Eigenschaft (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718560"
---
# <a name="item-property-ado"></a>Item-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.

## <a name="syntax"></a>Syntax

Legen Sie*Objekt* = *Auflistung*. Item (Index)

## <a name="return-value"></a>Rückgabewert

Gibt einen Objektverweis zurück.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.|

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben. Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf. Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.

Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:

```vb
    collection.Item (Index)
    collection (Index)
```
