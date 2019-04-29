---
title: Übersicht über den MAPI-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426541"
---
# <a name="mapi-address-book-provider-overview"></a>Übersicht über den MAPI-Adressbuchanbieter
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter behandeln den Zugriff auf Verzeichnisinformationen. Verzeichnisinformationen bestehen aus Daten für zwei Arten von Nachrichtenempfängern: einzelne Messagingbenutzer und Gruppen von Messaging Benutzern, die gemeinsam in Verteilerlisten adressiert werden. Je nach Empfängertyp und Adressbuchanbieter gibt es eine Vielzahl von Informationen, die verfügbar gemacht werden können. Alle Adressbuchanbieter speichern beispielsweise den Namen, die Adresse und den Adresstyp eines Empfängers.
  
Jeder Adressbuchanbieter organisiert diese Daten mithilfe eines oder mehrerer Container. Die Anzahl und Struktur der Container hängt von der Implementierung des Adressbuch Anbieters ab. Beispielsweise kann ein Adressbuchanbieter einen einzigen Container für alle Informationen verwenden, ein anderer Container der obersten Ebene, in dem untergeordnete Speicher enthalten sind, und ein drittes kann mehrere Container auf oberster Ebene verwenden, die jeweils untergeordnete Containers enthalten. Eine Adressbuch-Containerhierarchie kann sehr tief sein; Es gibt keine Begrenzung für die Anzahl der Untercontainer, die verwendet werden können.
  
Die folgende Abbildung zeigt eine typische MAPI-Adressbuch Organisation.
  
**Adressbuchorganisation**
  
![Adressbuch Organisation] (media/amapi_04.gif "Adressbuch Organisation")
  
MAPI integriert alle von den installierten Adressbuch Anbietern bereitgestellten Informationen in ein einzelnes Adressbuch und stellt eine einheitliche Ansicht für die Clientanwendung dar. In der integrierten Liste sind die Container der obersten Ebene aufgeführt, die von den einzelnen installierten Adressbuch Anbietern angezeigt werden. Die meisten Adressbuchanbieter setzen nur einige wenige Container (in der Regel eins bis drei) auf der obersten Ebene für die Aufnahme in die oberste Ebene des integrierten MAPI-Adressbuchs ein. Ein Adressbuchanbieter kann beispielsweise "alle Benutzer" und "lokale Benutzer" als zwei Container auf der obersten Ebene zur Verfügung stellen.
  
Die Benutzer von Clientanwendungen können die Inhalte von Adressbuch Containern anzeigen und in einigen Fällen den Inhalt ändern. Adressbuchcontainer können je nach Adressbuchanbieter mit unterschiedlichen Zugriffsebenen erstellt werden. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

