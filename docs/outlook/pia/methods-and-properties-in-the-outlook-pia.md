---
title: Methoden und Eigenschaften in der Outlook-PIA
TOCTitle: Methods and properties in the Outlook PIA
ms:assetid: ec7742de-ead6-41dd-90a3-1280fdf09d54
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612528(v=office.15)
ms:contentKeyID: 55119780
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b1bee381e6f53b4d8a63e69a920e4f4a6e9e302a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407373"
---
# <a name="methods-and-properties-in-the-outlook-pia"></a><span data-ttu-id="f614f-102">Methoden und Eigenschaften in der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="f614f-102">Methods and Properties in the Outlook PIA</span></span>

<span data-ttu-id="f614f-103">In diesem Thema wird beschrieben, wie mithilfe der Outlook Primary Interop Assembly (PIA) auf Methoden und Eigenschaften eines Objekts in verwaltetem Code zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="f614f-103">This topic describes how to access methods and properties of an object in managed code by using the Outlook Primary Interop Assembly (PIA).</span></span>

## <a name="where-helper-objects-come-from"></a><span data-ttu-id="f614f-104">Ursprung von Hilfsobjekten</span><span class="sxs-lookup"><span data-stu-id="f614f-104">Where Helper Objects Come From</span></span>

<span data-ttu-id="f614f-p101">Zum Erstellen der Outlook PIA verwendet Outlook den Typbibliothekimporter (Type Library Importer, TLBIMP) von .NET Framework, um Typdefinitionen in der COM-Typbibliothek in entsprechende Definitionen in einer Common Language Runtime-Assembly (CLR) zu konvertieren. In COM stellt ein Objekt eine Co-Klasse dar, die Folgendes umfasst:</span><span class="sxs-lookup"><span data-stu-id="f614f-p101">To create the Outlook PIA, Outlook uses the Type Library Importer (TLBIMP) in the .NET Framework to convert type definitions in the COM type library into equivalent definitions in a common language runtime (CLR) assembly. In COM, an object is actually a coclass that consists of the following:</span></span>

- <span data-ttu-id="f614f-107">Die primäre Schnittstelle (z. B. die [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\))-Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="f614f-107">The primary interface (for example, the _FormRegion interface).</span></span>

- <span data-ttu-id="f614f-108">Die Ereignisschnittstelle (z. B. die [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))-Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="f614f-108">The event interface (for example, the [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\)) interface).</span></span>

<span data-ttu-id="f614f-109">TLBIMP importiert die primäre Schnittstelle und die Ereignisschnittstelle für jedes Objekt und erstellt eine Reihe von Schnittstellen, Delegaten und Klassen, zu denen die folgenden gehören:</span><span class="sxs-lookup"><span data-stu-id="f614f-109">TLBIMP imports the primary interface and the event interface for each object and creates a number of interfaces, delegates, and classes, among which are the following:</span></span>

- <span data-ttu-id="f614f-110">Die .NET-Ereignisschnittstelle (z. B. die [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\))-Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="f614f-110">The .NET event interface (for example, the FormRegionEvents_Event interface).</span></span>

- <span data-ttu-id="f614f-111">Die .NET-Klasse (z. B. die [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))-Klasse).</span><span class="sxs-lookup"><span data-stu-id="f614f-111">The .NET class (for example, the [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\)) class).</span></span>

- <span data-ttu-id="f614f-112">Die .NET-Schnittstelle (z. B. die [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\))-Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="f614f-112">The .NET interface (for example, the [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) interface).</span></span>

## <a name="what-the-helper-objects-are-for"></a><span data-ttu-id="f614f-113">Zweck der Hilfsobjekte</span><span class="sxs-lookup"><span data-stu-id="f614f-113">What the Helper Objects Are For</span></span>

<span data-ttu-id="f614f-114">Bei weiterer Verwendung des **FormRegion**-Objekts als Beispiel prüft die folgende Liste, was die einzelnen Schnittstellen und zuvor aufgeführten Klassen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f614f-114">Continuing to use the **FormRegion** object as an example, the following list examines what each interface and class listed earlier contains.</span></span>

