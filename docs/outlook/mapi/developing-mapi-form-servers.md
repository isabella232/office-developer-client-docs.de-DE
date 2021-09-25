---
title: Entwickeln von MAPI-Formularservern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af3960938defba5b14a602704ccd5a214951a6e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605034"
---
# <a name="developing-mapi-form-servers"></a>Entwickeln von MAPI-Formularservern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Abschnitt wird das Erstellen von ausführbaren Formularserver- und Formularkonfigurationsdateien zum Erstellen von benutzerdefinierten MAPI-Formularen beschrieben. Bevor Sie diesen Abschnitt lesen, sollten Sie sich mit den Informationen in [MAPI-Formularen](mapi-forms.md)vertraut machen.
  
Das Entwickeln eines Formularservers umfasst die folgenden Schritte:
  
1. Entscheiden Sie, welche Informationen das Formular enthalten soll, und wählen Sie eine Reihe von Eigenschaften aus, um diese Informationen zu speichern. Weitere Informationen finden Sie unter [Auswählen des Eigenschaftensatzes eines Formulars.](choosing-a-form-s-property-set.md)
    
2. Entwerfen einer Benutzeroberfläche, mit der Benutzer mit den Eigenschaften des Formulars interagieren können.
    
3. Auswählen einer Nachrichtenklasse und Generieren eines eindeutigen Klassenbezeichners (UNIQUE Class Identifier, CLSID). Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI-Nachrichtenklassen.](mapi-message-classes.md) Weitere Informationen zu Nachrichtenklassen und Formularen finden Sie unter [Auswählen einer Nachrichtenklasse.](choosing-a-message-class.md)
    
4. Implementieren der erforderlichen MAPI-Formularschnittstellen sowie aller optionalen Schnittstellen, die ihr bestimmter Formularserver benötigt. Weitere Informationen finden Sie unter [Schreiben von Formularservercode.](writing-form-server-code.md) 
    
5. Schreiben von Benutzeroberflächencode zum Behandeln der Benutzerinteraktion mit dem Formularobjekt und den eigenschaften, die das Formular verwendet.
    
6. Erstellen einer Formularkonfigurationsdatei für das Formular. Weitere Informationen finden Sie unter [Dateiformat von Formularkonfigurationsdateien.](file-format-of-form-configuration-files.md)
    
7. Installieren des Formulars auf den Computern der Benutzer. Weitere Informationen finden Sie unter [Installieren eines Formulars in einer Bibliothek.](installing-a-form-into-a-library.md)
    
Sie führen die Schritte 1 bis 5 wahrscheinlich gleichzeitig aus, anstatt sie nacheinander abzuschließen. Der Prozess der Entwicklung eines Formularservers ist, wie viele Programmierungsprojekte, kein Prozess, in dem es eine besonders gut definierte Sequenz gibt. Das Erstellen einer Formularkonfigurationsdatei wird z. B. im vorletzten Schritt oben angezeigt. Wahrscheinlich erstellen Sie die Formularkonfigurationsdatei jedoch inkrementell, und sie wird vollständiger, wenn Sie Ihrem Formularserver Features hinzufügen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

