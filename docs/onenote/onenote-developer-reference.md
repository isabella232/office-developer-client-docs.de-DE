---
title: OneNote-Entwicklerreferenz
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Diese Referenz enthält konzeptionelle Übersichten und programmatische Referenzen, die Sie beim Entwickeln von Lösungen für OneNote 2013-Desktopclientanwendungen unterstützen sollen.
ms.openlocfilehash: 8af3f0b8623f0b457250ea11f185a25cadec7386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790914"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="64406-103">OneNote-Entwicklerreferenz</span><span class="sxs-lookup"><span data-stu-id="64406-103">OneNote developer reference</span></span>

<span data-ttu-id="64406-104">Diese Referenz enthält konzeptionelle Übersichten und programmatische Referenzen, die Sie beim Entwickeln von Lösungen für OneNote 2013-Desktopclientanwendungen unterstützen sollen.</span><span class="sxs-lookup"><span data-stu-id="64406-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="64406-105">Sie enthält alle Ergänzungen und Änderungen der OneNote 2013-Anwendungsprogrammierschnittstelle (API) und bietet Codebeispiele in C#, um zu zeigen, wie Sie einige Aufgaben in OneNote ausführen können.</span><span class="sxs-lookup"><span data-stu-id="64406-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C# and Visual Basic to show how to perform common tasks in Outlook.</span></span> <span data-ttu-id="64406-106">Über die OneNote 2013-API können Benutzer programmgesteuert auf OneNote-Inhalte zugreifen und diese bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="64406-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="64406-107">Benutzer können auch Änderungen an der Ansicht von OneNote-Fenstern vornehmen.</span><span class="sxs-lookup"><span data-stu-id="64406-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="64406-108">Diese Dokumentation enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="64406-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="64406-109">[Fensterschnittstellen](window-interfaces-onenote.md): Beschreibt die **Window**- und **Windows**-Schnittstellen, über die Benutzer die Reihe von OneNote-Fenstern durchlaufen und bestimmte Fenstereigenschaften ändern können.</span><span class="sxs-lookup"><span data-stu-id="64406-109">Window interfaces: Describes the Window and Windows interfaces, which enable users to enumerate through the set of onnvshort windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="64406-110">[Schnittstellen für das Schnellablage-Dialogfeld](quick-filing-dialog-box-interfaces-onenote.md): Beschreibt die Schnittstellen, die Sie verwenden können, um das Dialogfeld für die **Schnellablage** in OneNote 2013 programmgesteuert anzupassen.</span><span class="sxs-lookup"><span data-stu-id="64406-110">Quick Filing dialog box interfaces: Describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in on15short.</span></span> 
    
- <span data-ttu-id="64406-111">[Anwendungsschnittstelle](application-interface-onenote.md): Beschreibt Methoden, Eigenschaften und Ereignisse, mit denen OneNote 2013-Informationen und -Inhalte abgerufen, bearbeitet und aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="64406-111">Application interface: Describes methods, properties, and events that help retrieve, manipulate, and update on15short information and content.</span></span>
    
- <span data-ttu-id="64406-112">[Enumerationen](enumerations-onenote-developer-reference.md): Beschreibt die Enumerationen im OneNote 2013-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="64406-112">Enumerations: Describes the enumerations in the on15short object model.</span></span>
    
- <span data-ttu-id="64406-113">[Fehlercodes](error-codes-onenote.md): In diesem Thema werden die Fehlercodes im OneNote 2013-Objektmodell aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="64406-113">This topic lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="64406-p102">Die in dieser Dokumentation beschriebenen APIs sind nur für OneNote Win32-Desktopclientlösungen in nicht verbundenen Szenarios. Verwenden Sie für verbundene Szenarien die empfohlenen OneNote-Dienst-APIs. Weitere Informationen finden Sie unter [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="64406-p102">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios. For connected scenarios, use the recommended OneNote service APIs. To learn more, visit [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64406-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64406-117">See also</span></span>

- [<span data-ttu-id="64406-118">OneNote für Entwickler</span><span class="sxs-lookup"><span data-stu-id="64406-118">OneNote for developers</span></span>](http://go.microsoft.com/fwlink/?LinkID=390615)
    
- <span data-ttu-id="64406-119">[Beispiele auf GitHub](https://github.com/OneNoteDev/) (OneNote-Dienst-APIs)</span><span class="sxs-lookup"><span data-stu-id="64406-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span> 
    
- [<span data-ttu-id="64406-120">Barrierefreiheit in Microsoft-Produkten</span><span class="sxs-lookup"><span data-stu-id="64406-120">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)
    
- [<span data-ttu-id="64406-121">Konventionen in diesem Dokument</span><span class="sxs-lookup"><span data-stu-id="64406-121">Document Conventions</span></span>](http://msdn.microsoft.com/de-DE/office/aa905365.aspx)
    
- [<span data-ttu-id="64406-122">OneNote-Entwicklerreferenz – Copyrightinformationen</span><span class="sxs-lookup"><span data-stu-id="64406-122">OneNote 2013 Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/de-DE/library/office/jj680116.aspx)
    
- [<span data-ttu-id="64406-123">Microsoft Online-Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="64406-123">Microsoft Online Privacy Notice</span></span>](http://privacy.microsoft.com/de-DE/default.mspx)
    

