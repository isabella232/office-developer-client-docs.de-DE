---
<span data-ttu-id="f93ef-101"><<<<<<< HEAD-Titel: Description-Eigenschaft (ADO) TOCTitle: Description-Eigenschaft (ADO) === Titel: Description-Eigenschaft (ADO) TOCTitle: Description-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f93ef-101"><<<<<<< HEAD title: Description Property (ADO) TOCTitle: Description Property (ADO) ======= title: Description property (ADO) TOCTitle: Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f93ef-102">Master Ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) Ms:contentKeyID: 48544064 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="f93ef-102">master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f93ef-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="f93ef-103"><<<<<<< HEAD</span></span>
# <a name="description-property-ado"></a><span data-ttu-id="f93ef-104">Description-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f93ef-104">Description Property (ADO)</span></span>
=======
# <a name="description-property-ado"></a><span data-ttu-id="f93ef-105">Description-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f93ef-105">Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f93ef-106">master</span><span class="sxs-lookup"><span data-stu-id="f93ef-106">master</span></span>


<span data-ttu-id="f93ef-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f93ef-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f93ef-108">Beschreibt ein [Error](error-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f93ef-108">Describes an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="f93ef-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="f93ef-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f93ef-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f93ef-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f93ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f93ef-111">Return value</span></span>
>>>>>>> <span data-ttu-id="f93ef-112">master</span><span class="sxs-lookup"><span data-stu-id="f93ef-112">master</span></span>

<span data-ttu-id="f93ef-113">Gibt einen Wert vom Datentyp **String** zurück, der eine Beschreibung des Fehlers enthält.</span><span class="sxs-lookup"><span data-stu-id="f93ef-113">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f93ef-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f93ef-114">Remarks</span></span>

<span data-ttu-id="f93ef-p101">Verwenden Sie die **Description** -Eigenschaft, um eine kurze Beschreibung des Fehlers zu erhalten. Zeigen Sie diese Eigenschaft an, um den Benutzer auf einen Fehler hinzuweisen, den Sie nicht behandeln können oder möchten. Die Zeichenfolge stammt aus ADO oder von einem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f93ef-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="f93ef-p102">Die Anbieter sind für das Übergeben eines bestimmten Fehlertexts an ADO verantwortlich. ADO fügt für jeden Anbieterfehler oder jede erhaltene Warnung der [Errors](error-object-ado.md) -Auflistung ein **Error**-Objekt hinzu. Zeigen Sie die **Errors** -Auflistung an, um die vom Anbieter gemeldeten Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f93ef-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

