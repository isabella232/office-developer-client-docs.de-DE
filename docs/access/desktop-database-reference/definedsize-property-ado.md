---
title: DefinedSize-Eigenschaft (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868854"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="684eb-102">DefinedSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="684eb-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="684eb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="684eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="684eb-104">Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="684eb-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="684eb-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="684eb-105">Return value</span></span>

<span data-ttu-id="684eb-106">Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="684eb-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="684eb-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="684eb-107">Remarks</span></span>

<span data-ttu-id="684eb-108">Mithilfe der **DefinedSize** -Eigenschaft bestimmen Sie die Datenkapazität eines **Field** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="684eb-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="684eb-p101">Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="684eb-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

