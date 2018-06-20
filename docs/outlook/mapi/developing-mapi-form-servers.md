---
title: Entwickeln von MAPI-Formular-Servern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791543"
---
# <a name="developing-mapi-form-servers"></a>Entwickeln von MAPI-Formular-Servern

  
  
**Betrifft**: Outlook 
  
Dieser Abschnitt beschreibt den Prozess beim Erstellen von Forms Server ausführbare und Konfigurationsdateien für das Erstellen von benutzerdefinierter Formularen für MAPI-Formular. Vor dem Lesen dieses Abschnitts, sollten Sie sich mit den Informationen im [MAPI-Formulare](mapi-forms.md)vertraut machen.
  
Entwickeln von einem Formular Server umfasst die folgenden Schritte aus:
  
1. Entscheiden, welche Informationen des Formulars enthalten soll, und wählen Sie eine Gruppe von Eigenschaften, die diese Informationen enthalten soll. Weitere Informationen finden Sie unter [Auswählen eines Formulars-Eigenschaft festgelegt](choosing-a-form-s-property-set.md).
    
2. Entwerfen eine Benutzeroberfläche, mit denen Benutzer die Eigenschaften des Formulars interagieren können.
    
3. Auswählen einer Nachrichtenklasse und Generieren einer eindeutigen Klassen-ID (CLSID). Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI Message Classes](mapi-message-classes.md). Weitere Informationen zu Nachrichtenklassen und Formulare finden Sie unter [Auswählen einer Nachrichtenklasse](choosing-a-message-class.md).
    
4. Implementieren die erforderlichen Schnittstellen des MAPI-Formular als auch optionalen Schnittstellen, die Ihre Server bestimmten Formulars benötigt. Weitere Informationen finden Sie unter [Writing Formularcode Server](writing-form-server-code.md). 
    
5. Schreiben von Code für die Benutzeroberfläche zur Handhabung der Interaktion mit der Form-Objekt und die Eigenschaften des Benutzers verwendet das Formular.
    
6. Erstellen eine Formular-Konfigurationsdatei für das Formular. Weitere Informationen finden Sie unter [File Format des Formulars Konfigurationsdateien](file-format-of-form-configuration-files.md).
    
7. Das Formular wird auf den Computern der Benutzer installiert. Weitere Informationen finden Sie unter [Installieren eines Formulars in eine Bibliothek](installing-a-form-into-a-library.md).
    
Ausführen der Schritte 1 bis 5 wahrscheinlich gleichzeitig, anstatt sie in der Abfolge abschließen. Der Prozess der Entwicklung von einem Formular Server, wie viele Projekte programming, also keiner der in dem eine besonders gut definierte Sequenz vorhanden ist. Erstellen einer Konfigurationsdatei Formular ist beispielsweise dargestellt, wie die letzte Sekunde Schritt oben, aber wahrscheinlich Sie Ihre Konfiguration Formulardatei inkrementell erstellen und genauere Dies wird, wie Sie Features auf Ihrem Formular Server hinzufügen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

