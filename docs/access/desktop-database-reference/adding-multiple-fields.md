---
title: Hinzufügen mehrerer Felder
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01330eeed2645a0bd76f6ac51e96542068b245e7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878976"
---
# <a name="adding-multiple-fields"></a>Hinzufügen mehrerer Felder


**Betrifft**: Access 2013, Office 2013

Hin und wieder kann es effizienter sein, ein Array von Feldern und die entsprechenden Werte an die **AddNew** -Methode zu übergeben, anstatt **Value** mehrmals für jedes neue Feld festzulegen. Wenn *FieldList* ein Array ist, muss *Werte* auch ein Array mit der gleichen Anzahl von Elementen sein; andernfalls, tritt ein Fehler auf. Die Reihenfolge der Feldnamen muss der Reihenfolge der Feldwerte in jedem Array entsprechen. Mit dem folgenden Code wird ein Array von Feldern und ein Array von Werten an die **AddNew** -Methode übergeben.

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

