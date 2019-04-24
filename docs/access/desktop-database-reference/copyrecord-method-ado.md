---
title: CopyRecord-Methode (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295527"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="ed158-102">CopyRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ed158-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="ed158-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed158-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed158-104">Kopiert eine durch einen **Record** dargestellte Entität an einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ed158-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed158-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed158-105">Syntax</span></span>

<span data-ttu-id="ed158-106">*Record*. CopyRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="ed158-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ed158-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed158-107">Parameters</span></span>

|<span data-ttu-id="ed158-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed158-108">Parameter</span></span>|<span data-ttu-id="ed158-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed158-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ed158-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="ed158-110">*Source*</span></span> |<span data-ttu-id="ed158-p101">Optional. Ein **String**-Wert mit einer URL, die die zu kopierende Entität (z. B. eine Datei oder ein Verzeichnis) angibt. Wenn *Source* nicht angegeben ist oder eine leere Zeichenfolge angibt, wird die bzw. das durch den aktuellen [Record](record-object-ado.md) dargestellte Datei oder Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="ed158-p101">Optional. A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory). If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="ed158-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="ed158-114">*Destination*</span></span> |<span data-ttu-id="ed158-115">Optional.</span><span class="sxs-lookup"><span data-stu-id="ed158-115">Optional.</span></span> <span data-ttu-id="ed158-116">Ein **String**-Wert mit einer URL, die den Speicherort angibt, an den die *Source* kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed158-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="ed158-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="ed158-117">*UserName*</span></span> |<span data-ttu-id="ed158-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="ed158-118">Optional.</span></span> <span data-ttu-id="ed158-119">Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.</span><span class="sxs-lookup"><span data-stu-id="ed158-119">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="ed158-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="ed158-120">*Password*</span></span> |<span data-ttu-id="ed158-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="ed158-121">Optional.</span></span> <span data-ttu-id="ed158-122">Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.</span><span class="sxs-lookup"><span data-stu-id="ed158-122">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="ed158-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="ed158-123">*Options*</span></span> |<span data-ttu-id="ed158-p105">Optional. Ein [CopyRecordOptionsEnum](copyrecordoptionsenum.md)-Wert, der den Standardwert **adCopyUnspecified** besitzt. Gibt das Verhalten dieser Methode an.</span><span class="sxs-lookup"><span data-stu-id="ed158-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="ed158-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="ed158-127">*Async*</span></span> |<span data-ttu-id="ed158-p106">Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass dieser Vorgang asynchron sein soll.</span><span class="sxs-lookup"><span data-stu-id="ed158-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="ed158-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed158-130">Return value</span></span>

<span data-ttu-id="ed158-131">Ein **String**-Wert, der in der Regel den Wert für *Destination* zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ed158-131">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="ed158-132">Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="ed158-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed158-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed158-133">Remarks</span></span>

<span data-ttu-id="ed158-p108">Die Werte für *Source* und *Destination* dürfen nicht identisch sein, andernfalls tritt ein Laufzeitfehler auf. Mindestens einer der Server-, Pfad- oder Ressourcennamen muss unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="ed158-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="ed158-p109">Wenn **adCopyNonRecursive** nicht angegeben ist, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) von *Source* rekursiv kopiert. Bei einem rekursiven Vorgang darf es sich bei der *Destination* nicht um ein Unterverzeichnis von *Source* handeln, andernfalls kann der Vorgang nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ed158-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="ed158-138">Diese Methode schlägt fehl, wenn die *Destination* eine vorhandene Entität (z. B. eine Datei oder ein Verzeichnis) angibt und **adCopyOverWrite** nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ed158-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed158-p110">Verwenden Sie die Option **adCopyOverWrite** nur nach sorgfältiger Überlegung. Wenn Sie diese Option beispielsweise beim Kopieren einer Datei in ein Verzeichnis angeben, wird das Verzeichnis *gelöscht* und durch die Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ed158-p110">Use the **adCopyOverWrite** option judiciously. For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="ed158-141">Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ed158-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ed158-142">Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="ed158-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


