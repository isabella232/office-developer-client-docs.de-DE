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
  
Adressbuchanbieter verarbeiten den Zugriff auf Verzeichnisinformationen. Verzeichnisinformationen bestehen aus Daten für zwei Arten von Nachrichtenempfängern: einzelne Messagingbenutzer und Gruppen von Messagingbenutzern, die häufig gemeinsam in Verteilerlisten adressiert werden. Je nach Empfängertyp und Adressbuchanbieter gibt es eine vielzahl von Informationen, die zur Verfügung stehen können. Beispielsweise speichern alle Adressbuchanbieter den Namen, die Adresse und den Adresstyp eines Empfängers.
  
Jeder Adressbuchanbieter organisiert diese Daten mithilfe eines oder mehreren Containern. Die Anzahl und Struktur der Container hängt von der Implementierung des Adressbuchanbieters ab. Ein Adressbuchanbieter kann z. B. einen einzelnen Container verwenden, um alle Informationen zu enthalten, ein anderer kann einen Container auf oberster Ebene verwenden, der Untercontainer enthält, und ein dritter kann mehrere Container auf oberster Ebene verwenden, die jeweils Untercontainer enthalten. Eine Adressbuchcontainerhierarchie kann recht tief sein. Es gibt keine Beschränkung der Anzahl von Untercontainern, die verwendet werden können.
  
Die folgende Abbildung zeigt eine typische MAPI-Adressbuchorganisation.
  
**Adressbuchorganisation**
  
![Adressbuchorganisation](media/amapi_04.gif "Adressbuchorganisation")
  
MAPI integriert alle Informationen, die von den installierten Adressbuchanbietern bereitgestellt werden, in ein einzelnes Adressbuch und stellt eine einheitliche Ansicht für die Clientanwendung zur Verfügung. Die integrierte Liste zeigt die Container auf oberster Ebene an, die von jedem der installierten Adressbuchanbieter angezeigt werden. Die meisten Adressbuchanbieter machen nur wenige Container (in der Regel 1 bis 3) auf oberster Ebene verfügbar, um in die oberste Ebene des integrierten Adressbuchs mapI zu integrieren. Ein Adressbuchanbieter kann beispielsweise "Alle Benutzer" und "Lokale Benutzer" als zwei Container auf oberster Ebene zur Verfügung stellen.
  
Die Benutzer von Clientanwendungen können den Inhalt von Adressbuchcontainern anzeigen und in einigen Fällen den Inhalt ändern. Adressbuchcontainer können je nach Adressbuchanbieter mit unterschiedlichen Zugriffsebenen erstellt werden. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

