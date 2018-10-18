---
<span data-ttu-id="e96c8-101"><<<<<<< HEAD-Titel: DataMember-Eigenschaft (ADO) TOCTitle: DataMember-Eigenschaft (ADO) === Titel: DataMember-Eigenschaft (ADO) TOCTitle: DataMember-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e96c8-101"><<<<<<< HEAD title: DataMember Property (ADO) TOCTitle: DataMember Property (ADO) ======= title: DataMember property (ADO) TOCTitle: DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e96c8-102">Master Ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) Ms:contentKeyID: 48548787 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="e96c8-102">master ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: 48548787 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e96c8-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e96c8-103"><<<<<<< HEAD</span></span>
# <a name="datamember-property-ado"></a><span data-ttu-id="e96c8-104">DataMember-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e96c8-104">DataMember Property (ADO)</span></span>
=======
# <a name="datamember-property-ado"></a><span data-ttu-id="e96c8-105">DataMember-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e96c8-105">DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e96c8-106">master</span><span class="sxs-lookup"><span data-stu-id="e96c8-106">master</span></span>

<span data-ttu-id="e96c8-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e96c8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e96c8-108">Gibt den Namen des Datenelements an, das von dem durch die [DataSource](datasource-property-ado.md)-Eigenschaft angegebenen Objekt abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e96c8-108">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

<span data-ttu-id="e96c8-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e96c8-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="e96c8-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e96c8-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="e96c8-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e96c8-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="e96c8-112">master</span><span class="sxs-lookup"><span data-stu-id="e96c8-112">master</span></span>

<span data-ttu-id="e96c8-p101">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben. Die Groß-/Kleinschreibung wird für den Namen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e96c8-p101">Sets or returns a **String** value. The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="e96c8-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e96c8-115">Remarks</span></span>

<span data-ttu-id="e96c8-p102">Mithilfe dieser Eigenschaft werden datengebundene Steuerelemente mit der Datenumgebung erstellt. Die Datenumgebung verwaltet Datensammlungen (Datenquellen), die benannte Objekte (*Datenelemente*) enthalten und als [Recordset](recordset-object-ado.md)-Objekt dargestellt werden.\*\*</span><span class="sxs-lookup"><span data-stu-id="e96c8-p102">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="e96c8-118">Die Eigenschaften **DataMember** und **DataSource** müssen in Kombination verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e96c8-118">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="e96c8-p103">Die **DataMember** -Eigenschaft bestimmt, welches durch die **DataSource** -Eigenschaft angegebene Objekt als **Recordset** -Objekt dargestellt wird. Das **Recordset** -Objekt muss geschlossen werden, bevor diese Eigenschaft festgelegt wird. Ein Fehler wird generiert, falls die **DataMember** -Eigenschaft nicht vor der **DataSource** -Eigenschaft festgelegt wird oder falls der Name der **DataMember** -Eigenschaft von dem in der **DataSource** -Eigenschaft angegebenen Objekt nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="e96c8-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="e96c8-122">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="e96c8-122">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
