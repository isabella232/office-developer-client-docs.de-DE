---
title: Funktionen, die von Formularmanagern nicht unterstützt werden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419380"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Funktionen, die von Formularmanagern nicht unterstützt werden

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden Features werden vom Standardmäßigen Formular-Manager aus Leistungsgründen nicht unterstützt, können jedoch von benutzerdefinierten Formularmanagern unterstützt werden.
  
- Eine Hierarchie, die das Gruppieren oder Kategorisieren von Formularen in einer Formularbibliothek ermöglicht. Eine Formularbibliothek ist eine Flachdateidatenbank von Formularen.
    
- Zugriffssteuerung für Formularkategorien, die Nachrichtenklassen oder Superklassen zugeordnet sind.
    
- Unterstützung für mehrere Sprachversionen desselben Formulars in einer einzelnen Formularbibliothek.
    
Dies sind Implementierungsprobleme. Es gibt nichts, was einen benutzerdefinierten Formular-Manager daran hindern kann, diese Features zu implementieren.
  
Die MAPI-Formulararchitektur unterstützt nicht mehrere Formularmanager, die gleichzeitig ausgeführt werden. Obwohl MAPI mehrere gleichzeitige Nachrichtenspeicheranbieter, Transportanbieter und Adressbuchanbieter unterstützt, wird nur ein einzelner Formular-Manager unterstützt.
  
Da möglicherweise nur ein Formular-Manager gleichzeitig ausgeführt wird, müssen Sie beim Implementieren eines benutzerdefinierten Formular-Managers alle benötigten Funktionen aus dem Standardformular-Manager neu implementieren. Da ihr benutzerdefinierter Formular-Manager den Standardformular-Manager vollständig ersetzt, stehen Funktionen des Standardformular-Managers nicht zur Verfügung, es sei denn, sie werden im benutzerdefinierten Formular-Manager dupliziert.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

