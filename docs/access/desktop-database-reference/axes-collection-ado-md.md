---
title: Axes-Auflistung (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88bf27f406a439d051112afb9abf94697a13b12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922231"
---
# <a name="axes-collection-ado-md"></a>Axes-Auflistung (ADO MD)


**Betrifft**: Access 2013, Office 2013

Enthält die [Axis](axis-object-ado-md.md)-Objekte, die eine Zellmenge definieren.

## <a name="remarks"></a>Hinweise

Ein [Cellset](cellset-object-ado-md.md)-Objekt enthält eine **Axes** -Auflistung. Nach dem Öffnen des **Cellset** -Objekts enthält diese Auflistung mindestens ein **Axis** -Objekt. Eine ausführlichere Erläuterung zum Verwenden von [Axis](axis-object-ado-md.md) -Objekten finden Sie im Thema zum **Axis**-Objekt.


> [!NOTE]
> [!HINWEIS] Die Filterachse eines **Cellset** -Objekts ist nicht in der **Axes** -Auflistung enthalten. Weitere Informationen finden Sie im Thema zur [FilterAxis](filteraxis-property-ado-md.md)-Eigenschaft.



**Axes** ist eine ADO-Standardauflistung. Die Eigenschaften und Methoden einer Auflistung ermöglichen Folgendes:

  - Abrufen der Anzahl an Objekten in der Auflistung, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben eines Objekts aus der Auflistung, indem Sie die Standardeigenschaft [Item](item-property-ado.md) verwenden.

  - Aktualisieren der Objekte in der Auflistung aus dem Anbieter, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

