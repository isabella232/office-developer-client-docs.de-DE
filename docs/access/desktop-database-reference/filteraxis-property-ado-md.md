---
title: FilterAxis-Eigenschaft (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a2bd438f2556aea44785922dd399aeb47940a78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581154"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt Filterinformationen zur aktuellen Zellmenge an.

## <a name="return-values"></a>Rückgabewerte

Gibt ein schreibgeschütztes [Axis](axis-object-ado-md.md)-Objekt zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **FilterAxis** -Eigenschaft, um Informationen zu den Dimensionen zurückzugeben, die zum Segmentieren von Daten verwendet wurden. Die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft des **Axis** -Objekts gibt gibt die Anzahl der Dimensionen zurück. Diese Achse verfügt normalerweise nur über eine Zeile.

Das **Axis** -Objekt, das von [FilterAxis](filteraxis-property-ado-md.md) zurückgegeben wird, ist nicht in der [Axes](axes-collection-ado-md.md)-Auflistung für ein [Cellset](cellset-object-ado-md.md)-Objekt vorhanden.

