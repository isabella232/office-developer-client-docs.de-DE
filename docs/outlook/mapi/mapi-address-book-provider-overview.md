---
title: Übersicht über den MAPI-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 262b32b2ee95c3f9eb0a83db00f37bcb78c23b88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584150"
---
# <a name="mapi-address-book-provider-overview"></a>Übersicht über den MAPI-Adressbuchanbieter
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter verarbeiten den Zugriff auf Verzeichnisinformationen. Verzeichnisinformationen bestehen aus Daten für zwei Arten von Nachrichtenempfängern: einzelne Messagingbenutzer und Gruppen von Messagingbenutzern, die häufig in Verteilerlisten gemeinsam adressiert werden. Je nach Empfängertyp und Adressbuchanbieter gibt es eine Vielzahl von Informationen, die zur Verfügung gestellt werden können. Beispielsweise speichern alle Adressbuchanbieter den Namen, die Adresse und den Adresstyp eines Empfängers.
  
Jeder Adressbuchanbieter organisiert diese Daten mithilfe eines oder mehrerer Container. Die Anzahl und Struktur der Container hängt von der Implementierung des Adressbuchanbieters ab. Beispielsweise kann ein Adressbuchanbieter einen einzelnen Container verwenden, um alle Informationen zu speichern, ein anderer einen Container auf oberster Ebene, der Untercontainer enthält, und ein dritter Container kann mehrere Container auf oberster Ebene verwenden, die jeweils Untercontainer enthalten. Eine Adressbuchcontainerhierarchie kann recht tief sein. Es gibt keine Beschränkung für die Anzahl von Untercontainern, die verwendet werden können.
  
Die folgende Abbildung zeigt eine typische MAPI-Adressbuchorganisation.
  
**Adressbuchorganisation**
  
![Adressbuchorganisation](media/amapi_04.gif "Adressbuchorganisation")
  
MAPI integriert alle von den installierten Adressbuchanbietern bereitgestellten Informationen in ein einzelnes Adressbuch und stellt eine einheitliche Ansicht für die Clientanwendung dar. Die integrierte Liste enthält die Container auf oberster Ebene, die von jedem der installierten Adressbuchanbieter angezeigt werden. Die meisten Adressbuchanbieter machen nur wenige Container (in der Regel ein bis drei) auf der obersten Ebene verfügbar, um in die oberste Ebene des integrierten MAPI-Adressbuchs aufgenommen zu werden. Beispielsweise kann ein Adressbuchanbieter "Alle Benutzer" und "Lokale Benutzer" als zwei Container auf oberster Ebene verfügbar machen.
  
Die Benutzer von Clientanwendungen können den Inhalt von Adressbuchcontainern anzeigen und in einigen Fällen den Inhalt ändern. Adressbuchcontainer können je nach Adressbuchanbieter mit unterschiedlichen Zugriffsebenen erstellt werden. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

