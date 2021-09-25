---
title: Neugestaltung (Access-Desktopdatenbankreferenz)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: af282f86f75d6208be19ab7c8b491dfd8b17dc92
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557820"
---
# <a name="reshaping"></a>Reshaping

**Gilt für**: Access 2013, Office 2013

Einem **Recordset**-Objekt, das mit einer Klausel eines Shape-Befehls erstellt wird, kann ein *Aliasname* zugewiesen werden (in der Regel mit dem AS-Schlüsselwort). Auf den Alias eines strukturierten **Recordset**-Objekts kann in einem völlig anderen Befehl verwiesen werden. Das heißt, dass Sie ein zuvor strukturiertes **Recordset**-Objekt in einem neuen Shape-Befehl erneut verwenden bzw. *umstrukturieren* können. Zur Unterstützung dieses Features stellt ADO eine Eigenschaft [Reshape Name](reshape-name-property-dynamic-ado.md) bereit.

Die Umstrukturierung erfüllt zwei Hauptfunktionen. Die erste Funktion besteht darin, einem vorhandenen **Recordset**-Objekt ein neues übergeordnetes **Recordset**-Objekt zuzuordnen.

## <a name="example"></a>Beispiel

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

Die zweite Funktion besteht darin, mithilfe der Syntax nicht kapitelbasierten Zugriff auf vorhandene untergeordnete **Recordset-Objekte** zu `"SHAPE <recordset reshape name>"` ermöglichen.

> [!NOTE]
> [!HINWEIS] Sie können keine Spalten an ein vorhandenes **Recordset** -Objekt anfügen, kein parametrisiertes **Recordset** -Objekt oder **Recordset** -Objekte in einer dazwischen liegenden COMPUTE-Klausel umstrukturieren und keine Aggregatoperationen zu einem **Recordset** -Objekt ausführen, das von dem umzustrukturierenden **Recordset** abstammt. Das **Recordset-Objekt, das** neu gestaltet wird, und der neue Shape-Befehl müssen beide dasselbe **[Connection-Objekt](connection-object-ado.md) verwenden.


