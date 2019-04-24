---
title: �bersicht �ber Outlook-MAPI-Referenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Letzte Änderung: Freitag, 1. Februar 2013'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348496"
---
# <a name="outlook-mapi-reference-overview"></a>Übersicht über die Outlook-MAPI-Referenz

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema bietet Übersichtsinformationen zur Referenzdokumentation für die Outlook 2013-MAPI.
  
## <a name="about-this-documentation"></a>Informationen zu dieser Dokumentation

Diese Dokumentation gilt für die Implementierung der Messaging-API (MAPI) in Microsoft Outlook 2013. 
  
Vor Microsoft Office Outlook 2007 war die MAPI-Programmiererreferenz Teil der Microsoft Exchange-Dokumentation.
  
> [!NOTE]
> [!HINWEIS] Da in Exchange die Verwendung von MAPI seit Microsoft Exchange Server 2007 keine gro�e Bedeutung mehr hat, ist die Unterst�tzung f�r die Exchange-Implementierung eingeschr�nkt. 
  
Die Outlook-Implementierung von MAPI unterscheidet sich von der Microsoft Exchange-Implementierung. Die Outlook-Implementierung ist f�r eine Ausf�hrung auf Clientcomputern optimiert und legt Wert auf geringe Wartezeit. Die Exchange-Implementierung ist f�r Server gedacht, bei denen hohe Verf�gbarkeit und besseres Multithreading wichtig sind.
  
Verwenden Sie diese Dokumentation f�r Anwendungen auf Endbenutzersystemen. Verwenden Sie f�r Serveranwendungen die Exchange-Implementierung von MAPI, sofern zutreffend, oder verwenden Sie aktuelle Exchange-APIs, wie z. B. Exchange-Webdienste. Weitere Informationen zu Exchange-Webdiensten finden Sie in der [Exchange-Webdienstereferenz](https://msdn.microsoft.com/library/bb204119.aspx).
  
Es k�nnen m�glicherweise Anwendungen geschrieben werden, die mit der Outlook- oder der Exchange-Implementierung von MAPI funktionieren. Beispielsweise funktioniert MFCMAPI gut auf beiden Plattformen. Die Implementierungen haben viele gemeinsame Funktionen, es gibt jedoch offensichtliche und subtile Unterschiede. Sie m�ssen sorgf�ltig auf beiden Plattformen testen, wenn Sie m�chten, dass Ihre Anwendung in allen Umgebungen funktioniert. Diese Tests erfordern zwei Systeme, da das Ausf�hren beider Implementierungen auf demselben Betriebssystem nicht unterst�tzt wird.
  
Bedenken Sie, dass MAPI f�r den einfachen Zugriff auf Daten in einem MAPI-Speicher oder zum Erstellen eines Transportspeichers, eines Nachrichtenspeichers oder Adressbuchanbieters geeignet ist. Da MAPI die Gesch�ftslogik von Outlook umgeht, sollten Sie auch die Verwendung des Outlook-Objektmodells in Betracht ziehen, wenn Sie APIs f�r das Erstellen Ihrer L�sung auswerten. Das Outlook-Objektmodell schlie�t die Outlook-Gesch�ftslogik ein, ist jedoch nicht geeignet f�r Multithread-Code, Synchronisierungsanbieter oder Windows-Anwendungen.
  
Weitere Informationen zu Neuigkeiten in dieser Version finden Sie unter den folgenden Themen:
  
- [Neu in dieser Edition (engl.)](what-s-new-in-this-edition.md)
    
- [In dieser Edition veraltete API-Elemente](api-elements-deprecated-in-this-edition.md)
    
Wenn Sie noch nicht mit der Entwicklung von MAPI-Anwendungen f�r Outlook lesen Sie die folgenden Themen:
  
- [Ausw�hlen einer API oder Technologie f�r die Entwicklung von L�sungen f�r Outlook 2013](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [H�ufig verwendete Headerdateien](commonly-used-header-files.md)
    
- [H�ufig verwendete Eigenschaften](commonly-used-properties.md)
    
- [H�ufig verwendete Objekte](commonly-used-objects.md)
    
Die restliche Referenz ist in die folgenden drei Informationstypen unterteilt:
  
- [MAPI-Beispiele](mapi-samples.md) Leitet Sie zu zahlreichen Codebeispielen weiter, in denen die Verwendung von verschiedenen API-Elementen, die Implementierung grundlegender MAPI-Anbieter und das Erstellen von Outlook-Elementen veranschaulicht wird. 
    
- [MAPI-Konzepte (engl.)](mapi-concepts.md) Erl�utert die Konzepte und die Architektur von MAPI. 
    
- [MAPI Reference](mapi-reference.md) Bietet detaillierte Informationen zu den Funktionen, Schnittstellen, Strukturen und Eigenschaften in MAPI. 
    
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)
- [MAPI-Beispiele](mapi-samples.md)
- [MAPI-Konzepte (engl.)](mapi-concepts.md)

