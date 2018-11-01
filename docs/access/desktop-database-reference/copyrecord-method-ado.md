---
title: CopyRecord-Methode (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9daa27f5a5e31aac295babf6f40b32f89a9df5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874965"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="8e4ed-102">CopyRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e4ed-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="8e4ed-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e4ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e4ed-104">Kopiert eine durch einen **Record** dargestellte Entität an einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4ed-105">Syntax</span></span>

<span data-ttu-id="8e4ed-106">*Datensatz*. CopyRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="8e4ed-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="8e4ed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4ed-107">Parameters</span></span>

  - <span data-ttu-id="8e4ed-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="8e4ed-108">*Source*</span></span>

  - <span data-ttu-id="8e4ed-109">Optional.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-109">Optional.</span></span> <span data-ttu-id="8e4ed-110">Ein **String** -Wert, der eine URL, die Entität kopiert werden soll (beispielsweise eine Datei oder ein Verzeichnis) enthält.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="8e4ed-111">Wenn *Source* ausgelassen wird oder eine leere Zeichenfolge angibt, wird die Datei oder das Verzeichnis vom aktuellen [Datensatz](record-object-ado.md) dargestellt kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="8e4ed-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="8e4ed-112">*Destination*</span></span>

  - <span data-ttu-id="8e4ed-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-113">Optional.</span></span> <span data-ttu-id="8e4ed-114">Ein **String** -Wert, der eine URL des Speicherorts, in dem *Quelle* kopiert werden, enthält.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="8e4ed-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="8e4ed-115">*UserName*</span></span>

  - <span data-ttu-id="8e4ed-p103">Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="8e4ed-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="8e4ed-118">*Password*</span></span>

  - <span data-ttu-id="8e4ed-p104">Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="8e4ed-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="8e4ed-121">*Options*</span></span>

  - <span data-ttu-id="8e4ed-p105">Optional. Ein [CopyRecordOptionsEnum](copyrecordoptionsenum.md)-Wert, der den Standardwert **adCopyUnspecified** besitzt. Gibt das Verhalten dieser Methode an.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="8e4ed-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="8e4ed-125">*Async*</span></span>

  - <span data-ttu-id="8e4ed-p106">Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass dieser Vorgang asynchron sein soll.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e4ed-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e4ed-128">Return value</span></span>

<span data-ttu-id="8e4ed-p107">Ein **String**-Wert, der in der Regel den Wert für *Destination* zurückgibt. Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4ed-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e4ed-131">Remarks</span></span>

<span data-ttu-id="8e4ed-132">Die Werte der *Quell-* und *Zielserver* dürfen nicht identisch sein; andernfalls tritt ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-132">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="8e4ed-133">Mindestens einer der Server-, Pfad- oder Ressourcennamen muss unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-133">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="8e4ed-p109">Wenn **adCopyNonRecursive** nicht angegeben ist, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) von *Source* rekursiv kopiert. Bei einem rekursiven Vorgang darf es sich bei der *Destination* nicht um ein Unterverzeichnis von *Source* handeln, andernfalls kann der Vorgang nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="8e4ed-136">Diese Methode schlägt fehl, wenn das *Ziel* eine vorhandene Entität (beispielsweise eine Datei oder ein Verzeichnis) identifiziert, es sei denn, **AdCopyOverWrite** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-136">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="8e4ed-137">[!WICHTIG] Verwenden Sie die Option **adCopyOverWrite** nur nach sorgfältiger Überlegung.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-137">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="8e4ed-138">Beispielsweise wird durch das Angeben dieser Option beim Kopieren einer Datei in ein Verzeichnis das Verzeichnis wird *Löschen* und Ersetzen Sie ihn mit der Datei.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-138">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>




> [!NOTE]
> <span data-ttu-id="8e4ed-139">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-139">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="8e4ed-140">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="8e4ed-140">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


