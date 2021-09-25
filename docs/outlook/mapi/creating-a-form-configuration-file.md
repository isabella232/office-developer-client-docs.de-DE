---
title: Erstellen einer Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 621660ab3a366ae38bf7c10d3bc83ce19b51b39f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576421"
---
# <a name="creating-a-form-configuration-file"></a>Erstellen einer Formularkonfigurationsdatei

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularkonfigurationsdatei stellt Informationen zu einem Formular sowohl für den verwendeten Formular-Manager als auch für Clientanwendungen bereit. Eine Formularkonfigurationsdatei enthält eine umfassende Spezifikation für ein Formular, einschließlich der vom Formular veröffentlichten Eigenschaften für die Verwendung durch Messagingclients, der vom Formular implementierten Verben und der vom Formular unterstützten Plattformen.
  
Eine Formularkonfigurationsdatei ist eine Datei mit der Erweiterung CFG und hat ein ähnliches Format wie eine Windows Initialisierungsdatei. Es handelt sich um eine Nur-Text-Datei mit einer Reihe von Abschnitten. Jeder Abschnitt beginnt mit einem Abschnittsnamen, der in eckige Klammern eingeschlossen ist. Jeder Abschnitt enthält eine oder mehrere Zeilen, die für diesen Abschnitt relevante Werte und Einstellungen definieren. Werte haben einen der folgenden Typen:
  
- String
    
- Angezeigte Zeichenfolge
    
- Plattformzeichenfolge
    
- Pfadname
    
- Ganze Zahl
    
- GUID
    
Weitere Informationen zu den Abschnitten einer CFG-Datei finden Sie unter ["Dateiformat von Formularkonfigurationsdateien".](file-format-of-form-configuration-files.md)
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

