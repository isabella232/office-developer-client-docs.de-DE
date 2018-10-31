---
title: CopyRecord-Methode (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01141e0dc2445a91267cf7744214b906a1af3fd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860343"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="a32d0-102">CopyRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a32d0-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="a32d0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a32d0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a32d0-104">Kopiert eine durch einen **Record** dargestellte Entität an einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="a32d0-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32d0-105">Syntax</span></span>

<span data-ttu-id="a32d0-106">*Datensatz*. CopyRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="a32d0-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="a32d0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32d0-107">Parameters</span></span>

  - <span data-ttu-id="a32d0-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="a32d0-108">*Source*</span></span>

  - <span data-ttu-id="a32d0-109">Optional.</span><span class="sxs-lookup"><span data-stu-id="a32d0-109">Optional.</span></span> <span data-ttu-id="a32d0-110">Ein **String** -Wert, der eine URL, die Entität kopiert werden soll (beispielsweise eine Datei oder ein Verzeichnis) enthält.</span><span class="sxs-lookup"><span data-stu-id="a32d0-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="a32d0-111">Wenn *Source* ausgelassen wird oder eine leere Zeichenfolge angibt, wird die Datei oder das Verzeichnis vom aktuellen [Datensatz](record-object-ado.md) dargestellt kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="a32d0-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="a32d0-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="a32d0-112">*Destination*</span></span>

  - <span data-ttu-id="a32d0-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="a32d0-113">Optional.</span></span> <span data-ttu-id="a32d0-114">Ein **String** -Wert, der eine URL des Speicherorts, in dem *Quelle* kopiert werden, enthält.</span><span class="sxs-lookup"><span data-stu-id="a32d0-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="a32d0-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="a32d0-115">*UserName*</span></span>

  - <span data-ttu-id="a32d0-p103">Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="a32d0-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="a32d0-118">*Password*</span></span>

  - <span data-ttu-id="a32d0-p104">Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="a32d0-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="a32d0-121">*Options*</span></span>

  - <span data-ttu-id="a32d0-p105">Optional. Ein [CopyRecordOptionsEnum](copyrecordoptionsenum.md)-Wert, der den Standardwert **adCopyUnspecified** besitzt. Gibt das Verhalten dieser Methode an.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="a32d0-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="a32d0-125">*Async*</span></span>

  - <span data-ttu-id="a32d0-p106">Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass dieser Vorgang asynchron sein soll.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

<span data-ttu-id="a32d0-128"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a32d0-128"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a32d0-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a32d0-129">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a32d0-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a32d0-130">Return value</span></span>
>>>>>>> <span data-ttu-id="a32d0-131">master</span><span class="sxs-lookup"><span data-stu-id="a32d0-131">master</span></span>

<span data-ttu-id="a32d0-p107">Ein **String**-Wert, der in der Regel den Wert für *Destination* zurückgibt. Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="a32d0-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a32d0-134">Remarks</span></span>

<span data-ttu-id="a32d0-135">Die Werte der *Quell-* und *Zielserver* dürfen nicht identisch sein; andernfalls tritt ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="a32d0-135">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="a32d0-136">Mindestens einer der Server-, Pfad- oder Ressourcennamen muss unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="a32d0-136">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="a32d0-p109">Wenn **adCopyNonRecursive** nicht angegeben ist, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) von *Source* rekursiv kopiert. Bei einem rekursiven Vorgang darf es sich bei der *Destination* nicht um ein Unterverzeichnis von *Source* handeln, andernfalls kann der Vorgang nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="a32d0-139">Diese Methode schlägt fehl, wenn das *Ziel* eine vorhandene Entität (beispielsweise eine Datei oder ein Verzeichnis) identifiziert, es sei denn, **AdCopyOverWrite** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a32d0-139">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="a32d0-140">[!WICHTIG] Verwenden Sie die Option **adCopyOverWrite** nur nach sorgfältiger Überlegung.</span><span class="sxs-lookup"><span data-stu-id="a32d0-140">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="a32d0-141">Beispielsweise wird durch das Angeben dieser Option beim Kopieren einer Datei in ein Verzeichnis das Verzeichnis wird *Löschen* und Ersetzen Sie ihn mit der Datei.</span><span class="sxs-lookup"><span data-stu-id="a32d0-141">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>




> [!NOTE]
<span data-ttu-id="a32d0-142"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a32d0-142"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="a32d0-p111">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="a32d0-p111">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="a32d0-145">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a32d0-145">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="a32d0-146">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="a32d0-146">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="a32d0-147">master</span><span class="sxs-lookup"><span data-stu-id="a32d0-147">master</span></span>


