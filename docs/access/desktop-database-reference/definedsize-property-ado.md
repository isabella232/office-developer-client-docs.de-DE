---
title: DefinedSize-Eigenschaft (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715326"
---
# <a name="definedsize-property-ado"></a>DefinedSize-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.

## <a name="remarks"></a>Hinweise

Mithilfe der **DefinedSize** -Eigenschaft bestimmen Sie die Datenkapazität eines **Field** -Objekts.

Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.

