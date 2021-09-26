---
title: DefinedSize-Eigenschaft (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e92929f1973cf30b88d9e9d04f05489f7cfd09a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626799"
---
# <a name="definedsize-property-ado"></a>DefinedSize-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.

## <a name="remarks"></a>Bemerkungen

Mithilfe der **DefinedSize**-Eigenschaft bestimmen Sie die Datenkapazität eines **Field**-Objekts.

Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.

