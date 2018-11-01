---
title: Item-Eigenschaft (ADO MD-Zellmenge)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4f2f67daf4bf072037fac07ecdc3cd163904818
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883799"
---
# <a name="item-property-ado-md-cellset"></a>Item-Eigenschaft (ADO MD-Zellmenge)

**Betrifft**: Access 2013, Office 2013

Ruft eine Zelle aus einer Zellmenge mithilfe der entsprechenden Koordinaten ab.

## <a name="syntax"></a>Syntax

*Zielzelle* = *Zellmenge*. Item (*Positionen*)

## <a name="parameters"></a>Parameter

- *Positions*

- Ein **Variant** - **Array** von Werten, die eine Zelle eindeutig angegeben. *Positionen* kann eine der folgenden sein:
    
  - Ein Array mit Positionsnummern
    
  - Ein Array mit Elementnamen
    
  - Die Ordnungsposition

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Item** -Eigenschaft, um ein [Cell](cell-object-ado-md.md)-Objekt in einem [Cellset](cellset-object-ado-md.md)-Objekt zurückzugeben. Wenn die **Item** -Eigenschaft auf die Zelle entspricht dem Argument *Positionen* finden kann, tritt ein Fehler auf.

Die **Item** -Eigenschaft ist die Standardeigenschaft für das **Cellset** -Objekt. Die folgenden Syntaxformen sind austauschbar:

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

Das Argument *Positionen* gibt an, welche Zelle zurückgegeben. Sie können die Zelle anhand ihrer Ordnungsposition oder anhand der einzelnen Achsenpositionen angeben. Wenn Sie die Zelle anhand der Achsenpositionen angeben, können Sie den numerischen Wert der Position oder die Namen der einzelnen Positionselemente angeben.

Die Ordnungsposition ist eine Zahl, durch die eine Zelle innerhalb der**** Zellmenge eindeutig bestimmt wird. Bei diesem Konzept sind die Zellen in einer**** Zellmenge nummeriert, als wäre die**** Zellmenge ein *p*-dimensionales Array, wobei *p* die Anzahl der Achsen darstellt. Zellen sind zeilenweise strukturiert.

Wenn Elementnamen als Zeichenfolgen an **Item** übergeben werden, müssen die Elemente aufsteigend nach numerischen Achsen-IDs sortiert sein. Innerhalb einer Achse müssen die Elemente in Bezug auf die geschachtelten Dimensionen in aufsteigender Reihenfolge aufgeführt sein, d. h. das Element der äußersten Dimension wird zuerst aufgelistet, dann folgen die Elemente der inneren Dimensionen. Jede Dimension sollte durch eine separate Zeichenfolge dargestellt werden, und die einzelnen Elementzeichenfolgen sollten in der Liste durch Kommas voneinander getrennt sein.


> [!NOTE]
> [!HINWEIS] Das Abrufen von Zellen nach Elementnamen wird möglicherweise von Ihrem Datenanbieter nicht unterstützt. Weitere Informationen finden Sie in der Anbieterdokumentation.


