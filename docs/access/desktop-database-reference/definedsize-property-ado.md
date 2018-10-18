---
<span data-ttu-id="6a2ce-101"><<<<<<< HEAD-Titel: DefinedSize-Eigenschaft (ADO) TOCTitle: DefinedSize-Eigenschaft (ADO) === Titel: DefinedSize-Eigenschaft (ADO) TOCTitle: DefinedSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a2ce-101"><<<<<<< HEAD title: DefinedSize Property (ADO) TOCTitle: DefinedSize Property (ADO) ======= title: DefinedSize property (ADO) TOCTitle: DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6a2ce-102">Master Ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) Ms:contentKeyID: 48546257 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="6a2ce-102">master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6a2ce-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="6a2ce-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-ado"></a><span data-ttu-id="6a2ce-104">DefinedSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a2ce-104">DefinedSize Property (ADO)</span></span>
=======
# <a name="definedsize-property-ado"></a><span data-ttu-id="6a2ce-105">DefinedSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a2ce-105">DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6a2ce-106">master</span><span class="sxs-lookup"><span data-stu-id="6a2ce-106">master</span></span>


<span data-ttu-id="6a2ce-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a2ce-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a2ce-108">Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-108">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="6a2ce-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="6a2ce-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6a2ce-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a2ce-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6a2ce-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a2ce-111">Return value</span></span>
>>>>>>> <span data-ttu-id="6a2ce-112">master</span><span class="sxs-lookup"><span data-stu-id="6a2ce-112">master</span></span>

<span data-ttu-id="6a2ce-113">Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-113">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a2ce-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a2ce-114">Remarks</span></span>

<span data-ttu-id="6a2ce-115">Mithilfe der **DefinedSize** -Eigenschaft bestimmen Sie die Datenkapazität eines **Field** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-115">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="6a2ce-p101">Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

