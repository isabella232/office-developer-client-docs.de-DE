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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290793"
---
# <a name="item-property-ado"></a>Item-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.

## <a name="syntax"></a>Syntax

*Objekt* = *Sammlung*festlegen. Item (Index)

## <a name="return-value"></a>Rückgabewert

Gibt einen Objektverweis zurück.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Item**-Eigenschaft, wenn ein bestimmtes Objekt in einer Auflistung zurückgegeben werden soll. Wenn **Item** kein Objekt in der Auflistung findet, das dem Argument *Index* entspricht, tritt ein Fehler auf. Außerdem unterstützen einige Auflistungen keine benannten Objekte. Für diese Auflistungen müssen Sie Ordnungszahlverweise verwenden.

Die **Item**-Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:

```vb
    collection.Item (Index)
    collection (Index)
```
