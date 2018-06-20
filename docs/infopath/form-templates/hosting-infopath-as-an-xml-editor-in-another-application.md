---
title: Hosten von InfoPath als XML-Editor in einer anderen Anwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Der Microsoft InfoPath-formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden ermöglicht Entwicklern das Integrieren von InfoPath-Formular formularbearbeitungsumgebung in Line-of-Business Applications.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790726"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="f8cf2-103">Hosten von InfoPath als XML-Editor in einer anderen Anwendung</span><span class="sxs-lookup"><span data-stu-id="f8cf2-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="f8cf2-104">Der Microsoft InfoPath-formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="f8cf2-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="f8cf2-105">Dieses Feature ermöglicht Entwicklern das Integrieren von InfoPath-Formular formularbearbeitungsumgebung in Line-of-Business Applications.</span><span class="sxs-lookup"><span data-stu-id="f8cf2-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="f8cf2-106">Entwickler von herkömmlichen COM-basierten können **InfoPathEditorObject** -Objekt, das durch einen Verweis auf die DLL-Datei IPEDITOR verfügbar ist. DLL-Datei, und Entwickler von Microsoft. NET-basierte Anwendung können die Assembly **Microsoft.Office.InfoPath.FormControl** die verwaltete Typen basierend auf der COM-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f8cf2-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="f8cf2-107">DLL-Datei IPEDITOR. DLL und **Microsoft.Office.InfoPath.FormControl** sind beide zusammen mit InfoPath im c:\Programme\Gemeinsame Dateien (x86) \Microsoft Office\Office15 Ordner C:\Program Files\Microsoft Office\Office15 oder installiert.</span><span class="sxs-lookup"><span data-stu-id="f8cf2-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="f8cf2-108">Hosten der InfoPath 2007-Formularbearbeitungsumgebung in einer benutzerdefinierten Windows Forms-Anwendung im MSDN-Artikel konzentriert sich auf das Objekt **FormControl** und wie Sie sie in Ihre benutzerdefinierte integrieren. NET-basierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f8cf2-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="f8cf2-109">Der Download für den Artikel enthält eine benutzerdefinierte Anwendung, die .NET Funktionen für die Replikation von formularbearbeitungsumgebung durch die Verwendung von COM- **IOleCommandTargets**InfoPath-Formular bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f8cf2-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

