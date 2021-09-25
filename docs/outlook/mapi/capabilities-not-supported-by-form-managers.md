---
title: Von Formularmanagern nicht unterstützte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 50f0bb1159654c5dba1e24d00c36daabca8e4611
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605118"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Von Formularmanagern nicht unterstützte Funktionen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden Features werden vom Standardformular-Manager aus Leistungsgründen nicht unterstützt, können jedoch von benutzerdefinierten Formularmanagern unterstützt werden.
  
- Eine Hierarchie, die das Gruppieren oder Kategorisieren von Formularen in einer Formularbibliothek ermöglicht. Eine Formularbibliothek ist eine Flachdateidatenbank von Formularen.
    
- Zugriffssteuerung für Formularkategorien, die Nachrichtenklassen oder Superklassen entsprechen.
    
- Unterstützung für mehrere Sprachversionen desselben Formulars in einer einzelnen Formularbibliothek.
    
Dies sind Implementierungsprobleme. Es gibt nichts, was verhindert, dass ein benutzerdefinierter Formular-Manager diese Features implementiert.
  
Die MAPI-Formulararchitektur unterstützt nicht mehrere Gleichzeitig ausgeführte Formularmanager. Obwohl die MAPI mehrere gleichzeitige Nachrichtenspeicheranbieter, Transportanbieter und Adressbuchanbieter unterstützt, wird nur ein einzelner Formular-Manager unterstützt.
  
Da möglicherweise nur ein Formular-Manager gleichzeitig ausgeführt wird, müssen Sie beim Implementieren eines benutzerdefinierten Formular-Managers alle Funktionen des standardmäßigen Formular-Managers, die Sie benötigen, erneut implementieren. Da Ihr benutzerdefinierter Formular-Manager den Standardformular-Manager vollständig ersetzt, sind die Funktionen des Standardformular-Managers nicht verfügbar, es sei denn, sie werden im benutzerdefinierten Formular-Manager dupliziert.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

