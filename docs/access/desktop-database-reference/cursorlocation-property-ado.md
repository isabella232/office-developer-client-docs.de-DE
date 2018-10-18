---
<span data-ttu-id="ea2aa-101"><<<<<<< HEAD-Titel: CursorLocation-Eigenschaft (ADO) TOCTitle: CursorLocation-Eigenschaft (ADO) === Titel: CursorLocation-Eigenschaft (ADO) TOCTitle: CursorLocation-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea2aa-101"><<<<<<< HEAD title: CursorLocation Property (ADO) TOCTitle: CursorLocation Property (ADO) ======= title: CursorLocation property (ADO) TOCTitle: CursorLocation property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ea2aa-102">Master Ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15) Ms:contentKeyID: 48546182 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="ea2aa-102">master ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15) ms:contentKeyID: 48546182 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ea2aa-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ea2aa-103"><<<<<<< HEAD</span></span>
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="ea2aa-104">CursorLocation-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea2aa-104">CursorLocation Property (ADO)</span></span>
=======
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="ea2aa-105">CursorLocation-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea2aa-105">CursorLocation property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ea2aa-106">master</span><span class="sxs-lookup"><span data-stu-id="ea2aa-106">master</span></span>


<span data-ttu-id="ea2aa-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea2aa-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ea2aa-108">Gibt die Position des Cursordiensts an.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-108">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ea2aa-109">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ea2aa-109">Settings And Return Values</span></span>

<span data-ttu-id="ea2aa-110">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben, für den einer der [CursorLocationEnum](cursorlocationenum.md)-Werte festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-110">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea2aa-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ea2aa-111">Remarks</span></span>

<span data-ttu-id="ea2aa-p101">Diese Eigenschaft ermöglicht es Ihnen, zwischen verschiedenen Cursorbibliotheken auszuwählen, auf die der Anbieter zugreifen kann. In der Regel können Sie wählen zwischen einer clientseitigen Cursorbibliothek und einer Cursorbibliothek auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="ea2aa-p102">Diese Eigenschaftseinstellung wirkt sich nur auf Verbindungen aus, die nach dem Festlegen der Eigenschaft eingerichtet wurden. Das Ändern der **CursorLocation** -Eigenschaft hat keine Auswirkung auf vorhandene Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="ea2aa-p103">Cursor, die von der [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\))-Methode zurückgegeben werden, erben diese Einstellung. **Recordset** -Objekte erben diese Einstellung automatisch von den zugeordneten Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-p103">Cursors returned by the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="ea2aa-118">Diese Eigenschaft hat Lese-/Schreibzugriff für ein [Connection](connection-object-ado.md)-Objekt oder ein geschlossenes [Recordset](recordset-object-ado.md)-Objekt. Für ein geöffnetes **Recordset** -Objekt ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-118">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="ea2aa-119">**Remote Data Service-Verwendung** Wenn in einem clientseitigen **Recordset** oder **Connection** -Objekt verwendet wird, kann die **CursorLocation** -Eigenschaft nur auf **AdUseClient**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ea2aa-119">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

