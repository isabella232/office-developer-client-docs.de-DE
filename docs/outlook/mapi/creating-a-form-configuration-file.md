---
title: Erstellen einer Formular Konfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333019"
---
# <a name="creating-a-form-configuration-file"></a>Erstellen einer Formular Konfigurationsdatei

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formular Konfigurationsdatei enthält Informationen zu einem Formular sowohl für den verwendeten Formular-Manager als auch für Clientanwendungen. Eine Formular Konfigurationsdatei enthält eine umfangreiche Spezifikation für ein Formular, einschließlich der Eigenschaften, die vom Formular für die Verwendung durch Messagingclients veröffentlicht werden, die Verben, die vom Formular implementiert werden, und die vom Formular unterstützten Plattformen.
  
Eine Formular Konfigurationsdatei ist eine Datei mit der Erweiterung. cfg und hat ein Format, das einer Windows-Initialisierungsdatei ähnelt. Es handelt sich um eine nur-Text-Datei mit einer Reihe von Abschnitten. Jeder Abschnitt beginnt mit einem Abschnittsnamen, der in eckigen Klammern eingeschlossen ist. Jeder Abschnitt enthält eine oder mehrere Zeilen, die Werte und Einstellungen für diesen Abschnitt definieren. Werte haben einen der folgenden Typen:
  
- Zeichenfolge
    
- Angezeigte Zeichenfolge
    
- Plattformzeichenfolge
    
- Pfadname
    
- Ganze Zahl
    
- GUID
    
Weitere Informationen zu den Abschnitten einer cfg-Datei finden Sie unter [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

