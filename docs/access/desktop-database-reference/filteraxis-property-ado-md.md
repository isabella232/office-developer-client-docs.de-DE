---
title: FilterAxis-Eigenschaft (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713268"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt Filterinformationen zur aktuellen Zellmenge an.

## <a name="return-values"></a>Rückgabewerte

Gibt ein schreibgeschütztes [Axis](axis-object-ado-md.md)-Objekt zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **FilterAxis** -Eigenschaft, um Informationen zu den Dimensionen zurückzugeben, die zum Segmentieren von Daten verwendet wurden. Die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft des **Axis** -Objekts gibt gibt die Anzahl der Dimensionen zurück. Diese Achse verfügt normalerweise nur über eine Zeile.

Das **Axis** -Objekt, das von [FilterAxis](filteraxis-property-ado-md.md) zurückgegeben wird, ist nicht in der [Axes](axes-collection-ado-md.md)-Auflistung für ein [Cellset](cellset-object-ado-md.md)-Objekt vorhanden.

