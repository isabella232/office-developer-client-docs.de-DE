---
title: Axes-Auflistung (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8183b0bad1dcbaba33088dffcf21959f5b9fd993
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721479"
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

