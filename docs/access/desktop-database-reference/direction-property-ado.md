---
<span data-ttu-id="2d730-101"><<<<<<< HEAD-Titel: Direction-Eigenschaft (ADO) TOCTitle: Direction-Eigenschaft (ADO) === Titel: Direction-Eigenschaft (ADO) TOCTitle: Direction-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d730-101"><<<<<<< HEAD title: Direction Property (ADO) TOCTitle: Direction Property (ADO) ======= title: Direction property (ADO) TOCTitle: Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2d730-102">Master Ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) Ms:contentKeyID: 48544823 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="2d730-102">master ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2d730-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="2d730-103"><<<<<<< HEAD</span></span>
# <a name="direction-property-ado"></a><span data-ttu-id="2d730-104">Direction-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d730-104">Direction Property (ADO)</span></span>
=======
# <a name="direction-property-ado"></a><span data-ttu-id="2d730-105">Direction-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d730-105">Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2d730-106">master</span><span class="sxs-lookup"><span data-stu-id="2d730-106">master</span></span>


<span data-ttu-id="2d730-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d730-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d730-108">Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter oder einen Ein- und Ausgabeparameter darstellt, oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.</span><span class="sxs-lookup"><span data-stu-id="2d730-108">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

<span data-ttu-id="2d730-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="2d730-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2d730-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2d730-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2d730-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2d730-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2d730-112">master</span><span class="sxs-lookup"><span data-stu-id="2d730-112">master</span></span>

<span data-ttu-id="2d730-113">Mit dieser Eigenschaft wird ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d730-113">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d730-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d730-114">Remarks</span></span>

<span data-ttu-id="2d730-p101">Mit der **Direction** -Eigenschaft geben Sie an, wie ein Parameter an eine oder aus einer Prozedur übergeben wird. Die **Direction** -Eigenschaft bietet Lese-/Schreibzugriff. Dadurch können Sie Anbieter verwenden, die diese Informationen nicht zurückgeben, oder Sie können diese Informationen festlegen, wenn ADO den Anbieter nicht extra aufrufen soll, um Parameterinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d730-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="2d730-p102">Nicht alle Anbieter können die Richtung von Parametern in ihren gespeicherten Prozeduren bestimmen. In diesen Fällen müssen Sie die **Direction** -Eigenschaft festlegen, bevor Sie die Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d730-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

