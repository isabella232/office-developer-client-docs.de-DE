---
title: ADO für Windows Foundation Classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706238"
---
# <a name="adowfc"></a><span data-ttu-id="a0a9d-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a0a9d-102">ADO/WFC</span></span>


<span data-ttu-id="a0a9d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0a9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0a9d-p101">ADO für Windows Foundation Classes (ADO/WFC) basiert auf dem ADO-Ereignismodell und stellt eine vereinfachte Anwendungsprogrammierschnittstelle dar. ADO/WFC fängt im Allgemeinen ADO-Ereignisse ab, konsolidiert die Ereignisparameter in einer einzelnen Ereignisklasse und ruft dann den Ereignishandler auf.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p101">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface. In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="a0a9d-106">**So verwenden Sie ADO-Ereignisse in ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="a0a9d-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="a0a9d-p102">Definieren Sie Ihren eigenen Ereignishandler, um ein Ereignis zu verarbeiten. Wenn Sie z. B. das **ConnectComplete** -Ereignis in der **ConnectionEvent** -Familie verarbeiten möchten, können Sie folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p102">Define your own event handler to process an event. For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="a0a9d-p103">Definieren Sie ein Handlerobjekt, um Ihren Ereignishandler darzustellen. Das Handlerobjekt sollte vom Datentyp **ConnectEventHandler** für ein Ereignis vom Typ **ConnectionEvent** sein, oder vom Datentyp **RecordsetEventHandler** für ein Ereignis vom Typ **RecordsetEvent**. Erstellen Sie z. B. den folgenden Code für den **ConnectComplete** -Ereignishandler:</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p103">Define a handler object to represent your event handler. The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**. For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="a0a9d-p104">Das erste Argument des **ConnectionEventHandler** -Konstruktors ist ein Verweis auf die Klasse, die den im zweiten Argument genannten Ereignishandler enthält. Darüber hinaus unterstützt der Microsoft Visual J++ Compiler eine entsprechende Syntax:</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p104">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="a0a9d-p105">Das erste Argument des **ConnectionEventHandler** -Konstruktors ist ein Verweis auf die Klasse, die den im zweiten Argument genannten Ereignishandler enthält. Darüber hinaus unterstützt der Microsoft Visual J++ Compiler eine entsprechende Syntax:</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p105">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="a0a9d-116">

Das einzelne Argument ist ein Verweis auf die gewünschte Klasse (\*\*this\*\*) und die gewünschte Methode innerhalb der Klasse (\*\*onConnectComplete**).
</span><span class="sxs-lookup"><span data-stu-id="a0a9d-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="a0a9d-117">Fügen Sie eine Liste der Handler zum Verarbeiten von einer bestimmten Art des Ereignisses festgelegte Ihre Ereignishandler hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="a0a9d-118">Verwenden Sie die Methode mit einem Namen wie \**AddOn \*\*\* EventName*(*Handler*).</span><span class="sxs-lookup"><span data-stu-id="a0a9d-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="a0a9d-p107">ADO/WFC implementiert intern alle ADO-Ereignishandler. Deshalb wird ein Ereignis, das durch einen **Connection** - oder **Recordset** -Vorgang verursacht wird, von einem ADO/WFC-Ereignishandler abgefangen. Der ADO/WFC-Ereignishandler übergibt **ConnectionEvent** -Parameter von ADO in einer Instanz der **ConnectionEvent** -Klasse von ADO/WFC oder **RecordsetEvent** -Parameter von ADO in einer Instanz der **RecordsetEvent** -Klasse von ADO/WFC. Diese ADO/WFC-Klassen konsolidieren die ADO-Ereignisparameter. Das heißt, jede ADO/WFC-Klasse enthält ein Datenelement für jeden eindeutigen Parameter in allen **ConnectionEvent** - oder **RecordsetEvent** -Methoden von ADO.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p107">ADO/WFC internally implements all the ADO event handlers. Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler. The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class. These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="a0a9d-p108">ADO/WFC ruft dann den Ereignishandler mit dem ADO/WFC-Ereignisobjekt auf. Beispielsweise weist Ihr **onConnectComplete** -Handler eine Signatur wie die folgende auf:</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p108">ADO/WFC then calls your event handler with the ADO/WFC event object. For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="a0a9d-125">Das erste Argument ist der Typ des Objekts, das das Ereignis ([Verbindung](connection-object-ado.md) oder [Recordset](recordset-object-ado.md)) gesendet, und das zweite Argument ist das ADO/WFC-Ereignisobjekt (**ConnectionEvent** oder **RecordsetEvent**).</span><span class="sxs-lookup"><span data-stu-id="a0a9d-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="a0a9d-126">Die Signatur des Ereignishandlers ist einfacher als ein ADO-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="a0a9d-127">Sie müssen jedoch dennoch das ADO-Ereignismodell kennen, um zu wissen, welche Parameter für ein Ereignis gelten und wie reagiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="a0a9d-p110">Wechseln Sie vom Ereignishandler zurück zum ADO/WFC-Handler für das ADO-Ereignis. ADO/WFC kopiert die entsprechenden Datenelemente für das ADO/WFC-Ereignis zurück in die ADO-Ereignisparameter, und anschließend wird wieder der ADO-Ereignishandler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-p110">Return from your event handler to the ADO/WFC handler for the ADO event. ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="a0a9d-130">Wenn Sie nach Abschluss des Vorgangs sind verarbeiten, entfernen Sie den Handler aus der Liste der ADO/WFC-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="a0a9d-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="a0a9d-131">Verwenden Sie die Methode mit einem Namen wie \**RemoveOn \*\*\* EventName*(*Handler*).</span><span class="sxs-lookup"><span data-stu-id="a0a9d-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

