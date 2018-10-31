---
<span data-ttu-id="40854-101"><<<<<<< HEAD-Titel: EditMode-Eigenschaft (ADO) TOCTitle: EditMode-Eigenschaft (ADO) === Titel: EditMode-Eigenschaft (ADO) TOCTitle: EditMode-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="40854-101"><<<<<<< HEAD title: EditMode Property (ADO) TOCTitle: EditMode Property (ADO) ======= title: EditMode property (ADO) TOCTitle: EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="40854-102">Master Ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) Ms:contentKeyID: 48543867 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="40854-102">master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="40854-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="40854-103"><<<<<<< HEAD</span></span>
# <a name="editmode-property-ado"></a><span data-ttu-id="40854-104">EditMode-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="40854-104">EditMode Property (ADO)</span></span>
=======
# <a name="editmode-property-ado"></a><span data-ttu-id="40854-105">EditMode-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="40854-105">EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="40854-106">master</span><span class="sxs-lookup"><span data-stu-id="40854-106">master</span></span>


<span data-ttu-id="40854-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40854-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40854-108">Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.</span><span class="sxs-lookup"><span data-stu-id="40854-108">Indicates the editing status of the current record.</span></span>

<span data-ttu-id="40854-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="40854-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="40854-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40854-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="40854-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40854-111">Return value</span></span>
>>>>>>> <span data-ttu-id="40854-112">master</span><span class="sxs-lookup"><span data-stu-id="40854-112">master</span></span>

<span data-ttu-id="40854-113">Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="40854-113">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40854-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40854-114">Remarks</span></span>

<span data-ttu-id="40854-p101">ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="40854-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="40854-119">Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.</span><span class="sxs-lookup"><span data-stu-id="40854-119">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="40854-120">Wenn ein Anruf an [Löschen](delete-method-ado-recordset.md) löscht den Datensatz nicht erfolgreich oder Datensätze in der Datenquelle (aufgrund von referenzielle Integrität Verstöße, beispielsweise), das [Recordset-Objekt](recordset-object-ado.md) im Bearbeitungsmodus bleiben (**EditMode** = \*\*AdEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="40854-120">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="40854-121">Dies bedeutet, dass **CancelUpdate** muss, bevor Sie fortfahren aufgerufen werden deaktiviert den aktuellen Datensatz (mit [Verschieben](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)oder [Schließen](close-method-ado.md), beispielsweise).</span><span class="sxs-lookup"><span data-stu-id="40854-121">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="40854-122">**EditMode** kann nur einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40854-122">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="40854-123">**EditMode** gibt einen Fehler zurück, wenn [BOF oder EOF](bof-eof-properties-ado.md) true ist, oder wenn der aktuelle Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="40854-123">**EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


