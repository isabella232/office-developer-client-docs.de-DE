---
title: Übersicht über Outlook-MAPI-Referenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Letzte Änderung: Freitag, 1. Februar 2013'
ms.openlocfilehash: a5c1daf44f89d1ef8aa7472d69dfd7e86bbb92f6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388000"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="72f1f-103">Übersicht über die Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="72f1f-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="72f1f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72f1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72f1f-105">Dieses Thema bietet Übersichtsinformationen zur Referenzdokumentation für die Outlook 2013-MAPI.</span><span class="sxs-lookup"><span data-stu-id="72f1f-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="72f1f-106">Informationen zu dieser Dokumentation</span><span class="sxs-lookup"><span data-stu-id="72f1f-106">About this documentation</span></span>

<span data-ttu-id="72f1f-107">Diese Dokumentation gilt für die Implementierung der Messaging-API (MAPI) in Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="72f1f-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="72f1f-108">Vor Microsoft Office Outlook 2007 war die MAPI-Programmiererreferenz Teil der Microsoft Exchange-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="72f1f-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="72f1f-109">Da in Exchange die Verwendung von MAPI seit Microsoft Exchange Server 2007 keine große Bedeutung mehr hat, ist die Unterstützung für die Exchange-Implementierung eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="72f1f-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="72f1f-p101">Die Outlook-Implementierung von MAPI unterscheidet sich von der Microsoft Exchange-Implementierung. Die Outlook-Implementierung ist für eine Ausführung auf Clientcomputern optimiert und legt Wert auf geringe Wartezeit. Die Exchange-Implementierung ist für Server gedacht, bei denen hohe Verfügbarkeit und besseres Multithreading wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="72f1f-p101">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation. The Outlook implementation is optimized for running on client computers and emphasizes low latency. The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="72f1f-p102">Verwenden Sie diese Dokumentation für Anwendungen auf Endbenutzersystemen. Verwenden Sie für Serveranwendungen die Exchange-Implementierung von MAPI, sofern zutreffend, oder verwenden Sie aktuelle Exchange-APIs, wie z. B. Exchange-Webdienste. Weitere Informationen zu Exchange-Webdiensten finden Sie in der [Exchange-Webdienstereferenz](https://msdn.microsoft.com/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="72f1f-p102">Use this documentation for applications running on end-user systems. For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services. For more information on Exchange Web Services, see the [Exchange Web Services Reference](https://msdn.microsoft.com/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="72f1f-p103">Es können möglicherweise Anwendungen geschrieben werden, die mit der Outlook- oder der Exchange-Implementierung von MAPI funktionieren. Beispielsweise funktioniert MFCMAPI gut auf beiden Plattformen. Die Implementierungen haben viele gemeinsame Funktionen, es gibt jedoch offensichtliche und subtile Unterschiede. Sie müssen sorgfältig auf beiden Plattformen testen, wenn Sie möchten, dass Ihre Anwendung in allen Umgebungen funktioniert. Diese Tests erfordern zwei Systeme, da das Ausführen beider Implementierungen auf demselben Betriebssystem nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="72f1f-p103">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI. For example, MFCMAPI works well on either platform. The implementations have many common features, but there are differences both obvious and subtle. You will have to test carefully on both platforms if you intend for your application to work in all environments. This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="72f1f-p104">Bedenken Sie, dass MAPI für den einfachen Zugriff auf Daten in einem MAPI-Speicher oder zum Erstellen eines Transportspeichers, eines Nachrichtenspeichers oder Adressbuchanbieters geeignet ist. Da MAPI die Geschäftslogik von Outlook umgeht, sollten Sie auch die Verwendung des Outlook-Objektmodells in Betracht ziehen, wenn Sie APIs für das Erstellen Ihrer Lösung auswerten. Das Outlook-Objektmodell schließt die Outlook-Geschäftslogik ein, ist jedoch nicht geeignet für Multithread-Code, Synchronisierungsanbieter oder Windows-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="72f1f-p104">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider. Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution. The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="72f1f-124">Weitere Informationen zu Neuigkeiten in dieser Version finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="72f1f-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="72f1f-125">Neu in dieser Edition</span><span class="sxs-lookup"><span data-stu-id="72f1f-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="72f1f-126">In dieser Edition veraltete API-Elemente</span><span class="sxs-lookup"><span data-stu-id="72f1f-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="72f1f-127">Wenn Sie noch nicht mit der Entwicklung von MAPI-Anwendungen für Outlook lesen Sie die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="72f1f-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="72f1f-128">Auswählen einer API oder Technologie für die Entwicklung von Lösungen für Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="72f1f-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [<span data-ttu-id="72f1f-129">Häufig verwendete Headerdateien</span><span class="sxs-lookup"><span data-stu-id="72f1f-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="72f1f-130">Häufig verwendete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72f1f-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="72f1f-131">Häufig verwendete Objekte</span><span class="sxs-lookup"><span data-stu-id="72f1f-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="72f1f-132">Die restliche Referenz ist in die folgenden drei Informationstypen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="72f1f-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="72f1f-133">[MAPI-Beispiele](mapi-samples.md) Leitet Sie zu zahlreichen Codebeispielen weiter, in denen die Verwendung von verschiedenen API-Elementen, die Implementierung grundlegender MAPI-Anbieter und das Erstellen von Outlook-Elementen veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="72f1f-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="72f1f-134">[MAPI-Konzepte](mapi-concepts.md) Erläutert die Konzepte und die Architektur von MAPI.</span><span class="sxs-lookup"><span data-stu-id="72f1f-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="72f1f-135">[MAPI Reference](mapi-reference.md) Bietet detaillierte Informationen zu den Funktionen, Schnittstellen, Strukturen und Eigenschaften in MAPI.</span><span class="sxs-lookup"><span data-stu-id="72f1f-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="72f1f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72f1f-136">See also</span></span>

- [<span data-ttu-id="72f1f-137">Erste Schritte mit der Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="72f1f-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="72f1f-138">MAPI-Beispiele</span><span class="sxs-lookup"><span data-stu-id="72f1f-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="72f1f-139">MAPI-Konzepte</span><span class="sxs-lookup"><span data-stu-id="72f1f-139">MAPI Concepts</span></span>](mapi-concepts.md)

