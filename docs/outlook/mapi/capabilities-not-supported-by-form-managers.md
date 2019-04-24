---
title: Von Formular Managern nicht unterstützte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326376"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Von Formular Managern nicht unterstützte Funktionen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden Features werden vom standardmäßigen Formular-Manager aus Leistungsgründen nicht unterstützt, können jedoch von benutzerdefinierten Formular-Managern unterstützt werden.
  
- Eine Hierarchie, die das Gruppieren oder Kategorisieren von Formularen in einer Formularbibliothek ermöglicht. Eine Formularbibliothek ist eine Flatfile-Datenbank mit Formularen.
    
- Zugriffssteuerung für Formular Kategorien, die Nachrichtenklassen oder übergeordneten Klassen entsprechen.
    
- Unterstützung für mehrere Sprachversionen desselben Formulars in einer einzelnen Formularbibliothek.
    
Dies sind Implementierungsprobleme. Es gibt nichts, was verhindert, dass ein benutzerdefinierter Formular-Manager diese Features implementiert.
  
Die MAPI-Formulararchitektur unterstützt nicht mehrere Formular-Manager, die gleichzeitig laufen. Obwohl MAPI mehrere gleichzeitige Nachrichtenspeicher Anbieter, Transportanbieter und Adressbuchanbieter unterstützt, wird nur ein einziger Formular-Manager unterstützt.
  
Da möglicherweise nur ein Formular-Manager gleichzeitig gestartet wird, müssen Sie, wenn Sie einen benutzerdefinierten Formular-Manager implementieren, alle Funktionen aus dem standardmäßigen Formular-Manager, den Sie benötigen, erneut implementieren. Da Ihr benutzerdefinierter Formular-Manager den standardmäßigen Formular-Manager vollständig ersetzen wird, sind die Funktionen des Standardformular-Managers nur dann verfügbar, wenn Sie in Ihrem benutzerdefinierten Formular-Manager dupliziert werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

