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
ms.openlocfilehash: 1f931382e790da13e7d4a746e286d9dc176b7b6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571906"
---
# <a name="mapi-service-providers"></a>MAPI-Dienstanbieter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Es gibt drei gängige Typen der Dienstanbieter:
  
- Beheben von adressbuchanbietern implementierte.
    
- Nachricht-Anbieter.
    
- Transport-Anbieter.
    
Address Book und Message-Anbieter müssen viele ähnlichkeiten. Registrieren sie einen eindeutigen Bezeichner MAPI, die sie zum Erstellen von Eintragsbezeichner für Objekte verwenden. Sie bieten eine Hierarchie von Objekten und Eigenschaften, die Clients zugreifen und diese bearbeiten können. Für ihre Containerobjekte unterstützen sie eine Hierarchie und einer Inhaltstabelle. Sie unterstützen ereignisbenachrichtigung zu diesen Tabellen und optional für einzelne Objekte, damit Clients über Änderungen informiert werden können, die während der Sitzung auftreten. Wenn Vorgänge langen werden, können sie eine Statusanzeige um informieren den Benutzer über den Vorgang Status anzeigen. Können Clients kommunizieren mit Address Book und Message-Anbieter entweder indirekt über MAPI mithilfe der [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) und [IMAPISession: IUnknown](imapisessioniunknown.md) Schnittstellen oder direkt mithilfe eines der Service Provider-Schnittstellen in der in der folgenden Tabelle. 
  
|**Address Book Provider-Schnittstellen**|**Nachricht Store Provider-Schnittstellen**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Transportanbieter unterscheiden sich von Adresse Adressbuch und Nachricht Speicher-Anbieter in die Möglichkeit, den, die Sie mit MAPI- und -Clients kommunizieren. In der Regel warten Transportanbieter MAPI, um Informationen dazu auffordern, anstatt Kommunikation zu initiieren. Im Gegensatz zu anderen Anbietern unterstützt Transportanbieter keine Vielzahl von Objekten und Tabellen, die von Clients häufig zugegriffen werden. Allerdings unterstützen sie ein Statusobjekt wie alle-Dienstanbieter, und seine Eigenschaften in der Statustabelle veröffentlichen. Während Address Book und Message-Anbieter die [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode zum Registrieren der eindeutige Bezeichner für die Erstellung ihrer Eintragsbezeichner aufrufen, rufen Sie Transportanbieter die [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode Registrieren Sie sich eindeutige Bezeichner als auch-Adresstypen für die Verantwortung für die Übermittlung von bestimmten Nachrichten. 
  
Ihren Dienstanbieter müssen drei Headerdateien: eine öffentliche Headerdatei und zwei interne Dateien. Verwenden Sie die öffentlichen Header-Datei aus, für die Konfiguration und zum Dokumentieren von Eigenschaften und deren Werten. Enthalten Sie in einem der internen Headerdateien alle erforderlichen öffentlichen MAPI-Header. Diese Headerdatei sollte in allen der Service Provider Quelldateien enthalten sein. Verwenden Sie die anderen interne Datei Resource Identifier definieren.
  
Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden Aufgaben aus:
  
- Geben Sie eine Eintrag-Funktion. 
    
- Geben Sie ein Anbieter und Anmeldeobjekt zur Verarbeitung von Anmelde- und Initialisierung an. 
    
- Wenn der Anbieter eine Message Service gehört, geben Sie eine Nachricht Service Entry Point-Funktion. 
    
- Konfiguration durch die Implementierung eines Eigenschaftenblatts unterstützt.
    
- Implementieren Sie ein Statusobjekt und Unterstützung der Statustabelle. 
    
- Handle Herunterfahren.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte](mapi-concepts.md)

