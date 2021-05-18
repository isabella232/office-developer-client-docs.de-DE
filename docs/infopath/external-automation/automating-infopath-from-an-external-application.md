---
title: Automatisieren von InfoPath aus einer externen Anwendung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath bietet Anwendungsautomatisierung von Code, der mithilfe von COM und Skript mithilfe von Methoden des Application-Objekts und der XDocuments-Auflistung geschrieben wurde.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412667"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="d7955-103">Automatisieren von InfoPath aus einer externen Anwendung</span><span class="sxs-lookup"><span data-stu-id="d7955-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="d7955-104">Microsoft InfoPath bietet Anwendungsautomatisierung von Code, der mithilfe von COM und Skript mithilfe von Methoden des **Application-Objekts** und der **XDocuments-Auflistung geschrieben** wurde.</span><span class="sxs-lookup"><span data-stu-id="d7955-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="d7955-105">Übersicht über die Anwendungs- und XDocument-Objekte</span><span class="sxs-lookup"><span data-stu-id="d7955-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="d7955-106">Das **Application-Objekt** enthält die folgenden Methoden, die für die Automatisierung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="d7955-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="d7955-107">**Methode**</span><span class="sxs-lookup"><span data-stu-id="d7955-107">**Method**</span></span>|<span data-ttu-id="d7955-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7955-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7955-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="d7955-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="d7955-110">Untersucht den im Cache und aktualisiert ihn bei Bedarf vom veröffentlichten Speicherort der Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="d7955-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="d7955-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="d7955-111">**Quit**</span></span> <br/> |<span data-ttu-id="d7955-112">Beendet die Microsoft Office InfoPath-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d7955-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="d7955-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="d7955-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="d7955-114">Installiert die angegebene Microsoft Office InfoPath-Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="d7955-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="d7955-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="d7955-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="d7955-116">Deinstalliert die angegebene Microsoft Office InfoPath-Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="d7955-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="d7955-117">Die **XDocuments-Auflistung** enthält die folgenden Methoden, die für die externe Automatisierung verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="d7955-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="d7955-118">**Methode**</span><span class="sxs-lookup"><span data-stu-id="d7955-118">**Method**</span></span>|<span data-ttu-id="d7955-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7955-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7955-120">**Close**-Methode</span><span class="sxs-lookup"><span data-stu-id="d7955-120">**Close** method</span></span>  <br/> |<span data-ttu-id="d7955-121">Schließt das angegebene Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="d7955-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="d7955-122">**Neue** Methode</span><span class="sxs-lookup"><span data-stu-id="d7955-122">**New** method</span></span>  <br/> |<span data-ttu-id="d7955-123">Erstellt ein neues Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="d7955-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="d7955-124">**NewFromSolution-Methode**</span><span class="sxs-lookup"><span data-stu-id="d7955-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="d7955-125">Erstellt ein neues Microsoft Office InfoPath-Formular basierend auf der angegebenen Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="d7955-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="d7955-126">**NewFromSolutionWithData-Methode**</span><span class="sxs-lookup"><span data-stu-id="d7955-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="d7955-127">Erstellt ein neues Microsoft Office InfoPath-Formular mithilfe der angegebenen XML-Daten und Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="d7955-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="d7955-128">**Open-Methode**</span><span class="sxs-lookup"><span data-stu-id="d7955-128">**Open** method</span></span>  <br/> |<span data-ttu-id="d7955-129">Öffnet das angegebene Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="d7955-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="d7955-130">Um das **Application-Objekt** aus einer externen Anwendung zu verwenden, verwenden Sie die **CreateObject-Funktion** mit der ProgID der InfoPath-Anwendung ("InfoPath.Application"), um eine Objektvariable zu erstellen, die die InfoPath-Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d7955-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="d7955-131">Anschließend können Sie die **XDocuments-Eigenschaft** verwenden, um auf die **XDocuments-Auflistung** zu zugreifen und die Methoden zum Öffnen oder Erstellen eines InfoPath-Formulars zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7955-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="d7955-132">Im folgenden Beispiel wird die Erstellung eines Verweises auf das **Application-Objekt** mithilfe der Programmiersprache Microsoft Visual Basic 6.0 oder Visual Basic for Applications (VBA) veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="d7955-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="d7955-133">Da die **CreateObject-Funktion** eine Objektvariable mit später Bindung erstellt, steht der automatische Abschluss der Anweisung im Editor Visual Basic zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d7955-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="d7955-134">Informationen zur richtigen Aufrufsyntax finden Sie in den Links in den vorherigen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d7955-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

