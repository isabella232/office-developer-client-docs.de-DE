---
title: Ereignisse in der Outlook-PIA
TOCTitle: Events in the Outlook PIA
ms:assetid: 1f9eafb3-6645-4e27-81fa-5d73bf94ae40
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb644571(v=office.15)
ms:contentKeyID: 55119782
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29217a633c02390587a370847291ef62d5621ce8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699212"
---
# <a name="events-in-the-outlook-pia"></a>Ereignisse in der Outlook-PIA

Wenn Sie die primäre Interopassembly (PIA) von Outlook durchsuchen, werden Sie bemerken, dass viele Schnittstellen- und Ereignisstellvertretungen nach aus dem Outlook-Objektmodell bekannten Objekt- und Ereignisnamen benannt sind. Anders als Ereignisse in der COM-Typbibliothek werden Ereignisse in der Outlook-PIA nicht in der gleichen Schnittstelle wie Methoden oder Eigenschaften des gleichen Objekts definiert. Ereignisabhängige Schnittstellen, Stellvertretungen und Senkenhilfsklassen werden entweder importiert oder erstellt, um Ereignisse in der Outlook-PIA zu unterstützen. Dieses Thema beschreibt die ereignisabhängigen Schnittstellen, Stellvertretungen und Senkenhilfsklassen.

## <a name="where-do-the-event-interfaces-delegates-and-sink-helper-classes-come-from"></a>Herkunft der ereignisabhängigen Schnittstellen, Stellvertretungen und Senkenhilfsklassen

