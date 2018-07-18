---
title: Automatisieren von InfoPath aus einer externen Anwendung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath bietet Anwendung Automatisierung von Code, COM und Skript mithilfe der Methoden des Application-Objekts und der XDocuments-Auflistung verwendet.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790626"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="e7e02-103">Automatisieren von InfoPath aus einer externen Anwendung</span><span class="sxs-lookup"><span data-stu-id="e7e02-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="e7e02-104">Microsoft InfoPath bietet Anwendung Automatisierung von Code, COM und Skript mithilfe der Methoden des **Application** -Objekts und der **XDocuments** -Auflistung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7e02-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="e7e02-105">Übersicht über die Anwendung und der XDocument-Objekte</span><span class="sxs-lookup"><span data-stu-id="e7e02-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="e7e02-106">Das **Application** -Objekt enthält die folgenden Methoden, die für die Automatisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="e7e02-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="e7e02-107">**Methode**</span><span class="sxs-lookup"><span data-stu-id="e7e02-107">**Method**</span></span>|<span data-ttu-id="e7e02-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7e02-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7e02-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="e7e02-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="e7e02-110">Untersucht die im Cache und, falls erforderlich, wird von den Veröffentlichungsort der Formularvorlage aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e7e02-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="e7e02-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="e7e02-111">**Quit**</span></span> <br/> |<span data-ttu-id="e7e02-112">Beendet die Anwendung Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e7e02-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="e7e02-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="e7e02-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="e7e02-114">Installiert die angegebene Microsoft Office InfoPath-Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="e7e02-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="e7e02-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="e7e02-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="e7e02-116">Deinstalliert die angegebene Microsoft Office InfoPath-Formularvorlage an.</span><span class="sxs-lookup"><span data-stu-id="e7e02-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="e7e02-117">Die **XDocuments** -Auflistung enthält die folgenden Methoden, die für die externe Automatisierung verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="e7e02-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="e7e02-118">**Methode**</span><span class="sxs-lookup"><span data-stu-id="e7e02-118">**Method**</span></span>|<span data-ttu-id="e7e02-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7e02-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7e02-120">**Close**-Methode</span><span class="sxs-lookup"><span data-stu-id="e7e02-120">**Close** method</span></span>  <br/> |<span data-ttu-id="e7e02-121">Schließt das angegebene Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="e7e02-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="e7e02-122">**New** -Methode</span><span class="sxs-lookup"><span data-stu-id="e7e02-122">**New** method</span></span>  <br/> |<span data-ttu-id="e7e02-123">Erstellt ein neues Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="e7e02-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="e7e02-124">**NewFromSolution** -Methode</span><span class="sxs-lookup"><span data-stu-id="e7e02-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="e7e02-125">Erstellt ein neues Microsoft Office InfoPath-Formular basierend auf der angegebenen Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="e7e02-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="e7e02-126">**NewFromSolutionWithData** -Methode</span><span class="sxs-lookup"><span data-stu-id="e7e02-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="e7e02-127">Erstellt ein neues Microsoft Office InfoPath-Formular mithilfe der angegebenen XML-Daten und der Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="e7e02-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="e7e02-128">**Open** -Methode</span><span class="sxs-lookup"><span data-stu-id="e7e02-128">**Open** method</span></span>  <br/> |<span data-ttu-id="e7e02-129">Öffnet das angegebene Microsoft Office InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="e7e02-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="e7e02-130">Um das **Application** -Objekt aus einer externen Anwendung verwenden möchten, verwenden Sie die **CreateObject** -Funktion mit die ProgID des InfoPath-Anwendung ("InfoPath.Application") um eine Objektvariable zu erstellen, die InfoPath-Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7e02-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="e7e02-131">Sie können die **XDocuments** -Eigenschaft klicken Sie dann auf die **XDocuments** -Auflistung zuzugreifen und dessen Methoden zum Öffnen oder erstellen Sie ein InfoPath-Formular verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7e02-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="e7e02-132">Das folgende Beispiel veranschaulicht das Erstellen eines Verweises auf das **Application** -Objekt mithilfe der Microsoft Visual Basic 6.0 oder Visual Basic für Applikationen (VBA) Programmiersprache:</span><span class="sxs-lookup"><span data-stu-id="e7e02-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="e7e02-133">Da eine Objektvariable späten Bindung mithilfe die **CreateObject** -Funktion erstellt wird, wird Abschluss der automatischen Anweisung in Visual Basic-Editor nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7e02-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="e7e02-134">Verweisen Sie auf die Links in den vorherigen Tabellen Informationen zur richtigen Aufrufsyntax.</span><span class="sxs-lookup"><span data-stu-id="e7e02-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

