---
<span data-ttu-id="9ef51-101"><<<<<<< HEAD-Titel: DataSource-Eigenschaft (ADO) TOCTitle: DataSource-Eigenschaft (ADO) === Titel: DataSource-Eigenschaft (ADO) TOCTitle: DataSource-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ef51-101"><<<<<<< HEAD title: DataSource Property (ADO) TOCTitle: DataSource Property (ADO) ======= title: DataSource property (ADO) TOCTitle: DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9ef51-102">Master Ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) Ms:contentKeyID: 48545087 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="9ef51-102">master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9ef51-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="9ef51-103"><<<<<<< HEAD</span></span>
# <a name="datasource-property-ado"></a><span data-ttu-id="9ef51-104">DataSource-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ef51-104">DataSource Property (ADO)</span></span>
=======
# <a name="datasource-property-ado"></a><span data-ttu-id="9ef51-105">DataSource-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ef51-105">DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9ef51-106">master</span><span class="sxs-lookup"><span data-stu-id="9ef51-106">master</span></span>


<span data-ttu-id="9ef51-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ef51-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9ef51-108">Gibt ein Objekt an, das als [Recordset](recordset-object-ado.md)-Objekt darzustellende Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9ef51-108">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef51-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ef51-109">Remarks</span></span>

<span data-ttu-id="9ef51-p101">Mithilfe dieser Eigenschaft werden datengebundene Steuerelemente mit der Datenumgebung erstellt. Die Datenumgebung verwaltet Datensammlungen (Datenquellen), die benannte Objekte (*Datenelemente*) enthalten und als **Recordset**-Objekt dargestellt werden.\*\*</span><span class="sxs-lookup"><span data-stu-id="9ef51-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="9ef51-112">Die Eigenschaften [DataMember](datamember-property-ado.md) und **DataSource** müssen in Kombination verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ef51-112">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="9ef51-113">Das Objekt, auf das verwiesen wird, muss die **IDataSource** -Schnittstelle implementieren und eine **IRowset** -Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="9ef51-113">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="9ef51-114">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="9ef51-114">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