- <span data-ttu-id="f614f-115">Die \_FormRegion-Schnittstelle definiert alle Methoden und Eigenschaften von FormRegion.</span><span class="sxs-lookup"><span data-stu-id="f614f-115">The _FormRegion interface defines all the methods and properties of FormRegion.</span></span> <span data-ttu-id="f614f-116">In der Regel wird diese Schnittstelle nicht im Code verwendet, mit Ausnahme einer nachfolgend besprochenen Bedingung.</span><span class="sxs-lookup"><span data-stu-id="f614f-116">Typically you do not use this interface in code, except for a condition discussed below.</span></span>

- <span data-ttu-id="f614f-117">Die **FormRegionEvents**-Schnittstelle definiert Methoden, die Ereignissen von FormRegion zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f614f-117">The FormRegionEvents interface defines methods mapping to events of FormRegion.</span></span> <span data-ttu-id="f614f-118">Verwenden Sie diese Schnittstelle nicht im Code.</span><span class="sxs-lookup"><span data-stu-id="f614f-118">You do not use this interface in code.</span></span>

- <span data-ttu-id="f614f-119">TLBIMP verarbeitet die **FormRegionEvents**-Schnittstelle weiter, um die **FormRegionEvents**\_Event-Schnittstelle zu erstellen, die alle Ereignisse von FormRegion definiert.</span><span class="sxs-lookup"><span data-stu-id="f614f-119">TLBIMP further processes the **FormRegionEvents** interface to create the **FormRegionEvents_Event** interface that defines all the events of \_.</span></span> <span data-ttu-id="f614f-120">In der Regel wird diese Schnittstelle nicht im Code verwendet, mit Ausnahme einer nachfolgend besprochenen Bedingung.</span><span class="sxs-lookup"><span data-stu-id="f614f-120">Typically you do not use this interface in code, except for a condition discussed below.</span></span>

- <span data-ttu-id="f614f-p105">Die FormRegionClass-Klasse definiert alle Methoden-, Eigenschaften- und Ereignismember von FormRegion. Dieser Klasse wird die FormRegion-Schnittstelle im Hintergrund zugeordnet, sodass Sie Code schreiben können, um eine Instanz der FormRegion-Schnittstelle zu erstellen. Sie verwenden die Schnittstelle jedoch nicht direkt in Code.</span><span class="sxs-lookup"><span data-stu-id="f614f-p105">The FormRegionClass class defines all the method, property, and event members of FormRegion. This is the class that the FormRegion interface is attributed to associate with behind the scenes so that you can write code to create an instance of the FormRegion interface. However, you do not use this interface directly in code.</span></span>

- <span data-ttu-id="f614f-124">Die FormRegion-Schnittstelle erbt die \__FormRegion-Schnittstelle und die **FormRegionEvents**\_-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f614f-124">The \_ interface inherits the **_FormRegion** interface and the \_ interface.</span></span> <span data-ttu-id="f614f-125">Abbildung 1 zeigt die Vererbungsbeziehung.</span><span class="sxs-lookup"><span data-stu-id="f614f-125">Figure 1 illustrates this inheritance relationship.</span></span>
    
  <span data-ttu-id="f614f-126">**Abbildung 1. Die FormRegion-Schnittstelle erbt Methoden und Eigenschaften von der \_FormRegion-Schnittstelle und Ereignisse von der FormRegionEvents\_Event-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f614f-126">Figure 1. The FormRegion interface inherits methods and properties from the _FormRegion interface, and inherits events from the FormRegionEvents_Event interface</span></span>

  ![Die FormRegion-Schnittstelle erbt Methoden und Eigenschaften von der _FormRegion-Schnittstelle und Ereignisse von der FormRegionEvents_Event-Schnittstelle](media/pia-form-region-interface.gif)
    
  <span data-ttu-id="f614f-128">In der Regel ist FormRegion die einzige Schnittstelle, die Sie in verwaltetem Code verwenden, um auf das Objekt und die Methoden-, Eigenschaften- und Ereignismember des **FormRegion**-Objekts zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f614f-128">Typically, **FormRegion** is the one interface you use in managed code to access the object and the method, property, and event members of the FormRegion object.</span></span>

