---
<span data-ttu-id="5813a-101"><<<<<<< HEAD-Titel: Anzahl-Eigenschaft (ADO) TOCTitle: Anzahl-Eigenschaft (ADO) === Titel: Number-Eigenschaft (ADO) TOCTitle: Number-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5813a-101"><<<<<<< HEAD title: Number Property (ADO) TOCTitle: Number Property (ADO) ======= title: Number property (ADO) TOCTitle: Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5813a-102">Master Ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) Ms:contentKeyID: 48547243 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="5813a-102">master ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5813a-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5813a-103"><<<<<<< HEAD</span></span>
# <a name="number-property-ado"></a><span data-ttu-id="5813a-104">Number-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5813a-104">Number Property (ADO)</span></span>
=======
# <a name="number-property-ado"></a><span data-ttu-id="5813a-105">Number-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5813a-105">Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5813a-106">master</span><span class="sxs-lookup"><span data-stu-id="5813a-106">master</span></span>


<span data-ttu-id="5813a-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5813a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5813a-108">Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5813a-108">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="5813a-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5813a-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5813a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5813a-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5813a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5813a-111">Return value</span></span>
>>>>>>> <span data-ttu-id="5813a-112">master</span><span class="sxs-lookup"><span data-stu-id="5813a-112">master</span></span>

<span data-ttu-id="5813a-113">Gibt einen **Long** -Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="5813a-113">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="5813a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5813a-114">Remarks</span></span>

<span data-ttu-id="5813a-p101">Ermitteln Sie mit der **Number** -Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.</span><span class="sxs-lookup"><span data-stu-id="5813a-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="5813a-117">Die [Errors](errors-collection-ado.md) -Auflistung gibt ein HRESULT im Hexadezimal-Format (beispielsweise 0 x 80004005) oder long-Wert (beispielsweise 2147467259) zurück.</span><span class="sxs-lookup"><span data-stu-id="5813a-117">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="5813a-118">Diese HRESULT-Werte können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5813a-118">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="5813a-119">Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 von der *OLE DB-Programmierreferenz.*</span><span class="sxs-lookup"><span data-stu-id="5813a-119">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

