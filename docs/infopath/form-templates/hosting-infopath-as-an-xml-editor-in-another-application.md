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
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hosten von InfoPath als XML-Editor in einer anderen Anwendung

Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows gehostet werden. Mit diesem Feature können Entwickler die InfoPath-Formularbearbeitungsumgebung in Geschäftsanwendungen integrieren. Entwickler, die herkömmliche COM-basierte Anwendungen schreiben, können das **InfoPathEditorObject-Objekt** verwenden, das verfügbar ist, indem sie auf die IPEDITOR.DLL verweisen, und Entwickler, die Microsoft schreiben. NET-basierte Anwendungen können **microsoft.Office. InfoPath.FormControl-Assembly,** die verwaltete Typen basierend auf der COM-Schnittstelle bietet. Die IPEDITOR.DLL und **Microsoft.Office. Die InfoPath.FormControl-Assembly** wird zusammen mit InfoPath im Ordner C:\Program Files\Microsoft Office\Office15 oder C:\Program Files (x86)\Microsoft Office\Office15 installiert. 
  
Der MSDN-Artikel hosten die InfoPath 2007-Formularbearbeitungsumgebung in einer benutzerdefinierten Windows-Formularanwendung und befasst sich mit dem **FormControl-Objekt** und derEn Integration in Ihre benutzerdefinierte . NET-basierte Anwendungen. Der Download für diesen Artikel enthält eine benutzerdefinierte Anwendung, die .NET-Funktionen zum Replizieren der InfoPath-Formularbearbeitungsumgebung mithilfe der COM-Schnittstelle **IOleCommandTargets** bereitstellt.
  

