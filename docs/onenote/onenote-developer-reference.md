---
title: OneNote-Entwicklerreferenz
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Diese Referenz enthält konzeptionelle Übersichten und programmgesteuerten Verweise als Leitfaden zur Entwicklung von Lösungen für OneNote 2013 desktop-Clientanwendungen.
ms.openlocfilehash: 8af3f0b8623f0b457250ea11f185a25cadec7386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790914"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="62e68-103">OneNote-Entwicklerreferenz</span><span class="sxs-lookup"><span data-stu-id="62e68-103">OneNote developer reference</span></span>

<span data-ttu-id="62e68-104">Diese Referenz enthält konzeptionelle Übersichten und programmgesteuerten Verweise als Leitfaden zur Entwicklung von Lösungen für OneNote 2013 desktop-Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="62e68-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="62e68-105">Es enthält alle Ergänzungen und Änderungen an der OneNote 2013 Application programming Interface (API) und bietet Beispielcode in c# zu veranschaulichen, wie einige Aufgaben in OneNote.</span><span class="sxs-lookup"><span data-stu-id="62e68-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="62e68-106">Der OneNote 2013-API ermöglicht Benutzern programmgesteuerten Zugriff auf und Bearbeiten von OneNote-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="62e68-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="62e68-107">Benutzer können auch die Ansicht der OneNote-Fenster ändern.</span><span class="sxs-lookup"><span data-stu-id="62e68-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="62e68-108">In dieser Dokumentation werden die folgenden Informationen bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="62e68-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="62e68-109">[Window-Schnittstellen](window-interfaces-onenote.md): Beschreibt die **Fenster** und **Windows** -Schnittstellen, mit deren Hilfe Benutzer bestimmte Fenstereigenschaften zu durchlaufen, die Gruppe von OneNote-Fenster.</span><span class="sxs-lookup"><span data-stu-id="62e68-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="62e68-110">[Schnelles ablegen Dialogfeld Feld Schnittstellen](quick-filing-dialog-box-interfaces-onenote.md): Beschreibt die Schnittstellen, die Sie zum programmgesteuerten Anpassung des Dialogfelds **Quick ablegen** in OneNote 2013 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="62e68-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="62e68-111">[Anwendungsschnittstelle](application-interface-onenote.md): Beschreibt Methoden, Eigenschaften und Ereignisse, mit deren Hilfe abrufen, bearbeiten und Aktualisieren von OneNote 2013 Informationen und Inhalte.</span><span class="sxs-lookup"><span data-stu-id="62e68-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="62e68-112">[Enumerationen](enumerations-onenote-developer-reference.md): Beschreibt die Enumerationen im Objektmodell von OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="62e68-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="62e68-113">[Fehlercodes](error-codes-onenote.md): Listet die Fehlercodes im Objektmodell von OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="62e68-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="62e68-p102">Die in dieser Dokumentation beschriebenen APIs sind nur für OneNote Win32-Desktopclientlösungen in nicht verbundenen Szenarios. Verwenden Sie für verbundene Szenarien die empfohlenen OneNote-Dienst-APIs. Weitere Informationen finden Sie unter [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="62e68-p102">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios. For connected scenarios, use the recommended OneNote service APIs. To learn more, visit [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62e68-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62e68-117">See also</span></span>

- [<span data-ttu-id="62e68-118">OneNote für Entwickler</span><span class="sxs-lookup"><span data-stu-id="62e68-118">OneNote for developers</span></span>](http://go.microsoft.com/fwlink/?LinkID=390615)
    
- <span data-ttu-id="62e68-119">[Beispiele für GitHub](https://github.com/OneNoteDev/) (OneNote Service-APIs)</span><span class="sxs-lookup"><span data-stu-id="62e68-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span> 
    
- [<span data-ttu-id="62e68-120">Accessibility in Microsoft Products (Barrierefreiheit in Microsoft-Produkten, in englischer Sprache)</span><span class="sxs-lookup"><span data-stu-id="62e68-120">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)
    
- [<span data-ttu-id="62e68-121">Konventionen für Office Developer-Dokumente</span><span class="sxs-lookup"><span data-stu-id="62e68-121">Document Conventions</span></span>](http://msdn.microsoft.com/de-de/office/aa905365.aspx)
    
- [<span data-ttu-id="62e68-122">Copyright-Informationen OneNote-Entwicklerreferenz</span><span class="sxs-lookup"><span data-stu-id="62e68-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/de-de/library/office/jj680116.aspx)
    
- [<span data-ttu-id="62e68-123">Auszüge aus den Onlinedatenschutzbestimmungen von Microsoft</span><span class="sxs-lookup"><span data-stu-id="62e68-123">Microsoft Online Privacy Notice</span></span>](http://privacy.microsoft.com/en-us/default.mspx)
    

