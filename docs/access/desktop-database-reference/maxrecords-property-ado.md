---
<span data-ttu-id="8b8b0-101"><<<<<<< HEAD-Titel: MaxRecords-Eigenschaft (ADO) TOCTitle: MaxRecords-Eigenschaft (ADO) === Titel: MaxRecords-Eigenschaft (ADO) TOCTitle: MaxRecords-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b8b0-101"><<<<<<< HEAD title: MaxRecords Property (ADO) TOCTitle: MaxRecords Property (ADO) ======= title: MaxRecords property (ADO) TOCTitle: MaxRecords property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8b8b0-102">Master Ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) Ms:contentKeyID: 48544475 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="8b8b0-102">master ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: 48544475 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8b8b0-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8b8b0-103"><<<<<<< HEAD</span></span>
# <a name="maxrecords-property-ado"></a><span data-ttu-id="8b8b0-104">MaxRecords-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b8b0-104">MaxRecords Property (ADO)</span></span>
=======
# <a name="maxrecords-property-ado"></a><span data-ttu-id="8b8b0-105">MaxRecords-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b8b0-105">MaxRecords property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8b8b0-106">master</span><span class="sxs-lookup"><span data-stu-id="8b8b0-106">master</span></span>


<span data-ttu-id="8b8b0-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b8b0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8b8b0-108">Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b8b0-108">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

<span data-ttu-id="8b8b0-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8b8b0-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8b8b0-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8b8b0-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8b8b0-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8b8b0-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8b8b0-112">master</span><span class="sxs-lookup"><span data-stu-id="8b8b0-112">master</span></span>

<span data-ttu-id="8b8b0-p101">Legt einen Long-Wert fest, der die maximale Anzahl von zurückgegebenen Datensätzen angibt, oder gibt den Wert zurück. Der Standardwert ist Null (kein Limit).</span><span class="sxs-lookup"><span data-stu-id="8b8b0-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b8b0-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b8b0-115">Remarks</span></span>

<span data-ttu-id="8b8b0-116">Verwenden Sie die **MaxRecords** -Eigenschaft zur Begrenzung der Anzahl von Datensätzen, die der Anbieter aus der Datenquelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8b8b0-116">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="8b8b0-117">Die Standardeinstellung dieser Eigenschaft ist NULL und bedeutet, dass der Anbieter alle angeforderten Datensätze zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8b8b0-117">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="8b8b0-118">Die **MaxRecords** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8b8b0-118">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

