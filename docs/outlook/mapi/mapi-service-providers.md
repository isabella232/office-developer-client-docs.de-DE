---
title: MAPI-Dienstanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346676"
---
# <a name="mapi-service-providers"></a>MAPI-Dienstanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt drei gängige Typen von Dienstanbietern:
  
- Adressbuchanbieter.
    
- Nachrichtenspeicher Anbieter.
    
- Transport Anbieter.
    
Adressbuch-und Nachrichtenspeicher Anbieter haben viele Ähnlichkeiten. Sie registrieren einen eindeutigen Bezeichner mit MAPI, den Sie zum Erstellen von Eintrags Bezeichnern für Ihre Objekte verwenden. Sie bieten eine Hierarchie von Objekten und Eigenschaften, auf die Clients zugreifen und diese bearbeiten können. Für Ihre Container-Objekte unterstützen Sie eine Hierarchietabelle und eine Inhaltstabelle. Sie unterstützen Ereignisbenachrichtigungen für diese Tabellen und optional für einzelne Objekte, sodass Clients über Änderungen informiert werden können, die während der Sitzung stattfinden. Wenn Vorgänge langwierig werden, können Sie eine Statusanzeige anzeigen, um den Benutzer über den Status des Vorgangs zu informieren. Clients können mit Adressbuch-und Nachrichtenspeicher Anbietern entweder indirekt über MAPI kommunizieren, indem Sie die [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) und [IMAPISession: IUnknown](imapisessioniunknown.md) -Schnittstellen verwenden oder direkt über eine der Dienstanbieter Schnittstellen in der folgende Tabelle. 
  
|**Schnittstellen des Adressbuch Anbieters**|**Schnittstellen des Nachrichtenspeicher Anbieters**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Transport Anbieter unterscheiden sich von Adressbuch-und Nachrichtenspeicher Anbietern bei der Kommunikation mit MAPI und mit Clients. Transport Anbieter warten in der Regel, bis MAPI Sie zur Information auffordert, statt die Kommunikation zu initiieren. Im Gegensatz zu anderen Anbietern unterstützen Transportanbieter keine Vielzahl von Objekten und Tabellen, auf die häufig Clients zugreifen. Sie unterstützen jedoch ein Status-Objekt, wie alle Dienstanbieter, und veröffentlichen die Eigenschaften in der Statustabelle. Während Adressbuch-und Nachrichtenspeicher Anbieter die [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode aufrufen, um eindeutige Bezeichner für die Erstellung Ihrer Eintragsbezeichner zu registrieren, rufen Transportanbieter die [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode auf, um Registrieren Sie eindeutige Bezeichner sowie Adresstypen für die Übernahme der Verantwortung für die Bereitstellung bestimmter Nachrichten. 
  
Der Dienstanbieter sollte drei Headerdateien haben: eine öffentliche Headerdatei und zwei interne Dateien. Verwenden Sie die öffentliche Headerdatei zur Konfiguration und zum Dokumentieren von Eigenschaften und deren Werten. Fügen Sie in eine der internen Headerdateien alle erforderlichen öffentlichen MAPI-Header ein. Diese Headerdatei sollte in allen Dienstanbieter-Quelldateien enthalten sein. Verwenden Sie die andere interne Datei, um Ressourcen-IDs zu definieren.
  
Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden Aufgaben aus:
  
- Geben Sie eine Einstiegspunktfunktion an. 
    
- Geben Sie einen Anbieter und ein Anmeldeobjekt an, um die Anmeldung und Initialisierung zu behandeln. 
    
- Wenn der Anbieter zu einem Nachrichtendienst gehört, geben Sie eine Einstiegspunktfunktion für den Nachrichtendienst ein. 
    
- Unterstützen der Konfiguration durch Implementieren eines Eigenschaftenblatts.
    
- Implementieren Sie ein Status-Objekt, und unterstützen Sie die Statustabelle. 
    
- Handle heruntergefahren.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

