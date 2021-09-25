---
title: Hosten von InfoPath als XML-Editor in einer anderen Anwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden, wodurch Entwickler die InfoPath-Formularbearbeitungsumgebung in Branchenanwendungen integrieren können.
ms.openlocfilehash: d5fab1cb5a211f72660e768cf5e9745676847904
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596743"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hosten von InfoPath als XML-Editor in einer anderen Anwendung

Die Microsoft InfoPath-Formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows Anwendung gehostet werden. Mit diesem Feature können Entwickler die InfoPath-Formularbearbeitungsumgebung in Branchenanwendungen integrieren. Entwickler, die herkömmliche COM-basierte Anwendungen schreiben, können das **infoPathEditorObject-Objekt** verwenden, das verfügbar ist, indem sie auf die IPEDITOR.DLL verweisen, und Entwickler, die Microsoft schreiben. NET-basierte Anwendungen können die **Microsoft.Office verwenden. InfoPath.FormControl-Assembly,** die verwaltete Typen basierend auf der COM-Schnittstelle bereitstellt. Die IPEDITOR.DLL und **Microsoft.Office. Die InfoPath.FormControl-Assembly** wird zusammen mit InfoPath im Ordner "C:\Programme\Microsoft Office\Office15" oder "C:\Programme (x86)\Microsoft Office\Office15" installiert. 
  
Der MSDN-Artikel "Hosten der InfoPath 2007-Formularbearbeitungsumgebung in einer benutzerdefinierten Windows Formularanwendung" befasst sich mit dem **FormControl-Objekt** und dessen Integration in Ihre benutzerdefinierte . NET-basierte Anwendungen. Der Download für diesen Artikel enthält eine benutzerdefinierte Anwendung, die .NET-Funktionen zum Replizieren der InfoPath-Formularbearbeitungsumgebung mithilfe der COM-Schnittstelle **IOleCommandTargets** bereitstellt.
  

