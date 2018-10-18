---
<span data-ttu-id="ac733-101"><<<<<<< HEAD-Titel: RecordCount-Eigenschaft (ADO) TOCTitle: RecordCount-Eigenschaft (ADO) === Titel: RecordCount-Eigenschaft (ADO) TOCTitle: RecordCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac733-101"><<<<<<< HEAD title: RecordCount Property (ADO) TOCTitle: RecordCount Property (ADO) ======= title: RecordCount property (ADO) TOCTitle: RecordCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ac733-102">Master Ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15) Ms:contentKeyID: 48548304 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="ac733-102">master ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15) ms:contentKeyID: 48548304 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ac733-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ac733-103"><<<<<<< HEAD</span></span>
# <a name="recordcount-property-ado"></a><span data-ttu-id="ac733-104">RecordCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac733-104">RecordCount Property (ADO)</span></span>
=======
# <a name="recordcount-property-ado"></a><span data-ttu-id="ac733-105">RecordCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac733-105">RecordCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ac733-106">master</span><span class="sxs-lookup"><span data-stu-id="ac733-106">master</span></span>


<span data-ttu-id="ac733-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac733-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac733-108">Gibt die Anzahl von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ac733-108">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="ac733-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ac733-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ac733-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac733-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ac733-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac733-111">Return value</span></span>
>>>>>>> <span data-ttu-id="ac733-112">master</span><span class="sxs-lookup"><span data-stu-id="ac733-112">master</span></span>

<span data-ttu-id="ac733-113">Gibt einen **Long** -Wert zurück, der die Anzahl von Datensätzen im **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="ac733-113">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac733-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac733-114">Remarks</span></span>

<span data-ttu-id="ac733-p101">Ermitteln Sie mit der **RecordCount** -Eigenschaft die Anzahl von Datensätzen in einem **Recordset** -Objekt. Die Eigenschaft gibt -1 zurück, wenn ADO die Anzahl von Datensätzen nicht bestimmen kann oder wenn der Anbieter- oder Cursortyp **RecordCount** nicht unterstützt. Das Lesen der **RecordCount** -Eigenschaft für ein geschlossenes **Recordset** -Objekt verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ac733-p101">Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="ac733-p102">Wenn das **Recordset** -Objekt eine ungefähre Positionierung von Textmarken zulässt (d. h. **Supports (adApproxPosition)** oder **Supports (adBookmark)** geben jeweils **True** zurück), entspricht dieser Wert genau der Anzahl von Datensätzen im **Recordset** -Objekt, unabhängig davon, ob es vollständig gefüllt ist. Unterstützt das **Recordset** -Objekt keine ungefähre Positionierung, kann diese Eigenschaften die Ressourcen erheblich beeinträchtigen. Denn es müssen alle Datensätze abgerufen und gezählt werden, damit einen präziser **RecordCount** -Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ac733-p102">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated. If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="ac733-p103">Der Cursortyp des **Recordset** -Objekts beeinflusst die Anzahl von Datensätzen, die ermittelt werden können. Die **RecordCount** -Eigenschaft gibt -1 für einen Vorwärtscursor zurück; die tatsächliche Anzahl für einen statischen oder einen Keyset-Cursor; und je nach Datenquelle entweder -1 oder die tatsächliche Anzahl für einen dynamischen Cursor.</span><span class="sxs-lookup"><span data-stu-id="ac733-p103">The cursor type of the **Recordset** object affects whether the number of records can be determined. The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

