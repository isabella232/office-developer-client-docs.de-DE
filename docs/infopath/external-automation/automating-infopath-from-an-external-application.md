---
title: Automatisieren von InfoPath aus einer externen Anwendung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath stellt mithilfe der Methoden des Application-Objekts und der XDocuments-Auflistung die Anwendungsautomatisierung von Code bereit, der mithilfe von COM und Skripts geschrieben wurde.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412667"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="a8479-103">Automatisieren von InfoPath aus einer externen Anwendung</span><span class="sxs-lookup"><span data-stu-id="a8479-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="a8479-104">Microsoft InfoPath stellt mithilfe der Methoden des **Application** -Objekts und der XDocuments-Auflistung die Anwendungsautomatisierung von Code \*\*\*\* bereit, der mithilfe von com und Skripts geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="a8479-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="a8479-105">Übersicht über die Objekte Application und XDocument</span><span class="sxs-lookup"><span data-stu-id="a8479-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="a8479-106">Das **Application** -Objekt enthält die folgenden Methoden für die Automatisierung:</span><span class="sxs-lookup"><span data-stu-id="a8479-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="a8479-107">**Methode**</span><span class="sxs-lookup"><span data-stu-id="a8479-107">**Method**</span></span>|<span data-ttu-id="a8479-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8479-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8479-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="a8479-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="a8479-110">Untersucht die im Cache und aktualisiert Sie, falls erforderlich, vom veröffentlichten Speicherort der Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="a8479-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="a8479-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="a8479-111">**Quit**</span></span> <br/> |<span data-ttu-id="a8479-112">Beendet die Microsoft Office InfoPath-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a8479-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="a8479-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="a8479-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="a8479-114">Installiert die angegebene Microsoft Office InfoPath-Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="a8479-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="a8479-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="a8479-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="a8479-116">Deinstalliert die angegebene Microsoft Office InfoPath-Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="a8479-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="a8479-117">Die **XDocuments** -Auflistung enthält die folgenden Methoden, die für die externe Automatisierung verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="a8479-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="a8479-118">**Methode**</span><span class="sxs-lookup"><span data-stu-id="a8479-118">**Method**</span></span>|<span data-ttu-id="a8479-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8479-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8479-120">**Close**-Methode</span><span class="sxs-lookup"><span data-stu-id="a8479-120">**Close** method</span></span>  <br/> |<span data-ttu-id="a8479-121">Schließt das angegebene Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="a8479-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="a8479-122">**Neue** Methode</span><span class="sxs-lookup"><span data-stu-id="a8479-122">**New** method</span></span>  <br/> |<span data-ttu-id="a8479-123">Erstellt ein neues Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="a8479-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="a8479-124">**NewFromSolution** -Methode</span><span class="sxs-lookup"><span data-stu-id="a8479-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="a8479-125">Erstellt ein neues Microsoft Office InfoPath-Formular basierend auf der angegebenen Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="a8479-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="a8479-126">**NewFromSolutionWithData** -Methode</span><span class="sxs-lookup"><span data-stu-id="a8479-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="a8479-127">Erstellt mithilfe der angegebenen XML-Daten und Formularvorlage ein neues Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="a8479-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="a8479-128">**Open** -Methode</span><span class="sxs-lookup"><span data-stu-id="a8479-128">**Open** method</span></span>  <br/> |<span data-ttu-id="a8479-129">Öffnet das angegebene Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="a8479-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="a8479-130">Um das **Application** -Objekt aus einer externen Anwendung zu verwenden, verwenden Sie die **CreateObject** -Funktion mit der ProgID der InfoPath-Anwendung ("InfoPath. Application"), um eine Objektvariable zu erstellen, die die InfoPath-Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8479-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="a8479-131">Anschließend können Sie die **XDocuments** -Eigenschaft verwenden, um auf die **XDocuments** -Auflistung zuzugreifen und ihre Methoden zum Öffnen oder Erstellen eines InfoPath-Formulars zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8479-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="a8479-132">Das folgende Beispiel veranschaulicht die Erstellung eines Verweises auf das **Application** -Objekt, das die Programmiersprache Microsoft visual Basic 6,0 oder Visual Basic für Applikationen (VBA) verwendet:</span><span class="sxs-lookup"><span data-stu-id="a8479-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="a8479-133">Da die **CreateObject** -Funktion eine Objektvariable mithilfe der späten Bindung erstellt, ist die automatische Anweisungsvervollständigung im Visual Basic-Editor nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a8479-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="a8479-134">Informationen zur richtigen Aufrufsyntax finden Sie in den Links in den obigen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="a8479-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

