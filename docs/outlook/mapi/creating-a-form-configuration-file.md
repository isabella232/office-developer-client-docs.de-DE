---
title: Erstellen einer Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425218"
---
# <a name="creating-a-form-configuration-file"></a>Erstellen einer Formularkonfigurationsdatei

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularkonfigurationsdatei enthält Informationen zu einem Formular sowohl für den verwendeten Formular-Manager als auch für Clientanwendungen. Eine Formularkonfigurationsdatei enthält eine umfassende Spezifikation für ein Formular, einschließlich der vom Formular veröffentlichten Eigenschaften für die Verwendung durch Messagingclients, der vom Formular implementierten Verben und der vom Formular unterstützten Plattformen.
  
Eine Formularkonfigurationsdatei ist eine Datei mit einer CFG-Erweiterung und hat ein Format, das einer Windows ist. Es handelt sich um eine Nur-Text-Datei mit einer Reihe von Abschnitten. Jeder Abschnitt beginnt mit einem Abschnittsnamen, der in eckige Klammern eingeschlossen ist. Jeder Abschnitt enthält eine oder mehrere Zeilen, die Werte und Einstellungen definieren, die für diesen Abschnitt relevant sind. Werte haben einen der folgenden Typen:
  
- String
    
- Angezeigte Zeichenfolge
    
- Plattformzeichenfolge
    
- Pfadname
    
- Ganze Zahl
    
- GUID
    
Weitere Informationen zu den Abschnitten einer CFG-Datei finden Sie unter [Dateiformat von Formularkonfigurationsdateien](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

