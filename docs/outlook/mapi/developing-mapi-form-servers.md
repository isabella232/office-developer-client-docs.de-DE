---
title: Entwickeln von MAPI-Formularservern
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
# <a name="developing-mapi-form-servers"></a>Entwickeln von MAPI-Formularservern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Abschnitt wird das Erstellen ausführbarer Und Formularkonfigurationsdateien für formularserver zum Erstellen benutzerdefinierter MAPI-Formulare beschrieben. Bevor Sie diesen Abschnitt lesen, sollten Sie sich mit den Informationen in [MAPI Forms vertraut machen.](mapi-forms.md)
  
Die Entwicklung eines Formularservers umfasst die folgenden Schritte:
  
1. Entscheiden Sie, welche Informationen das Formular enthalten soll, und wählen Sie einen Satz von Eigenschaften aus, um diese Informationen zu enthalten. Weitere Informationen finden Sie [unter Choosing a Form's Property Set](choosing-a-form-s-property-set.md).
    
2. Entwerfen einer Benutzeroberfläche, mit der Benutzer mit den Eigenschaften des Formulars interagieren können.
    
3. Auswählen einer Nachrichtenklasse und Generieren einer eindeutigen Klassen-ID (CLSID). Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI Message Classes](mapi-message-classes.md). Weitere Informationen zu Nachrichtenklassen und Formularen finden Sie unter [Choosing a Message Class](choosing-a-message-class.md).
    
4. Implementieren der erforderlichen MAPI-Formularschnittstellen sowie optionaler Schnittstellen, die Ihr bestimmter Formularserver benötigt. Weitere Informationen finden Sie unter [Writing Form Server Code](writing-form-server-code.md). 
    
5. Schreiben von Benutzeroberflächencode zur Verarbeitung der Benutzerinteraktion mit dem Formularobjekt und den vom Formular verwendeten Eigenschaften.
    
6. Erstellen einer Formularkonfigurationsdatei für das Formular. Weitere Informationen finden Sie [unter Dateiformat von Formularkonfigurationsdateien](file-format-of-form-configuration-files.md).
    
7. Installieren des Formulars auf den Computern der Benutzer. Weitere Informationen finden Sie unter [Installing a Form into a Library](installing-a-form-into-a-library.md).
    
Wahrscheinlich führen Sie die Schritte 1 bis 5 gleichzeitig aus, anstatt sie in der Reihenfolge durchzuführen. Der Prozess der Entwicklung eines Formularservers ist wie viele Programmierprojekte kein Prozess, in dem eine besonders definierte Sequenz vorhanden ist. Das Erstellen einer Formularkonfigurationsdatei wird z. B. als vorletzter Schritt angezeigt, Aber Sie erstellen ihre Formularkonfigurationsdatei wahrscheinlich inkrementell, und sie wird vollständiger, wenn Sie Dem Formularserver Features hinzufügen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

