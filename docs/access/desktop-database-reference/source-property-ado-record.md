---
title: Source-Eigenschaft (ADO Record)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d6e010ce8db93baaf8faddaeff5ab4dabda6a84
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603385"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="b5673-102">Source-Eigenschaft (ADO Record)</span><span class="sxs-lookup"><span data-stu-id="b5673-102">Source Property (ADO Record)</span></span>


<span data-ttu-id="b5673-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5673-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b5673-104">Gibt die vom [Record](record-object-ado.md)-Objekt dargestellte Datenquelle oder das Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b5673-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

<span data-ttu-id="b5673-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b5673-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b5673-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b5673-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b5673-107">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b5673-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b5673-108">master</span><span class="sxs-lookup"><span data-stu-id="b5673-108">master</span></span>

<span data-ttu-id="b5673-109">Legt einen **Variant** -Wert fest, der die vom **Record** -Objekt dargestellte Entität angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b5673-109">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5673-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5673-110">Remarks</span></span>

<span data-ttu-id="b5673-111">Die **Source** -Eigenschaft gibt das Argument *Source* die [Open](open-method-ado-record.md) -Methode des **Record** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="b5673-111">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="b5673-112">Sie kann die Zeichenfolge einer absoluten oder relativen URL enthalten.</span><span class="sxs-lookup"><span data-stu-id="b5673-112">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="b5673-113">Eine absolute URL kann verwendet werden, ohne dass die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft festgelegt werden muss, um das **Record** -Objekt direkt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5673-113">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="b5673-114">In diesem Fall wird ein implizites **Connection** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5673-114">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="b5673-115">Die **Source** -Eigenschaft kann auch einen Verweis auf ein bereits geöffnetes **Recordset** -Objekt enthalten. Dadurch wird ein **Record** -Objekt geöffnet, das die aktuelle Zeile im **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5673-115">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="b5673-116">Außerdem kann die **Source** -Eigenschaft einen Verweis auf ein [Command](command-object-ado.md)-Objekt enthalten, das eine einzelne Datenzeile vom Anbieter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b5673-116">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="b5673-p102">Wenn die **ActiveConnection** -Eigenschaft ebenfalls festgelegt ist, muss die **Source** -Eigenschaft auf ein Objekt verweisen, das im Bereich dieser Verbindung vorhanden ist. Wenn z. B. in einem strukturierten Namespace die **Source** -Eigenschaft eine absolute URL enthält, muss sie auf einen Knoten zeigen, der innerhalb des Knotenbereichs vorhanden ist, der durch die URL in der Verbindungszeichenfolge identifiziert wird. Enthält die **Source** -Eigenschaft eine relative URL, dann wird sie innerhalb des Kontexts überprüft, der von der **ActiveConnection** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b5673-p102">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection. For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string. If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="b5673-120">Die **Source** -Eigenschaft ist nicht schreibgeschützt, wenn das **Record** -Objekt geschlossen ist, und schreibgeschützt, wenn das **Record** -Objekt geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b5673-120">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

<span data-ttu-id="b5673-121"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b5673-121"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="b5673-p103">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="b5673-p103">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> [!NOTE]
> <span data-ttu-id="b5673-124">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b5673-124">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="b5673-125">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="b5673-125">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="b5673-126">master</span><span class="sxs-lookup"><span data-stu-id="b5673-126">master</span></span>


