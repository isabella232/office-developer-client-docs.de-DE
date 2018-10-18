---
<span data-ttu-id="4499e-101"><<<<<<< HEAD-Titel: PageCount-Eigenschaft (ADO) TOCTitle: PageCount-Eigenschaft (ADO) === Titel: PageCount-Eigenschaft (ADO) TOCTitle: PageCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4499e-101"><<<<<<< HEAD title: PageCount Property (ADO) TOCTitle: PageCount Property (ADO) ======= title: PageCount property (ADO) TOCTitle: PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4499e-102">Master Ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) Ms:contentKeyID: 48546609 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="4499e-102">master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="4499e-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="4499e-103"><<<<<<< HEAD</span></span>
# <a name="pagecount-property-ado"></a><span data-ttu-id="4499e-104">PageCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4499e-104">PageCount Property (ADO)</span></span>
=======
# <a name="pagecount-property-ado"></a><span data-ttu-id="4499e-105">PageCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4499e-105">PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4499e-106">master</span><span class="sxs-lookup"><span data-stu-id="4499e-106">master</span></span>


<span data-ttu-id="4499e-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4499e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4499e-108">Gibt an, wie viele Seiten mit Daten das [Recordset](recordset-object-ado.md)-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="4499e-108">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

<span data-ttu-id="4499e-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="4499e-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="4499e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4499e-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="4499e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4499e-111">Return value</span></span>
>>>>>>> <span data-ttu-id="4499e-112">master</span><span class="sxs-lookup"><span data-stu-id="4499e-112">master</span></span>

<span data-ttu-id="4499e-113">Gibt einen **Long** -Wert zurück, der die Anzahl von Seiten im **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="4499e-113">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4499e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4499e-114">Remarks</span></span>

<span data-ttu-id="4499e-p101">Bestimmen Sie mit der PageCount-Eigenschaft, wie viele Seiten mit Daten in einem Recordset-Objekt enthalten sind. Seiten sind Datensatzgruppen, deren Größe der Einstellung der PageSize-Eigenschaft entspricht. Die letzte Seite wird auch dann als weitere Seite im PageCount-Wert gezählt, wenn sie nicht vollständig ist, weil sie weniger Datensätze enthält als der PageSize-Wert angibt. Wird diese Eigenschaft vom Recordset-Objekt nicht unterstützt, gibt der Wert -1 an, dass PageCount nicht bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4499e-p101">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="4499e-119">Weitere Informationen zur Seitenfunktionalität finden Sie unter den Eigenschaften **PageSize** und [AbsolutePage](absolutepage-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4499e-119">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

