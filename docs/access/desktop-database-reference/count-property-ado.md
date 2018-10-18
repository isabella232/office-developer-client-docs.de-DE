---
<span data-ttu-id="c3ac2-101"><<<<<<< HEAD-Titel: Count-Eigenschaft (ADO) TOCTitle: Count-Eigenschaft (ADO) === Titel: Count-Eigenschaft (ADO) TOCTitle: Count-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c3ac2-101"><<<<<<< HEAD title: Count Property (ADO) TOCTitle: Count Property (ADO) ======= title: Count property (ADO) TOCTitle: Count property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c3ac2-102">Master Ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15) Ms:contentKeyID: 48547253 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="c3ac2-102">master ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15) ms:contentKeyID: 48547253 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c3ac2-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="c3ac2-103"><<<<<<< HEAD</span></span>
# <a name="count-property-ado"></a><span data-ttu-id="c3ac2-104">Count-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c3ac2-104">Count Property (ADO)</span></span>
=======
# <a name="count-property-ado"></a><span data-ttu-id="c3ac2-105">Count-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c3ac2-105">Count property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c3ac2-106">master</span><span class="sxs-lookup"><span data-stu-id="c3ac2-106">master</span></span>


<span data-ttu-id="c3ac2-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3ac2-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c3ac2-108">Gibt die Anzahl von Objekten in einer Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-108">Indicates the number of objects in a collection.</span></span>

<span data-ttu-id="c3ac2-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="c3ac2-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="c3ac2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3ac2-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="c3ac2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3ac2-111">Return value</span></span>
>>>>>>> <span data-ttu-id="c3ac2-112">master</span><span class="sxs-lookup"><span data-stu-id="c3ac2-112">master</span></span>

<span data-ttu-id="c3ac2-113">Gibt einen Wert vom Datentyp **Long** zurück.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-113">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ac2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c3ac2-114">Remarks</span></span>

<span data-ttu-id="c3ac2-115">Mit der **Count** -Eigenschaft bestimmen Sie, wie viele Objekte in einer bestimmten Auflistung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-115">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="c3ac2-p101">Die Nummerierung für Auflistungselemente beginnt bei Null, weshalb Sie im Code Schleifen stets mit dem Element Null beginnen und mit dem Wert der **Count** -Eigenschaft minus 1 beenden sollten. Falls Sie Microsoft Visual Basic verwenden und Schleifen durch die Auflistungselemente ausführen möchten, ohne die **Count** -Eigenschaft zu überprüfen, verwenden Sie den Befehl **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="c3ac2-118">Wenn die **Count** -Eigenschaft gleich null ist, sind in der Auflistung keine Objekte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-118">If the **Count** property is zero, there are no objects in the collection.</span></span>

