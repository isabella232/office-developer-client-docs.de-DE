---
title: DefinedSize-Eigenschaft (ADO)
TOCTitle: DefinedSize Property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8ffd8bb24abcab737ebc4bb23a0af717c02d486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473214"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="b3a89-102">DefinedSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="b3a89-102">DefinedSize Property (ADO)</span></span>


<span data-ttu-id="b3a89-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3a89-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3a89-104">Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b3a89-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3a89-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3a89-105">Return Value</span></span>

<span data-ttu-id="b3a89-106">Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="b3a89-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a89-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3a89-107">Remarks</span></span>

<span data-ttu-id="b3a89-108">Mithilfe der **DefinedSize** -Eigenschaft bestimmen Sie die Datenkapazität eines **Field** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b3a89-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="b3a89-p101">Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3a89-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

