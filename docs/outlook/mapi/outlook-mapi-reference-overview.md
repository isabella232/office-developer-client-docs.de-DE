---
title: �bersicht �ber Outlook-MAPI-Referenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Letzte �nderung: Freitag, 1. Februar 2013'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793323"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="062ce-103">�bersicht �ber Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="062ce-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="062ce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="062ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="062ce-105">Dieses Thema enth�lt einen �berblick �ber die Referenz zur Outlook 2013-MAPI-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="062ce-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="062ce-106">Informationen zu dieser Dokumentation</span><span class="sxs-lookup"><span data-stu-id="062ce-106">About this documentation</span></span>

<span data-ttu-id="062ce-107">Diese Dokumentation gilt f�r die Implementierung der Messaging-API (MAPI) in Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="062ce-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="062ce-108">Vor Microsoft Office Outlook 2007 war die MAPI-Programmiererreferenz Teil der Microsoft Exchange-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="062ce-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="062ce-109">[!HINWEIS] Da in Exchange die Verwendung von MAPI seit Microsoft Exchange Server 2007 keine gro�e Bedeutung mehr hat, ist die Unterst�tzung f�r die Exchange-Implementierung eingeschr�nkt.</span><span class="sxs-lookup"><span data-stu-id="062ce-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="062ce-p101">Die Outlook-Implementierung von MAPI unterscheidet sich von der Microsoft Exchange-Implementierung. Die Outlook-Implementierung ist f�r eine Ausf�hrung auf Clientcomputern optimiert und legt Wert auf geringe Wartezeit. Die Exchange-Implementierung ist f�r Server gedacht, bei denen hohe Verf�gbarkeit und besseres Multithreading wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="062ce-p101">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation. The Outlook implementation is optimized for running on client computers and emphasizes low latency. The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="062ce-p102">Verwenden Sie diese Dokumentation f�r Anwendungen auf Endbenutzersystemen. Verwenden Sie f�r Serveranwendungen die Exchange-Implementierung von MAPI, sofern zutreffend, oder verwenden Sie aktuelle Exchange-APIs, wie z. B. Exchange-Webdienste. Weitere Informationen zu Exchange-Webdiensten finden Sie in der [Exchange-Webdienstereferenz](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="062ce-p102">Use this documentation for applications running on end-user systems. For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services. For more information on Exchange Web Services, see the [Exchange Web Services Reference](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="062ce-p103">Es k�nnen m�glicherweise Anwendungen geschrieben werden, die mit der Outlook- oder der Exchange-Implementierung von MAPI funktionieren. Beispielsweise funktioniert MFCMAPI gut auf beiden Plattformen. Die Implementierungen haben viele gemeinsame Funktionen, es gibt jedoch offensichtliche und subtile Unterschiede. Sie m�ssen sorgf�ltig auf beiden Plattformen testen, wenn Sie m�chten, dass Ihre Anwendung in allen Umgebungen funktioniert. Diese Tests erfordern zwei Systeme, da das Ausf�hren beider Implementierungen auf demselben Betriebssystem nicht unterst�tzt wird.</span><span class="sxs-lookup"><span data-stu-id="062ce-p103">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI. For example, MFCMAPI works well on either platform. The implementations have many common features, but there are differences both obvious and subtle. You will have to test carefully on both platforms if you intend for your application to work in all environments. This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="062ce-p104">Bedenken Sie, dass MAPI f�r den einfachen Zugriff auf Daten in einem MAPI-Speicher oder zum Erstellen eines Transportspeichers, eines Nachrichtenspeichers oder Adressbuchanbieters geeignet ist. Da MAPI die Gesch�ftslogik von Outlook umgeht, sollten Sie auch die Verwendung des Outlook-Objektmodells in Betracht ziehen, wenn Sie APIs f�r das Erstellen Ihrer L�sung auswerten. Das Outlook-Objektmodell schlie�t die Outlook-Gesch�ftslogik ein, ist jedoch nicht geeignet f�r Multithread-Code, Synchronisierungsanbieter oder Windows-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="062ce-p104">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider. Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution. The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="062ce-124">Weitere Informationen zu Neuigkeiten in dieser Version finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="062ce-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="062ce-125">Neu in dieser Edition (engl.)</span><span class="sxs-lookup"><span data-stu-id="062ce-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="062ce-126">In dieser Edition veraltete API-Elemente</span><span class="sxs-lookup"><span data-stu-id="062ce-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="062ce-127">Wenn Sie noch nicht mit der Entwicklung von MAPI-Anwendungen f�r Outlook lesen Sie die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="062ce-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="062ce-128">Ausw�hlen einer API oder Technologie f�r die Entwicklung von L�sungen f�r Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="062ce-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [<span data-ttu-id="062ce-129">H�ufig verwendete Headerdateien</span><span class="sxs-lookup"><span data-stu-id="062ce-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="062ce-130">H�ufig verwendete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="062ce-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="062ce-131">H�ufig verwendete Objekte</span><span class="sxs-lookup"><span data-stu-id="062ce-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="062ce-132">Die restliche Referenz ist in die folgenden drei Informationstypen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="062ce-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="062ce-133">[MAPI-Beispiele](mapi-samples.md) Leitet Sie zu zahlreichen Codebeispielen weiter, in denen die Verwendung von verschiedenen API-Elementen, die Implementierung grundlegender MAPI-Anbieter und das Erstellen von Outlook-Elementen veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="062ce-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="062ce-134">[MAPI-Konzepte (engl.)](mapi-concepts.md) Erl�utert die Konzepte und die Architektur von MAPI.</span><span class="sxs-lookup"><span data-stu-id="062ce-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="062ce-135">[MAPI Reference](mapi-reference.md) Bietet detaillierte Informationen zu den Funktionen, Schnittstellen, Strukturen und Eigenschaften in MAPI.</span><span class="sxs-lookup"><span data-stu-id="062ce-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="062ce-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="062ce-136">See also</span></span>

- [<span data-ttu-id="062ce-137">Erste Schritte mit der Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="062ce-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="062ce-138">MAPI-Beispiele</span><span class="sxs-lookup"><span data-stu-id="062ce-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="062ce-139">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="062ce-139">MAPI Concepts</span></span>](mapi-concepts.md)

