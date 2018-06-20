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
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hosten von InfoPath als XML-Editor in einer anderen Anwendung

Der Microsoft InfoPath-formularbearbeitungsumgebung kann in einer benutzerdefinierten Windows-Anwendung gehostet werden. Dieses Feature ermöglicht Entwicklern das Integrieren von InfoPath-Formular formularbearbeitungsumgebung in Line-of-Business Applications. Entwickler von herkömmlichen COM-basierten können **InfoPathEditorObject** -Objekt, das durch einen Verweis auf die DLL-Datei IPEDITOR verfügbar ist. DLL-Datei, und Entwickler von Microsoft. NET-basierte Anwendung können die Assembly **Microsoft.Office.InfoPath.FormControl** die verwaltete Typen basierend auf der COM-Schnittstelle. DLL-Datei IPEDITOR. DLL und **Microsoft.Office.InfoPath.FormControl** sind beide zusammen mit InfoPath im c:\Programme\Gemeinsame Dateien (x86) \Microsoft Office\Office15 Ordner C:\Program Files\Microsoft Office\Office15 oder installiert. 
  
Hosten der InfoPath 2007-Formularbearbeitungsumgebung in einer benutzerdefinierten Windows Forms-Anwendung im MSDN-Artikel konzentriert sich auf das Objekt **FormControl** und wie Sie sie in Ihre benutzerdefinierte integrieren. NET-basierte Anwendung. Der Download für den Artikel enthält eine benutzerdefinierte Anwendung, die .NET Funktionen für die Replikation von formularbearbeitungsumgebung durch die Verwendung von COM- **IOleCommandTargets**InfoPath-Formular bereitstellt.
  

