---
title: Übersicht über Outlook-MAPI-Referenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Letzte Änderung: Freitag, 1. Februar 2013'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723019"
---
# <a name="outlook-mapi-reference-overview"></a>Übersicht über die Outlook-MAPI-Referenz

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema bietet Übersichtsinformationen zur Referenzdokumentation für die Outlook 2013-MAPI.
  
## <a name="about-this-documentation"></a>Informationen zu dieser Dokumentation

Diese Dokumentation gilt für die Implementierung der Messaging-API (MAPI) in Microsoft Outlook 2013. 
  
Vor Microsoft Office Outlook 2007 war die MAPI-Programmiererreferenz Teil der Microsoft Exchange-Dokumentation.
  
> [!NOTE]
> Da in Exchange die Verwendung von MAPI seit Microsoft Exchange Server 2007 keine große Bedeutung mehr hat, ist die Unterstützung für die Exchange-Implementierung eingeschränkt. 
  
Die Outlook-Implementierung von MAPI unterscheidet sich von der Microsoft Exchange-Implementierung. Die Outlook-Implementierung ist für eine Ausführung auf Clientcomputern optimiert und legt Wert auf geringe Wartezeit. Die Exchange-Implementierung ist für Server gedacht, bei denen hohe Verfügbarkeit und besseres Multithreading wichtig sind.
  
Verwenden Sie diese Dokumentation für Anwendungen auf Endbenutzersystemen. Verwenden Sie für Serveranwendungen die Exchange-Implementierung von MAPI, sofern zutreffend, oder verwenden Sie aktuelle Exchange-APIs, wie z. B. Exchange-Webdienste. Weitere Informationen zu Exchange-Webdiensten finden Sie in der [Exchange-Webdienstereferenz](https://msdn.microsoft.com/library/bb204119.aspx).
  
Es können möglicherweise Anwendungen geschrieben werden, die mit der Outlook- oder der Exchange-Implementierung von MAPI funktionieren. Beispielsweise funktioniert MFCMAPI gut auf beiden Plattformen. Die Implementierungen haben viele gemeinsame Funktionen, es gibt jedoch offensichtliche und subtile Unterschiede. Sie müssen sorgfältig auf beiden Plattformen testen, wenn Sie möchten, dass Ihre Anwendung in allen Umgebungen funktioniert. Diese Tests erfordern zwei Systeme, da das Ausführen beider Implementierungen auf demselben Betriebssystem nicht unterstützt wird.
  
Bedenken Sie, dass MAPI für den einfachen Zugriff auf Daten in einem MAPI-Speicher oder zum Erstellen eines Transportspeichers, eines Nachrichtenspeichers oder Adressbuchanbieters geeignet ist. Da MAPI die Geschäftslogik von Outlook umgeht, sollten Sie auch die Verwendung des Outlook-Objektmodells in Betracht ziehen, wenn Sie APIs für das Erstellen Ihrer Lösung auswerten. Das Outlook-Objektmodell schließt die Outlook-Geschäftslogik ein, ist jedoch nicht geeignet für Multithread-Code, Synchronisierungsanbieter oder Windows-Anwendungen.
  
Weitere Informationen zu Neuigkeiten in dieser Version finden Sie unter den folgenden Themen:
  
- [Neu in dieser Edition](what-s-new-in-this-edition.md)
    
- [In dieser Edition veraltete API-Elemente](api-elements-deprecated-in-this-edition.md)
    
Wenn Sie noch nicht mit der Entwicklung von MAPI-Anwendungen für Outlook lesen Sie die folgenden Themen:
  
- [Auswählen einer API oder Technologie für die Entwicklung von Lösungen für Outlook 2013](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [Häufig verwendete Headerdateien](commonly-used-header-files.md)
    
- [Häufig verwendete Eigenschaften](commonly-used-properties.md)
    
- [Häufig verwendete Objekte](commonly-used-objects.md)
    
Die restliche Referenz ist in die folgenden drei Informationstypen unterteilt:
  
- [MAPI-Beispiele](mapi-samples.md) Leitet Sie zu zahlreichen Codebeispielen weiter, in denen die Verwendung von verschiedenen API-Elementen, die Implementierung grundlegender MAPI-Anbieter und das Erstellen von Outlook-Elementen veranschaulicht wird. 
    
- [MAPI-Konzepte](mapi-concepts.md) Erläutert die Konzepte und die Architektur von MAPI. 
    
- [MAPI Reference](mapi-reference.md) Bietet detaillierte Informationen zu den Funktionen, Schnittstellen, Strukturen und Eigenschaften in MAPI. 
    
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)
- [MAPI-Beispiele](mapi-samples.md)
- [MAPI-Konzepte](mapi-concepts.md)

