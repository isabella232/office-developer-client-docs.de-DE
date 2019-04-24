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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294134"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="ae2f2-102">DefinedSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="ae2f2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae2f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae2f2-104">Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae2f2-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae2f2-105">Return value</span></span>

<span data-ttu-id="ae2f2-106">Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2f2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2f2-107">Remarks</span></span>

<span data-ttu-id="ae2f2-108">Mithilfe der **DefinedSize**-Eigenschaft bestimmen Sie die Datenkapazität eines **Field**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="ae2f2-p101">Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

