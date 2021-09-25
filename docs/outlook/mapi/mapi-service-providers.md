---
title: MAPI-Dienstanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 369a87b0adc5f36a59beb2663f6204feb8f34e19
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595784"
---
# <a name="mapi-service-providers"></a>MAPI-Dienstanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt drei gängige Arten von Dienstanbietern:
  
- Adressbuchanbieter.
    
- Nachrichtenspeicheranbieter.
    
- Transportanbieter.
    
Adressbuch- und Nachrichtenspeicheranbieter haben viele Ähnlichkeiten. Sie registrieren einen eindeutigen Bezeichner bei der MAPI, den sie zum Erstellen von Eintragsbezeichnern für ihre Objekte verwenden. Sie stellen eine Hierarchie von Objekten und Eigenschaften bereit, auf die Clients zugreifen und diese bearbeiten können. Für ihre Containerobjekte unterstützen sie eine Hierarchietabelle und ein Inhaltsverzeichnis. Sie unterstützen Ereignisbenachrichtigungen für diese Tabellen und optional für einzelne Objekte, sodass Clients über Änderungen informiert werden können, die während der Sitzung auftreten. Wenn Vorgänge länger werden, können sie eine Statusanzeige anzeigen, um den Benutzer über den Status des Vorgangs zu informieren. Clients können mit Adressbuch- und Nachrichtenspeicheranbietern entweder indirekt über die MAPI kommunizieren, indem sie das [IAddrBook : IMAPIProp-](iaddrbookimapiprop.md) und [IMAPISession : IUnknown-Schnittstellen](imapisessioniunknown.md) verwenden oder direkt mithilfe einer der Dienstanbieterschnittstellen in der folgenden Tabelle. 
  
|**Adressbuchanbieterschnittstellen**|**Schnittstellen des Nachrichtenspeicheranbieters**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Transportanbieter unterscheiden sich von Adressbuch- und Nachrichtenspeicheranbietern in der Art und Weise, wie sie mit der MAPI und mit Clients kommunizieren. Transportanbieter warten in der Regel, bis die MAPI sie zur Eingabe von Informationen auffordert, anstatt die Kommunikation zu initiieren. Im Gegensatz zu den anderen Anbietern unterstützen Transportanbieter keine Vielzahl von Objekten und Tabellen, auf die clients häufig zugreifen. Sie unterstützen jedoch ein Statusobjekt wie alle Dienstanbieter und veröffentlichen seine Eigenschaften in der Statustabelle. Während Adressbuch- und Nachrichtenspeicheranbieter die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) aufrufen, um eindeutige Bezeichner für die Erstellung ihrer Eintragsbezeichner zu registrieren, rufen Transportanbieter die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) auf, um eindeutige Bezeichner sowie Adresstypen für die Übernahme der Verantwortung für die Zustellung bestimmter Nachrichten zu registrieren. 
  
Ihr Dienstanbieter sollte drei Headerdateien haben: eine öffentliche Headerdatei und zwei interne Dateien. Verwenden Sie die öffentliche Headerdatei für die Konfiguration und die Dokumentation von Eigenschaften und deren Werten. Alle erforderlichen öffentlichen MAPI-Header in eine der internen Headerdateien einschließen; Diese Headerdatei sollte in allen Quelldateien des Dienstanbieters enthalten sein. Verwenden Sie die andere interne Datei, um Ressourcenbezeichner zu definieren.
  
Adressbuch-, Nachrichtenspeicher- und Transportanbieter führen die folgenden Aufgaben aus:
  
- Geben Sie eine Einstiegspunktfunktion an. 
    
- Geben Sie einen Anbieter und ein Anmeldeobjekt an, um die Anmeldung und Initialisierung zu verarbeiten. 
    
- Wenn der Anbieter zu einem Nachrichtendienst gehört, geben Sie eine Nachrichtendienst-Einstiegspunktfunktion an. 
    
- Unterstützen der Konfiguration durch Implementieren eines Eigenschaftenblatts.
    
- Implementieren Sie ein Statusobjekt, und unterstützen Sie die Statustabelle. 
    
- Behandeln des Herunterfahrens.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

