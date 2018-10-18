---
<span data-ttu-id="9663a-101"><<<<<<< HEAD-Titel: StayInSync-Eigenschaft (ADO) TOCTitle: StayInSync-Eigenschaft (ADO) === Titel: StayInSync-Eigenschaft (ADO) TOCTitle: StayInSync-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9663a-101"><<<<<<< HEAD title: StayInSync Property (ADO) TOCTitle: StayInSync Property (ADO) ======= title: StayInSync property (ADO) TOCTitle: StayInSync property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9663a-102">Master Ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) Ms:contentKeyID: 48542966 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="9663a-102">master ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: 48542966 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9663a-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="9663a-103"><<<<<<< HEAD</span></span>
# <a name="stayinsync-property-ado"></a><span data-ttu-id="9663a-104">StayInSync-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9663a-104">StayInSync Property (ADO)</span></span>
=======
# <a name="stayinsync-property-ado"></a><span data-ttu-id="9663a-105">StayInSync-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9663a-105">StayInSync property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9663a-106">master</span><span class="sxs-lookup"><span data-stu-id="9663a-106">master</span></span>


<span data-ttu-id="9663a-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9663a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9663a-108">In einem hierarchischen [Recordset](recordset-object-ado.md)-Objekt wird angegeben, ob der Verweis auf die zugrunde liegenden untergeordneten Datensätze (d. h. das *Kapitel*) geändert wird, wenn die Position der übergeordneten Zeile geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9663a-108">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

<span data-ttu-id="9663a-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="9663a-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="9663a-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9663a-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="9663a-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9663a-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="9663a-112">master</span><span class="sxs-lookup"><span data-stu-id="9663a-112">master</span></span>

<span data-ttu-id="9663a-p101">Legt einen **Boolean** -Wert fest oder gibt den Wert zurück. Der Standardwert lautet **True**. Wenn **True** festgelegt ist, wird das Kapitel bei einer Änderung der Zeilenposition des übergeordneten **Recordset** -Objekts aktualisiert. Ist **False** festgelegt, verweist das Kapitel weiterhin auf Daten im vorherigen Kapitel, auch wenn sich die Zeilenposition des übergeordneten **Recordset** -Objekts geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9663a-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="9663a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9663a-116">Remarks</span></span>

<span data-ttu-id="9663a-p102">Diese Eigenschaft gilt für hierarchische Recordsets wie diejenigen, die vom [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) unterstützt werden. Die Eigenschaft muss für das übergeordnete **Recordset** -Objekt festgelegt werden, bevor das untergeordnete **Recordset** -Objekt abgerufen wird. Das Navigieren in hierarchischen Recordsets wird mit dieser Eigenschaft vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9663a-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

