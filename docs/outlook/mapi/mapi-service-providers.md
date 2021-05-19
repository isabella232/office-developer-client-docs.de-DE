---
title: MAPI-Dienstanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409538"
---
# <a name="mapi-service-providers"></a>MAPI-Dienstanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt drei allgemeine Typen von Dienstanbietern:
  
- Adressbuchanbieter.
    
- Nachrichtenspeicheranbieter.
    
- Transportanbieter.
    
Adressbuch- und Nachrichtenspeicheranbieter haben viele Ähnlichkeiten. Sie registrieren einen eindeutigen Bezeichner bei MAPI, den sie zum Erstellen von Eintragsbezeichnern für ihre Objekte verwenden. Sie stellen eine Hierarchie von Objekten und Eigenschaften zur Verfügung, auf die Clients zugreifen und diese bearbeiten können. Für ihre Containerobjekte unterstützen sie eine Hierarchietabelle und eine Inhaltstabelle. Sie unterstützen Ereignisbenachrichtigungen für diese Tabellen und optional für einzelne Objekte, damit Clients über Änderungen informiert werden können, die während der Sitzung auftreten. Wenn Vorgänge länger werden, können sie eine Statusanzeige anzeigen, um den Benutzer über den Status des Vorgangs zu informieren. Clients können mit Adressbuch- und Nachrichtenspeicheranbietern entweder indirekt über MAPI kommunizieren, indem sie das [IAddrBook verwenden: IMAPIProp](iaddrbookimapiprop.md) und [IMAPISession : IUnknown-Schnittstellen](imapisessioniunknown.md) oder direkt mithilfe einer der Dienstanbieterschnittstellen in der folgenden Tabelle. 
  
|**Adressbuchanbieterschnittstellen**|**Schnittstellen des Nachrichtenspeicheranbieters**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Transportanbieter unterscheiden sich von Adressbuch- und Nachrichtenspeicheranbietern in der Art und Weise, wie sie mit MAPI und mit Clients kommunizieren. Transportanbieter warten in der Regel darauf, dass MAPI sie zur Information anfordert, anstatt die Kommunikation zu initiieren. Im Gegensatz zu anderen Anbietern unterstützen Transportanbieter keine Vielzahl von Objekten und Tabellen, auf die häufig von Clients zugegriffen wird. Sie unterstützen jedoch wie alle Dienstanbieter ein Statusobjekt und veröffentlichen seine Eigenschaften in der Statustabelle. Während Adressbuch- und Nachrichtenspeicheranbieter die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) aufrufen, um eindeutige Bezeichner für die Erstellung ihrer Eintragsbezeichner zu registrieren, rufen Transportanbieter die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) auf, um eindeutige Bezeichner sowie Adresstypen für die Übernahme der Verantwortung für die Zustellung bestimmter Nachrichten zu registrieren. 
  
Ihr Dienstanbieter sollte über drei Headerdateien verfügen: eine öffentliche Headerdatei und zwei interne Dateien. Verwenden Sie die öffentliche Headerdatei zur Konfiguration und zum Dokumentieren von Eigenschaften und deren Werten. Schließen Sie in eine der internen Headerdateien alle erforderlichen öffentlichen #A0 ein. Diese Headerdatei sollte in allen Quelldateien des Dienstanbieters enthalten sein. Verwenden Sie die andere interne Datei, um Ressourcenbezeichner zu definieren.
  
Adressbuch-, Nachrichtenspeicher- und Transportanbieter führen die folgenden Aufgaben aus:
  
- Gibt eine Einstiegspunktfunktion an. 
    
- Liefern Sie einen Anbieter und ein Anmeldeobjekt, um die Anmeldung und Initialisierung zu verarbeiten. 
    
- Wenn der Anbieter zu einem Nachrichtendienst gehört, müssen Sie eine Einstiegspunktfunktion für den Nachrichtendienst verwenden. 
    
- Unterstützen Sie die Konfiguration, indem Sie ein Eigenschaftenblatt implementieren.
    
- Implementieren Sie ein Statusobjekt, und unterstützen Sie die Statustabelle. 
    
- Behandeln Des Herunterfahrens.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

