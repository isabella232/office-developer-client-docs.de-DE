---
title: Laden von Nachrichten Store Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307805"
---
# <a name="loading-message-store-providers"></a>Laden von Nachrichten Store Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung einen Nachrichtenspeicher öffnet, lädt MAPI die DLL des Nachrichtenspeicheranbieters in den Arbeitsspeicher. Nachdem MAPI die DLL geladen hat, tritt eine sehr spezifische Abfolge von Methodenaufrufen zwischen dem Nachrichtenspeicheranbieter und MAPI auf. Mit dieser Methodenaufrufsequenz kann MAPI IMSProvider auf oberster Ebene [erhalten: IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)und [IMsgStore : IMAPIProp-Schnittstellen](imsgstoreimapiprop.md) und ermöglicht dem Nachrichtenspeicheranbieter, ein MAPI-Supportobjekt zu erhalten. Nach der Anrufsequenz sollte der Nachrichtenspeicheranbieter bereit sein, Anmeldungen von Clients zu akzeptieren. 
  
Die Aufrufsequenz beim Laden einer Nachrichtenanbieter-DLL lautet wie folgt:
  
1. Der Client ruft [IMAPISession::OpenMsgStore auf.](imapisession-openmsgstore.md)
    
2. Wenn der Nachrichtenspeicher noch nicht geöffnet ist, lädt MAPI die DLL des Speicheranbieters und ruft den [MSProviderInit-Einstiegspunkt](msproviderinit.md) der DLL auf. Wenn der Nachrichtenspeicher bereits geöffnet ist, überspringt MAPI die Schritte 2 und 3 und verwendet dann die vorhandene [IMSProvider : IUnknown-Schnittstelle,](imsprovideriunknown.md) um Schritt 4 zu schließen. 
    
3. **MSProviderInit** erstellt und gibt ein **IMSProvider-Objekt** zurück. 
    
4. MAPI ruft [IMSProvider::Logon auf](imsprovider-logon.md)und übertritt den Nachrichtenspeichereintragsbezeichner der Clientanwendung.
    
5. **IMSProvider::Logon** erstellt und gibt eine [IMSLogon : IUnknown-Schnittstelle](imslogoniunknown.md) und eine [IMsgStore : IMAPIProp-Schnittstelle](imsgstoreimapiprop.md) zurück und ruft dann die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) auf ihrer [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) auf. Wenn der Nachrichtenspeichereintragsbezeichner des Clients auf einen bereits geöffneten Nachrichtenspeicher verweist, kann der Nachrichtenspeicheranbieter vorhandene **IMSLogon-** und **IMsgStore-Schnittstellen** zurückgeben und **muss AddRef** nicht für das Supportobjekt aufrufen. 
    
6. Wenn der Client das MAPI_NO_MAIL-Flag bei der Anmeldung nicht festgelegt hat und die MDB_NO_MAIL in Schritt 1 nicht festgelegt hat, gibt MAPI dem MAPI-Spooler den Eintragsbezeichner des Nachrichtenspeichers, damit sich der MAPI-Spooler beim Nachrichtenspeicher anmelden kann.
    
7. MAPI gibt die **IMsgStore-Schnittstelle** an den Client zurück. 
    
8. Der MAPI-Spooler ruft [IMSProvider::SpoolerLogon auf.](imsprovider-spoolerlogon.md)
    
9. **IMSProvider::SpoolerLogon** gibt die gleichen **IMSLogon-** und **IMsgStore-Schnittstellen** aus Schritt 5 zurück. 
    
> [!NOTE]
> Wenn beim Anmeldeaufruf beim Nachrichtenspeicheranbieter ein Fehler auftritt, weil ein falsches Kennwort angegeben wurde und der Nachrichtenspeicheranbieter keine Schnittstelle anzeigen kann, um nach dem richtigen Kennwort zu fragen, sollte MAPI_E_FAILONEPROVIDER von der **IMSProvider::Logon-Methode** zurückgeben. Dadurch können Clients den Benutzer zur Eingabe eines Kennworts aufforderen, um die Anmeldung beim Nachrichtenspeicheranbieter erneut zu versuchen, anstatt zu verursachen, dass MAPI den Anbieter für die gesamte Sitzung ausfällt. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

