---
title: Hosten von InfoPath als XML-Editor in einer anderen Anwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden, die es Entwicklern ermöglicht, die InfoPath-Formularbearbeitungsumgebung in Branchenanwendungen zu integrieren.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303689"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hosten von InfoPath als XML-Editor in einer anderen Anwendung

Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden. Mit diesem Feature können Entwickler die InfoPath-Formularbearbeitungsumgebung in Branchenanwendungen integrieren. Entwickler, die herkömmliche COM-basierte Anwendungen schreiben, können das **InfoPathEditorObject** -Objekt verwenden, das verfügbar ist, indem Sie auf das IPEDITOR verweisen. DLL und Entwickler, die Microsoft schreiben. NET-basierte Anwendungen können die **Microsoft. Office. InfoPath. FormControl** -Assembly verwenden, die verwaltete Typen basierend auf der COM-Schnittstelle bereitstellt. Die IPEDITOR. DLL-und **Microsoft. Office. InfoPath. FormControl** -Assembly werden zusammen mit InfoPath im Ordner c:\Programme\Microsoft Office\Office15 or c:\Program Files (x86) \Microsoft Office\Office15 installiert. 
  
Der MSDN-Artikel, der die InfoPath 2007-Formularbearbeitungsumgebung in einer benutzerdefinierten Windows-Formularanwendung **** hostet, konzentriert sich auf das FormControl-Objekt und seine Einbindung in den benutzerdefinierten. NET-basierten Anwendungen. Der Download für diesen Artikel enthält eine benutzerdefinierte Anwendung, die .NET-Funktionen zum Replizieren der InfoPath-Formularbearbeitungsumgebung mithilfe der COM-Schnittstelle **IOleCommandTargets** bereitstellt.
  

