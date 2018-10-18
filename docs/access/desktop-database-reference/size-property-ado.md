---
<span data-ttu-id="45295-101"><<<<<<< HEAD-Titel: Size-Eigenschaft (ADO) TOCTitle: Size-Eigenschaft (ADO) === Titel: Größe-Eigenschaft (ADO) TOCTitle: Größe-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="45295-101"><<<<<<< HEAD title: Size Property (ADO) TOCTitle: Size Property (ADO) ======= title: Size property (ADO) TOCTitle: Size property (ADO)</span></span>
>>>>>>> <span data-ttu-id="45295-102">Master Ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15) Ms:contentKeyID: 48543753 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="45295-102">master ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15) ms:contentKeyID: 48543753 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="45295-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="45295-103"><<<<<<< HEAD</span></span>
# <a name="size-property-ado"></a><span data-ttu-id="45295-104">Size-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="45295-104">Size Property (ADO)</span></span>
=======
# <a name="size-property-ado"></a><span data-ttu-id="45295-105">Size-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="45295-105">Size property (ADO)</span></span>
>>>>>>> <span data-ttu-id="45295-106">master</span><span class="sxs-lookup"><span data-stu-id="45295-106">master</span></span>


<span data-ttu-id="45295-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="45295-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45295-108">Gibt die maximale Größe eines [Parameter](parameter-object-ado.md)-Objekts in Bytes oder Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="45295-108">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

<span data-ttu-id="45295-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="45295-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="45295-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="45295-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="45295-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="45295-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="45295-112">master</span><span class="sxs-lookup"><span data-stu-id="45295-112">master</span></span>

<span data-ttu-id="45295-113">Legt einen **Long** -Wert fest, der die maximale Größe eines Werts in einem **Parameter** -Objekt in Bytes oder Zeichen angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="45295-113">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="45295-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45295-114">Remarks</span></span>

<span data-ttu-id="45295-115">Bestimmen Sie mit der **Size** -Eigenschaft die maximale Größe von Werten, die in die [Value](value-property-ado.md)-Eigenschaft eines **Parameter** -Objekts geschrieben oder daraus gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="45295-115">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="45295-116">Wenn Sie einen Datentyp variabler Länge für ein **Parameter**-Objekt angeben (beispielsweise einen beliebigen **String**-Typ wie z. B. **adVarChar**), müssen Sie die **Size**-Eigenschaft festlegen, bevor Sie sie der [Parameters](parameters-collection-ado.md)-Auflistung anfügen. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="45295-116">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="45295-117">Wenn Sie das **Parameter** -Objekt bereits der **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts angefügt haben und seinen Typ in einen Datentyp variabler Länge ändern, müssen Sie die **Size** -Eigenschaft des **Parameter** -Objekts festlegen, bevor Sie das **Command** -Objekt ausführen. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="45295-117">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="45295-p101">Wenn Sie die [Refresh](refresh-method-ado.md)-Methode verwenden, um Parameterinformationen vom Anbieter zu erhalten, und ein oder mehrere **Parameter** -Objekte mit einem Datentyp variabler Länge zurückgegeben werden, reserviert ADO möglicherweise Speicher entsprechend der maximal möglichen Größe der Parameter. Das kann einen Fehler während der Ausführung verursachen. Damit kein Fehler auftritt, sollten Sie die **Size** -Eigenschaft für diese Parameter explizit festlegen, bevor Sie den Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="45295-p101">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution. To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="45295-120">Die **Size** -Eigenschaft ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="45295-120">The **Size** property is read/write.</span></span>

