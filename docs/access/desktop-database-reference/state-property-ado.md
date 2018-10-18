---
<span data-ttu-id="5a852-101"><<<<<<< HEAD-Titel: Status-Eigenschaft (ADO) TOCTitle: Status-Eigenschaft (ADO) === Titel: State-Eigenschaft (ADO) TOCTitle: State-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5a852-101"><<<<<<< HEAD title: State Property (ADO) TOCTitle: State Property (ADO) ======= title: State property (ADO) TOCTitle: State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5a852-102">Master Ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) Ms:contentKeyID: 48547053 ms.date: 09/18/2015 Mtps_version: Office. 15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="5a852-102">master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="5a852-103">ado210.chm1231176 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="5a852-103">ado210.chm1231176 f1_categories:</span></span>
- <span data-ttu-id="5a852-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="5a852-104">Office.Version=v15</span></span>
---

<span data-ttu-id="5a852-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5a852-105"><<<<<<< HEAD</span></span>
# <a name="state-property-ado"></a><span data-ttu-id="5a852-106">State-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5a852-106">State Property (ADO)</span></span>
=======
# <a name="state-property-ado"></a><span data-ttu-id="5a852-107">State-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5a852-107">State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5a852-108">master</span><span class="sxs-lookup"><span data-stu-id="5a852-108">master</span></span>


<span data-ttu-id="5a852-109">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a852-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5a852-110">Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt.</span><span class="sxs-lookup"><span data-stu-id="5a852-110">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="5a852-111">Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).</span><span class="sxs-lookup"><span data-stu-id="5a852-111">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

<span data-ttu-id="5a852-112"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5a852-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5a852-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a852-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5a852-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a852-114">Return value</span></span>
>>>>>>> <span data-ttu-id="5a852-115">master</span><span class="sxs-lookup"><span data-stu-id="5a852-115">master</span></span>

<span data-ttu-id="5a852-p101">Gibt einen **Long** -Wert zurück, bei dem es sich um einen [ObjectStateEnum](objectstateenum.md)-Wert handeln kann. Der Standardwert ist **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="5a852-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a852-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a852-118">Remarks</span></span>

<span data-ttu-id="5a852-119">Mit der **State** -Eigenschaft können Sie jederzeit den aktuellen Status eines bestimmten Objekts ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5a852-119">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="5a852-p102">Die **State** -Eigenschaft des Objekts kann kombinierte Werte besitzen. Wenn beispielsweise eine Anweisung ausgeführt wird, besitzt die Eigenschaft einen aus **adStateOpen** und **adStateExecuting** bestehenden kombinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="5a852-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="5a852-122">Die **State** -Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5a852-122">The **State** property is read-only.</span></span>

