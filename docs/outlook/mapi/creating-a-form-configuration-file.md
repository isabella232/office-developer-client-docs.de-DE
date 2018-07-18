---
title: Erstellen einer Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791483"
---
# <a name="creating-a-form-configuration-file"></a>Erstellen einer Formularkonfigurationsdatei

  
  
**Betrifft**: Outlook 
  
Eine Konfigurationsdatei Formular enthält Informationen zu einem Formular, an den Formular-Manager verwendeten und Clientanwendungen. Eine Konfigurationsdatei Formular enthält eine umfassende Spezifikation für ein Formular, einschließlich der Eigenschaften, die vom Formular für die Verwendung von messaging-Clients, die vom Formular implementierte Verben und die Plattformen, die vom Formular veröffentlicht.
  
Eine Konfigurationsdatei Formular ist eine Datei mit der Erweiterung cfg und weist das Format einer Windows-Initialisierungsdatei ähnelt. Es handelt sich um eine nur-Text-Datei mit einer Anzahl von Abschnitten. Jeder Abschnitt beginnt mit einem Abschnittsnamen, die in Klammern eingeschlossen. Jeder Abschnitt enthält eine oder mehrere Zeilen, die Werte und Einstellungen für diesen Abschnitt relevant definieren. Werte haben einen der folgenden Typen:
  
- Zeichenfolge
    
- Zeichenfolge angezeigt
    
- Plattformzeichenfolge
    
- Pfadname
    
- Ganze Zahl
    
- GUID
    
Weitere Informationen zu den Abschnitten einer Datei CFG finden Sie unter [File Format des Formulars Konfigurationsdateien](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

