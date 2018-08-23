---
title: Übersicht über die MAPI-Adresse Adressbuch-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 855b145bcca8007601eb8e841665306d4c58982f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576561"
---
# <a name="mapi-address-book-provider-overview"></a>Übersicht über die MAPI-Adresse Adressbuch-Anbieter
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Adressbuch Anbieter Handle Zugriff auf Verzeichnisinformationen. Verzeichnisinformationen besteht aus Daten für zwei Arten von Nachrichtenempfängern: einzelne messaging-Benutzer und Gruppen von messaging-Benutzer, die häufig miteinander in Verteilerlisten behandelt werden. Je nach Art der Empfänger und die Adressbuchanbieter ist eine Vielzahl von Informationen, die verfügbar gemacht werden kann. Beispielsweise speichern alle adressbuchanbietern implementierte Name, Adresse und Adresstyp des Empfängers.
  
Jede Adressbuchanbieter organisiert diese Daten mithilfe eines oder mehrerer Container. Die Anzahl und die Struktur der Container, hängt von der Adressbuchanbieter Implementierung ab. Beispielsweise eine Adressbuchanbieter möglicherweise einen einzelnen Container verwenden, um alle Informationen enthalten, eine andere möglicherweise einen Container der obersten Ebene, die Untercontainer enthält verwenden und eine dritte möglicherweise mehrere Container auf oberster Ebene, jede Betrieb Untercontainer verwenden. Ein Container Adressbuchhierarchie kann sehr tiefe sein. Es gibt keine Begrenzung der Anzahl der Container, die verwendet werden können.
  
Die folgende Abbildung zeigt eine typische MAPI-Struktur des Adressbuchs.
  
**Adressbuchorganisation**
  
![Struktur des Adressbuchs] (media/amapi_04.gif "Struktur des Adressbuchs")
  
MAPI integriert alle Informationen, die von den installierten adressbuchanbietern implementierte bereitgestellt wird, in einem einzigen Adressbuch, einer Präsentation eine einheitliche Ansicht an die Clientanwendung. Die integrierte Liste zeigt die Container der obersten Ebene, die von den einzelnen der installierten adressbuchanbietern implementierte angezeigt. Die meisten adressbuchanbietern implementierte verfügbar machen nur ein paar Container (in der Regel von 1 bis 3) auf der obersten Ebene für die Einbeziehung in der obersten Ebene der MAPI-integrierte des Adressbuchs. Beispielsweise kann ein Adressbuchanbieter verfügbar "Alle Benutzer" und "Lokale Benutzer" als zwei Container der obersten Ebene stellen.
  
Die Benutzer der Clientanwendungen können den Inhalt der Address Book Container anzeigen und ändern den Inhalt in einigen Fällen. Mit unterschiedlichen Zugriffsebenen, je nach der Adressbuchanbieter können Address Book Containern erstellt werden. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

