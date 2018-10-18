---
title: ChildCount-Eigenschaft (ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84e2e9873e076128c42e9fa7ae46d902f47865c7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606024"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="ad716-102">ChildCount-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ad716-102">ChildCount Property (ADO MD)</span></span>


<span data-ttu-id="ad716-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad716-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad716-104">Gibt die Anzahl von Elementen an, für die das aktuelle [Member](member-object-ado-md.md)-Objekt das übergeordnete Objekt (Hauptobjekt) in einer Hierarchie ist.</span><span class="sxs-lookup"><span data-stu-id="ad716-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

<span data-ttu-id="ad716-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ad716-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="ad716-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad716-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="ad716-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ad716-107">Return values</span></span>
>>>>>>> <span data-ttu-id="ad716-108">master</span><span class="sxs-lookup"><span data-stu-id="ad716-108">master</span></span>

<span data-ttu-id="ad716-109">Gibt einen schreibgeschützten, ganzzahligen **Long** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad716-109">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad716-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad716-110">Remarks</span></span>

<span data-ttu-id="ad716-p101">Verwenden Sie die **ChildCount** -Eigenschaft, um eine geschätzte Anzahl von untergeordneten Elementen eines **Member** -Objekts zurückzugeben. Die tatsächliche Anzahl von untergeordneten Elementen eines **Member** -Objekts kann durch die [Children](children-property-ado-md.md)-Eigenschaft zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad716-p101">Use the **ChildCount** property to return an estimate of how many children a **Member** has. The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="ad716-p102">Für **Member** -Objekte aus einem [Position](position-object-ado-md.md)-Objekt beträgt die maximal zurückgegebene Anzahl 65536. Wenn die tatsächliche Anzahl untergeordneter Elemente den Wert 65536 überschreitet, bleibt der Rückgabewert 65536. Die Anwendung sollte eine **ChildCount** -Eigenschaft von 65536 als größer/gleich 65536 untergeordnete Elemente interpretieren.</span><span class="sxs-lookup"><span data-stu-id="ad716-p102">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536. If the actual number of children exceeds 65536, the value returned will still be 65536. Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="ad716-p103">Verwenden Sie für **Member** -Objekte aus einem [Level](level-object-ado-md.md)-Objekt die ADO-[Count](count-property-ado.md)-Auflistungseigenschaft für die **Children** -Auflistung, um die genaue Anzahl von untergeordneten Elementen zu bestimmen. Das Bestimmen der genauen Anzahl untergeordneter Elemente kann einige Zeit dauern, wenn die Anzahl von untergeordneten Elementen in der Auflistung groß ist.</span><span class="sxs-lookup"><span data-stu-id="ad716-p103">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children. Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

