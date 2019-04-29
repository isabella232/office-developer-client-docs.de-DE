---
title: Entwickeln von MAPI-Formular Servern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420766"
---
# <a name="developing-mapi-form-servers"></a>Entwickeln von MAPI-Formular Servern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Abschnitt wird das Erstellen von ausführbaren Formularserver-und Formular Konfigurationsdateien zum Erstellen benutzerdefinierter MAPI-Formulare beschrieben. Bevor Sie diesen Abschnitt lesen, sollten Sie sich mit den Informationen in [MAPI-Formularen](mapi-forms.md)vertraut machen.
  
Die Entwicklung eines Formular Servers umfasst die folgenden Schritte:
  
1. Entscheiden Sie, welche Informationen das Formular enthalten soll, und wählen Sie eine Reihe von Eigenschaften aus, um diese Informationen zu speichern. Weitere Informationen finden Sie unter [Auswählen eines Formulareigenschaften Satzes](choosing-a-form-s-property-set.md).
    
2. Entwerfen einer Benutzeroberfläche, mit der Benutzer mit den Eigenschaften des Formulars interagieren können.
    
3. Auswählen einer Nachrichtenklasse und Generieren einer eindeutigen Klassen-ID (CLSID). Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI Message Classes](mapi-message-classes.md). Weitere Informationen zu Nachrichtenklassen und-Formularen finden Sie unter [Auswählen einer Nachrichtenklasse](choosing-a-message-class.md).
    
4. Implementieren der erforderlichen MAPI-Formular Schnittstellen sowie aller optionalen Schnittstellen, die für Ihren speziellen Formularserver erforderlich sind. Weitere Informationen finden Sie unter [Schreiben von Formular Server Code](writing-form-server-code.md). 
    
5. Schreiben von Benutzeroberflächencode, um die Interaktion des Benutzers mit dem Form-Objekt und den vom Formular verwendeten Eigenschaften zu behandeln.
    
6. Erstellen einer Formular Konfigurationsdatei für das Formular. Weitere Informationen finden Sie unter [Datei Format von Formular Konfigurationsdateien](file-format-of-form-configuration-files.md).
    
7. Installieren des Formulars auf Benutzercomputern. Weitere Informationen finden Sie unter [Installieren eines Formulars in einer Bibliothek](installing-a-form-into-a-library.md).
    
Sie werden die Schritte 1 bis 5 höchstwahrscheinlich gleichzeitig ausführen, statt Sie nacheinander abzuschließen. Der Prozess der Entwicklung eines Formular Servers ist, wie viele Programmierprojekte, nicht eine, in der es eine besonders gut definierte Sequenz gibt. Beispielsweise wird das Erstellen einer Formular Konfigurationsdatei als der vorletzte Schritt oben angezeigt, aber Sie erstellen Ihre Formular Konfigurationsdatei wahrscheinlich inkrementell, und Sie wird umfassender, wenn Sie Ihrem Formularserver Features hinzufügen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

