---
title: ADO für Windows Foundation-Klassen (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0be678323e24179c0362f119ecc4dc11bb85b0ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559220"
---
# <a name="adowfc"></a>ADO/WFC


**Gilt für**: Access 2013, Office 2013

ADO für Windows Foundation Classes (ADO/WFC) basiert auf dem ADO-Ereignismodell und stellt eine vereinfachte Anwendungsprogrammierschnittstelle dar. ADO/WFC fängt im Allgemeinen ADO-Ereignisse ab, konsolidiert die Ereignisparameter in einer einzelnen Ereignisklasse und ruft dann den Ereignishandler auf.

**So verwenden Sie ADO-Ereignisse in ADO/WFC**

1.  Definieren Sie Ihren eigenen Ereignishandler, um ein Ereignis zu verarbeiten. Wenn Sie z. B. das **ConnectComplete** -Ereignis in der **ConnectionEvent** -Familie verarbeiten möchten, können Sie folgenden Code verwenden:
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Definieren Sie ein Handlerobjekt, um Ihren Ereignishandler darzustellen. Das Handlerobjekt sollte vom Datentyp **ConnectEventHandler** für ein Ereignis vom Typ **ConnectionEvent** sein, oder vom Datentyp **RecordsetEventHandler** für ein Ereignis vom Typ **RecordsetEvent**. Erstellen Sie z. B. den folgenden Code für den **ConnectComplete** -Ereignishandler:
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    Das erste Argument des **ConnectionEventHandler** -Konstruktors ist ein Verweis auf die Klasse, die den im zweiten Argument genannten Ereignishandler enthält. Darüber hinaus unterstützt der Microsoft Visual J++ Compiler eine entsprechende Syntax:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Das erste Argument des **ConnectionEventHandler** -Konstruktors ist ein Verweis auf die Klasse, die den im zweiten Argument genannten Ereignishandler enthält. Darüber hinaus unterstützt der Microsoft Visual J++ Compiler eine entsprechende Syntax:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Das einzelne Argument ist ein Verweis auf die gewünschte Klasse (**this**) und die gewünschte Methode innerhalb der Klasse (**onConnectComplete**).

3.  Fügen Sie den Ereignishandler einer Liste von Handlern hinzu, die für die Verarbeitung eines bestimmten Ereignistyps vorgesehen sind. Verwenden Sie die Methode mit einem Namen wie z. B. **addOn**_EventName_(*handler*).

4.  ADO/WFC implementiert intern alle ADO-Ereignishandler. Deshalb wird ein Ereignis, das durch einen **Connection** - oder **Recordset** -Vorgang verursacht wird, von einem ADO/WFC-Ereignishandler abgefangen. Der ADO/WFC-Ereignishandler übergibt **ConnectionEvent** -Parameter von ADO in einer Instanz der **ConnectionEvent** -Klasse von ADO/WFC oder **RecordsetEvent** -Parameter von ADO in einer Instanz der **RecordsetEvent** -Klasse von ADO/WFC. Diese ADO/WFC-Klassen konsolidieren die ADO-Ereignisparameter. Das heißt, jede ADO/WFC-Klasse enthält ein Datenelement für jeden eindeutigen Parameter in allen **ConnectionEvent** - oder **RecordsetEvent** -Methoden von ADO.

5.  ADO/WFC ruft dann den Ereignishandler mit dem ADO/WFC-Ereignisobjekt auf. Beispielsweise weist Ihr **onConnectComplete** -Handler eine Signatur wie die folgende auf:
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    Das erste Argument ist der Objekttyp, der das Ereignis gesendet hat ([Connection](connection-object-ado.md) oder [Recordset](recordset-object-ado.md)), und das zweite Argument ist das ADO/WFC-Ereignisobjekt (**ConnectionEvent** oder **RecordsetEvent**). Die Signatur des Ereignishandlers ist einfacher als ein ADO-Ereignis. Sie müssen jedoch dennoch das ADO-Ereignismodell kennen, um zu wissen, welche Parameter für ein Ereignis gelten und wie reagiert werden soll.

6.  Wechseln Sie vom Ereignishandler zurück zum ADO/WFC-Handler für das ADO-Ereignis. ADO/WFC kopiert die entsprechenden Datenelemente für das ADO/WFC-Ereignis zurück in die ADO-Ereignisparameter, und anschließend wird wieder der ADO-Ereignishandler angezeigt.

7.  Wenn Sie die Verarbeitung abgeschlossen haben, entfernen Sie den Handler aus der Liste der ADO/WFC-Ereignishandler. Verwenden Sie die Methode mit einem Namen wie z. B. **removeOn**_EventName_(*handler*).

