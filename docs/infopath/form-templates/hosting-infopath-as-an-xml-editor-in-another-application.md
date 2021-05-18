---
title: Hosten von InfoPath als XML-Editor in einer anderen Anwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden, mit der Entwickler die InfoPath-Formularbearbeitungsumgebung in Geschäftsanwendungen integrieren können.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422579"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="10d76-103">Hosten von InfoPath als XML-Editor in einer anderen Anwendung</span><span class="sxs-lookup"><span data-stu-id="10d76-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="10d76-104">Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="10d76-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="10d76-105">Mit diesem Feature können Entwickler die InfoPath-Formularbearbeitungsumgebung in Geschäftsanwendungen integrieren.</span><span class="sxs-lookup"><span data-stu-id="10d76-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="10d76-106">Entwickler, die herkömmliche COM-basierte Anwendungen schreiben, können das **InfoPathEditorObject-Objekt** verwenden, das verfügbar ist, indem sie auf die IPEDITOR.DLL verweisen, und Entwickler, die Microsoft schreiben. NET-basierte Anwendungen können **microsoft.Office. InfoPath.FormControl-Assembly,** die verwaltete Typen basierend auf der COM-Schnittstelle bietet.</span><span class="sxs-lookup"><span data-stu-id="10d76-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="10d76-107">Die IPEDITOR.DLL und **Microsoft.Office. Die InfoPath.FormControl-Assembly** wird zusammen mit InfoPath im Ordner C:\Program Files\Microsoft Office\Office15 oder C:\Program Files (x86)\Microsoft Office\Office15 installiert.</span><span class="sxs-lookup"><span data-stu-id="10d76-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="10d76-108">Der MSDN-Artikel hosten die InfoPath 2007-Formularbearbeitungsumgebung in einer benutzerdefinierten Windows-Formularanwendung und befasst sich mit dem **FormControl-Objekt** und derEn Integration in Ihre benutzerdefinierte . NET-basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="10d76-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="10d76-109">Der Download für diesen Artikel enthält eine benutzerdefinierte Anwendung, die .NET-Funktionen zum Replizieren der InfoPath-Formularbearbeitungsumgebung mithilfe der COM-Schnittstelle **IOleCommandTargets** bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="10d76-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