<span data-ttu-id="f614f-p107">Unter Verwendung des **Application**-Objekts als weiteres Beispiel greifen Sie auf das **Application**-Objekt, Methoden, Eigenschaften und Ereignisse über die [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) -Schnittstelle zu. Es gibt jedoch drei Ausnahmen, bei denen Sie eine andere Schnittstelle verwenden müssen oder abhängig von der Sprache verwenden möchten:</span><span class="sxs-lookup"><span data-stu-id="f614f-p107">Using the **Application** object as another example, you access the **Application** object, methods, properties, and events through the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) interface. There are however three exceptions where you must use a different interface, or depending on the language, you would want to use a different interface:</span></span>

- <span data-ttu-id="f614f-131">Wenn Sie auf eine Methode zugreifen, die denselben Namen wie ein Ereignis aufweist, ist es ratsam, zur primären Schnittstelle zu wechseln, um die Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f614f-131">When you access a method that shares the same name as an event, a good practice is to cast to the primary interface to call the method.</span></span> <span data-ttu-id="f614f-132">Das **Application**-Objekt verfügt beispielsweise über eine [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\))-Methode und ein [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\))-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f614f-132">For example, the **Application** object has a [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) method and a [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)) event.</span></span> <span data-ttu-id="f614f-133">In Visual Basic .NET können Sie über die Anwendungsschnittstelle auf die Quit-Methode zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f614f-133">In Visual Basic .NET, you can access the Quit method through the Application interface.</span></span> <span data-ttu-id="f614f-134">In C\# können Sie eine Compilerwarnung vermeiden, indem Sie für die Quit-Methode zur primären Schnittstelle wechseln, wie im folgenden Codebeispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="f614f-134">In C#, you can avoid a compiler warning by casting the \# method to the primary interface, as shown in the following code sample:</span></span>
    
   ```csharp
      void DemoApp()
      {
          Outlook.Application myApp = new Outlook.Application();
          // Other application code here
          ((Outlook._Application)myApp).Quit();
      }
   ```

- <span data-ttu-id="f614f-135">Wenn Sie auf ein Ereignis zugreifen, das denselben Namen wie eine Methode dieses Objekts aufweist, müssen Sie zur entsprechenden Ereignisschnittstelle wechseln, um das Ereignis aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f614f-135">When you access an event that shares the same name as a method of that object, you must cast to the appropriate event interface to connect to the event.</span></span> <span data-ttu-id="f614f-136">Ähnlich zum vorherigen Beispiel müssen Sie zum Aufrufen des Quit-Ereignisses zur [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))-Schnittstelle wechseln.</span><span class="sxs-lookup"><span data-stu-id="f614f-136">Similar to the example above, to connect to the Quit event, you cast to the ApplicationEvents_11_Event interface.</span></span>

- <span data-ttu-id="f614f-137">Wenn Sie eine frühere Version eines Ereignisses aufrufen, das anschließend in einer späteren Version von Outlook erweitert wurde, müssen Sie die Version des Ereignisses in der früheren Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f614f-137">When you connect to an earlier version of an event that has been subsequently extended in a later version of Outlook, you must connect to the version of the event in the earlier interface.</span></span> <span data-ttu-id="f614f-138">Wenn Sie beispielsweise statt der neuesten Version die Version des Quit-Ereignisses für das **Application**-Objekt aufrufen möchten, die für Outlook 2002 implementiert wurde, rufen Sie das [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\))-Ereignis auf, das in der [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\))-Schnittstelle definiert ist, statt des Quit-Ereignisses, das in der ApplicationEvents\_11\_Event-Schnittstelle definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f614f-138">For example, if you want to connect to the version of the Quit event for the Application object implemented for Outlook 2002 instead of the latest version, connect to the Quit event defined in the ApplicationEvents_10_Event interface, instead of the Quit event defined in the ApplicationEvents_11_Event interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="f614f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f614f-139">See also</span></span>

- [<span data-ttu-id="f614f-140">Zuordnen der Outlook-PIA zum Objektmodell</span><span class="sxs-lookup"><span data-stu-id="f614f-140">Relating the Outlook PIA with the Object Model</span></span>](relating-the-outlook-pia-with-the-object-model.md)
- [<span data-ttu-id="f614f-141">Objekte in der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="f614f-141">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)
- [<span data-ttu-id="f614f-142">Ereignisse in der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="f614f-142">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)

