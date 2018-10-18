---
<span data-ttu-id="e469a-101">Titel: EOS-Eigenschaft (ADO - Access-desktop-Datenbank (engl.))) <<<<<<< HEAD TOCTitle: EOS-Eigenschaft (ADO) === TOCTitle: EOS-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e469a-101">title: EOS Property (ADO - Access desktop database reference)) <<<<<<< HEAD TOCTitle: EOS Property (ADO) ======= TOCTitle: EOS property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e469a-102">Master Ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15) Ms:contentKeyID: 48546474 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="e469a-102">master ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15) ms:contentKeyID: 48546474 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e469a-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e469a-103"><<<<<<< HEAD</span></span>
# <a name="eos-property-ado"></a><span data-ttu-id="e469a-104">EOS-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e469a-104">EOS Property (ADO)</span></span>
=======
# <a name="eos-property-ado"></a><span data-ttu-id="e469a-105">EOS-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e469a-105">EOS property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e469a-106">master</span><span class="sxs-lookup"><span data-stu-id="e469a-106">master</span></span>


<span data-ttu-id="e469a-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e469a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e469a-108">Gibt an, ob sich die aktuelle Position am Ende des Datenstroms befindet.</span><span class="sxs-lookup"><span data-stu-id="e469a-108">Indicates whether the current position is at the end of the stream.</span></span>

<span data-ttu-id="e469a-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e469a-109"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="e469a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e469a-110">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="e469a-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e469a-111">Return values</span></span>
>>>>>>> <span data-ttu-id="e469a-112">master</span><span class="sxs-lookup"><span data-stu-id="e469a-112">master</span></span>

<span data-ttu-id="e469a-p101">Gibt einen Wert vom Datentyp **Boolean** zurück, der angibt, ob sich die aktuelle Position am Ende des Datenstroms befindet. **EOS** gibt **True** zurück, wenn keine Bytes mehr im Datenstrom vorhanden sind. Wenn auf die aktuelle Position noch Bytes folgen, wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e469a-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="e469a-p102">Verwenden Sie die [SetEOS](seteos-method-ado.md)-Methode, um das Ende der Datenstromposition festzulegen. Mithilfe der [Position](position-property-ado.md)-Eigenschaft bestimmen Sie die aktuelle Position.</span><span class="sxs-lookup"><span data-stu-id="e469a-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