Beim Erstellen der Outlook-PIA verwendet Outlook das Type Library Importer-Tool (TLBIMP) von .NET Framework, um die Typdefinitionen der COM-Typbibliothek in entsprechende Definitionen einer Common Language Runtime-Assemby (CLR) zu konvertieren. TLBIMP importiert die folgenden beiden Typen von Schnittstellen für jedes Objekt:

  - Die primäre Schnittstelle (zum Beispiel die [\_Application](https://msdn.microsoft.com/library/bb611255\(v=office.15\))-Schnittstelle)

  - Die Ereignisschnittstelle (zum Beispiel die [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\))-Schnittstelle)

TLBIMP verarbeitet die importierten Schnittstellen und erstellt eine Anzahl von Schnittstellen, Stellvertretungen und Klassen, einschließlich der .NET-Schnittstelle (zum Beispiel die [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) -Schnittstelle). Verfügt das Objekt über Ereignisse, werden die folgenden erstellt:

  - Die Ereignisschnittstelle (zum Beispiel die [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))-Schnittstelle)

  - Stellvertretung für jedes Ereignis (zum Beispiel die [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\))-Stellvertretung)

  - Senkenhilfsklassen (zum Beispiel die [ApplicationEvents\_11\_SinkHelper](https://msdn.microsoft.com/library/bb609842\(v=office.15\))-Klasse)

### <a name="multiple-versions-of-events"></a>Mehrere Versionen von Ereignissen

Einige Objekte für mehrere verschiedene Versionen von Outlook verfügen über unterschiedliche Implementierungen von Ereignissen (je nach Version) und über zusätzliche Ereignisse, die hinzugefügt wurden, als neue Versionen veröffentlicht wurden. Um diese Ereignisse zu unterstützen, die über verschieden Versionen variieren, kennzeichnet Outlook diese ereignisabhängigen Schnittstellen, Stellvertretungen und Klassen, indem die Versionsnummer zum Namen hinzugefügt wird. Beispiel:

  - Die importierten Ereignisschnittstellen des **Application**-Objekts beinhalten:
    
      - Die erste Version für Outlook 98 und Outlook 2000: die [ApplicationEvents](https://msdn.microsoft.com/library/bb644093\(v=office.15\))-Schnittstelle
    
      - Die Version für Outlook 2002: die [ApplicationEvents\_10](https://msdn.microsoft.com/library/bb647702\(v=office.15\))-Schnittstelle
    
      - Die Version für Outlook 2003 und spätere Versionen: die [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\))-Schnittstelle

  - Die von TLBIMP erstellten .NET-Ereignisschnittstellen für das **Application**-Objekt umfassen:
    
      - Die erste Version für Outlook 98 und Outlook 2000: die [ApplicationEvents\_Event](https://msdn.microsoft.com/library/bb609380\(v=office.15\))-Schnittstelle
    
      - Die Version für Outlook 2002: die [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\))-Schnittstelle
    
      - Die Version für Outlook 2003 und spätere Versionen: die [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))-Schnittstelle

  - Die Stellvertretungen, die TLBIMP für jedes Ereignis in jeder Version des **Application**-Objekts erstellt hat. Zum Beispiel: eine Stellvertretung für jede Version des ItemSend-Ereignisses:
    
      - Die erste Version für Outlook 98 und Outlook 2000: die [ApplicationEvents\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb622515\(v=office.15\))-Stellvertretung
    
      - Die Version für Outlook 2002: die [ApplicationEvents\_10\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb646436\(v=office.15\))-Stellvertretung
    
      - Die Version für Outlook 2003 und spätere Versionen: die [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\))-Stellvertretung

Logischerweise werden Ereignisse, die in einer späteren Version hinzugefügt wurden, nicht in Ereignisschnittstellen früherer Version angezeigt und verfügen dort auch nicht über entsprechende Stellvertretungen. Wenn das [AttachmentSelectionChange](https://msdn.microsoft.com/library/ff184926\(v=office.15\))-Ereignis beispielsweise zum [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\))-Objekt in Outlook 2010, hinzugefügt wurde, ist es nicht Bestandteil dieser früheren Ereignisschnittstellen für das Explorer-Objekt:

  - ExplorerEvents-Schnittstelle

  - ExplorerEvents\_Event-Schnittstelle

Andererseits können Sie das Ereignis in letzten .NET-Ereignisschnittstelle finden, ExplorerEvents\_10\_Event, und seine Stellvertretung für die Outlook 2010-Version in [ExplorerEvents\_10\_AttachmentSelectionChangeEventHandler](https://msdn.microsoft.com/library/ff185177\(v=office.15\)).

## <a name="what-the-event-interfaces-delegates-and-sink-helper-classes-are-for"></a>Zweck der Ereignisschnittstellen, Stellvertretungen und Senkenhilfsklassen

In diesem Abschnitt wird unter Verwendung des **Application**-Objekts beschrieben, was die einzelnen oben aufgeführten Schnittstellen und Klassen enthalten:

  - Die primäre Schnittstelle, \_Application, definiert alle Methoden und Eigenschaften von Application. In der Regel wird diese Schnittstelle nicht im Code verwendet, mit Ausnahme einer nachfolgend besprochenen Bedingung.

  - Die Ereignisschnittstellen, die durch TLBIMP importiert wurden, wie ApplicationEvents\_11 and ApplicationEvents\_10, definieren Methoden, die Ereignisse von Application in der entsprechenden Version von Outlook zuordnen. Verwenden Sie diese Schnittstelle nicht im Code.

  - Die Ereignisschnittstellen von TLBIMP wie ApplicationEvents\_11\_Event und ApplicationEvents\_10\_Event definieren alle Ereignisse in Application in der entsprechenden Version von Outlook. Beim Entwerfen eines Ereignishandlers für Ereignisse in einer bestimmten Version implementieren Sie den Ereignishandler als Methode und verbinden die Methode mit dem Ereignis, das in der entsprechenden Version der .NET-Ereignisschnittstelle definiert wurde. In der Regel wird im Code nicht auf diese Ereignisse verwiesen, mit Ausnahme einer nachfolgend besprochenen Bedingung.

  - Die .NET-Schnittstelle, Application, erbt die \_Application-Schnittstelle und die ApplicationEvents\_11\_Event-Schnittstelle. Diese Schnittstelle wird üblicherweise im verwalteten Code verwendet, um auf das Objekt, die Methode, die Eigenschaft und die aktuellen Ereignismitglieder des **Application**-Objekts zuzugreifen. Es gibt allerdings zwei Ausnahmen, in denen Sie nicht die .NET-Schnittstelle, sondern eine andere Schnittstelle verwenden, um sich mit einem Ereignis zu verbinden:
    
      - Wenn Sie auf ein Ereignis zugreifen, das denselben Namen wie eine Methode des Objekts verwendet, wechseln Sie zur entsprechenden Ereignisschnittstelle, um sich mit dem Ereignis zu verbinden. Zum Verbinden mit dem [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\))-Ereignis, wechseln Sie beispielsweise zur ApplicationEvents\_11\_Event-Schnittstelle.
    
      - Wenn Sie sich mit einer früheren Version eines Ereignisses verbinden, das mittlerweile in einer späteren Version von Outlook erweitert wurde, verbindne Sie sich mit der früheren Version des Ereignisses. Wenn Sie beispielsweise statt der neuesten Version die Version des Quit-Ereignisses für das **Application**-Objekt aufrufen möchten, die für Outlook 2002 implementiert wurde, rufen Sie das [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\))-Ereignis auf, das in der ApplicationEvents\_10\_Event-Schnittstelle definiert ist, statt des Quit-Ereignisses, das in der ApplicationEvents\_11\_Event-Schnittstelle definiert ist.

  - Stellvertretungen bieten ein Framework zum Erstellen von benutzerdefinierten Ereignishandlern für bestimmte Ereignisse in einer bestimmten Version von Outlook. Wenn Sie beispielsweise eine Überprüfung des Vorhandenseins von Betreffzeilen in Outlook-Elementen, bevor diese gesendet werden, hinzufügen möchten, implementieren Sie diese Überprüfung in einer Rückrufmethode mit derselben Signatur wie die Stellvertretung, ApplicationEvents\_11\_ItemSendEventHandler. Verknüpfen Sie dann die Rückrufmethode als ein Ereignishandler für das ItemSend-Ereignis, das in der ApplicationEvents\_11\_-Schnittstelle definiert ist. Weitere Informationen über das Verbinden von Rückrufmethoden als Ereignishandler für ein Objekt finden Sie unter [Verbinden mit benutzerdefinierten Ereignishandlern](connecting-to-custom-event-handlers.md).

  - Die Senkenhilfsklassen von TLBIMP, wie ApplicationEvents\_11\_SinkHelper and [ApplicationEvents\_10\_SinkHelper](https://msdn.microsoft.com/library/bb644070\(v=office.15\)), sind Ereignishilfsobjekte für Application-Ereignisse in der entsprechenden Version von Outlook. Verwenden Sie diese Klassen nicht im Code.

## <a name="see-also"></a>Siehe auch

- [Zuordnen der Outlook-PIA zum Objektmodell](relating-the-outlook-pia-with-the-object-model.md)
- [Objekte in der Outlook-PIA](objects-in-the-outlook-pia.md)
- [Methoden und Eigenschaften in der Outlook-PIA](methods-and-properties-in-the-outlook-pia.md)
- [Entwickeln von verwalteten Outlook-Add-Ins mithilfe der Outlook-PIA](developing-managed-outlook-add-ins-using-the-outlook-pia.md)

