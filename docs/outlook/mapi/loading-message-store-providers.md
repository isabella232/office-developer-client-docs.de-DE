---
title: Laden von Nachrichten Store Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2cd4cfe3ba259a46752083f12b962c749ef4ce3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595917"
---
# <a name="loading-message-store-providers"></a>Laden von Nachrichten Store Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung einen Nachrichtenspeicher öffnet, lädt MAPI die DLL des Nachrichtenspeicheranbieters in den Speicher. Nachdem die MAPI die DLL geladen hat, erfolgt eine sehr spezifische Sequenz von Methodenaufrufen zwischen dem Nachrichtenspeicheranbieter und der MAPI. Mit dieser Methodenaufrufsequenz kann MAPI [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)und [IMsgStore : IMAPIProp-Schnittstellen](imsgstoreimapiprop.md) der obersten Ebene abrufen und dem Nachrichtenspeicheranbieter das Abrufen eines MAPI-Supportobjekts ermöglichen. Nach der Aufrufsequenz sollte der Nachrichtenspeicheranbieter bereit sein, Anmeldungen von Clients zu akzeptieren. 
  
Die Aufrufsequenz beim Laden einer Nachrichtenanbieter-DLL lautet wie folgt:
  
1. Der Client ruft [IMAPISession::OpenMsgStore auf.](imapisession-openmsgstore.md)
    
2. Wenn der Nachrichtenspeicher noch nicht geöffnet ist, lädt MAPI die DLL des Speicheranbieters und ruft den [MSProviderInit-Einstiegspunkt](msproviderinit.md) der DLL auf. Wenn der Nachrichtenspeicher bereits geöffnet ist, überspringt MAPI die Schritte 2 und 3 und verwendet dann die vorhandene [IMSProvider : IUnknown-Schnittstelle,](imsprovideriunknown.md) um Schritt 4 abzuschließen. 
    
3. **MSProviderInit** erstellt ein **IMSProvider-Objekt** und gibt es zurück. 
    
4. MAPI ruft [IMSProvider::Logon auf](imsprovider-logon.md)und übergibt den Eintragsbezeichner für den Nachrichtenspeicher der Clientanwendung.
    
5. **IMSProvider::Logon** erstellt und gibt eine [IMSLogon : IUnknown-Schnittstelle](imslogoniunknown.md) und eine [IMsgStore : IMAPIProp-Schnittstelle](imsgstoreimapiprop.md) zurück und ruft dann die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) auf ihrer [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) auf. Wenn sich der Eintragsbezeichner des Clientnachrichtenspeichers auf einen bereits geöffneten Nachrichtenspeicher bezieht, kann der Nachrichtenspeicheranbieter vorhandene **IMSLogon-** und **IMsgStore-Schnittstellen** zurückgeben und muss **AddRef** nicht für sein Supportobjekt aufrufen. 
    
6. Wenn der Client das MAPI_NO_MAIL Flag bei der Anmeldung nicht festgelegt hat und die MDB_NO_MAIL in Schritt 1 nicht festgelegt hat, gibt MAPI den Eintragsbezeichner des Nachrichtenspeichers an den MAPI-Spooler weiter, damit sich der MAPI-Spooler am Nachrichtenspeicher anmelden kann.
    
7. MAPI gibt die **IMsgStore-Schnittstelle** an den Client zurück. 
    
8. Der MAPI-Spooler ruft [IMSProvider::SpoolerLogon auf.](imsprovider-spoolerlogon.md)
    
9. **IMSProvider::SpoolerLogon** gibt die gleichen **IMSLogon-** und **IMsgStore-Schnittstellen** aus Schritt 5 zurück. 
    
> [!NOTE]
> Wenn beim Anmeldeaufruf beim Nachrichtenspeicheranbieter ein Fehler auftritt, weil ein falsches Kennwort angegeben wurde und der Nachrichtenspeicheranbieter keine Schnittstelle zum Anfordern des richtigen Kennworts anzeigen kann, sollte MAPI_E_FAILONEPROVIDER aus der **IMSProvider::Logon-Methode** zurückgegeben werden. Dadurch können Clients den Benutzer auffordern, ein Kennwort einzugeben, um erneut beim Nachrichtenspeicheranbieter anzumelden, anstatt dass die MAPI den Anbieter für die gesamte Sitzung ausfällt. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

