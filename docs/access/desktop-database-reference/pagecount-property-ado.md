---
title: PageCount-Eigenschaft (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aab5455e4fd54316a2ef9af22b5322f85eb3a4e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558142"
---
# <a name="pagecount-property-ado"></a>PageCount-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt an, wie viele Seiten mit Daten das [Recordset](recordset-object-ado.md)-Objekt enthält.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long**-Wert zurück, der die Anzahl von Seiten im **Recordset**-Objekt angibt.

## <a name="remarks"></a>HinwBemerkungeneise

Mit der **PageCount**-Eigenschaft bestimmen Sie die Anzahl der Datenseiten im **Recordset**-Objekt. *Seiten* sind Datensatzgruppen, deren Größe der Einstellung der [PageSize](pagesize-property-ado.md)-Eigenschaft entspricht. Selbst wenn die letzte Seite unvollständig ist, weil weniger Datensätze vorhanden sind, als für die **PageSize**-Eigenschaft angegeben ist, zählt sie als zusätzliche Seite für **PageCount**. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.

Weitere Informationen zur Seitenfunktionalität finden Sie unter den Eigenschaften **PageSize** und [AbsolutePage](absolutepage-property-ado.md).

