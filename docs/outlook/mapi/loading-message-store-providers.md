---
title: Laden von Nachrichtenspeicheranbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 47b209b9a8818cf235b7c28593da5778dd944989
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568700"
---
# <a name="loading-message-store-providers"></a>Laden von Nachrichtenspeicheranbietern

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung einen Nachrichtenspeicher geöffnet wird, wird MAPI der Nachricht Informationsdienst DLL in den Arbeitsspeicher geladen. Nachdem MAPI die DLL-Datei geladen wurde, tritt eine ganz bestimmte Folge von-Methode aufrufen zwischen den Speicheranbieter Nachricht und MAPI. Diese Methode Anruf Sequenz ermöglicht MAPI auf oberster Ebene abrufen [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), und [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Schnittstellen und ermöglicht es dem Anbieter Nachricht anmelden, um ein MAPI-Support-Objekt abzurufen. Nach der Sequenz Anruf sollte der Nachricht Informationsdienst zur Annahme von Anmeldungen von Clients bereit. 
  
Die Anruf Sequenz verwendet, wenn eine Nachrichtenanbieter-DLL geladen wird, lautet wie folgt:
  
1. Der Client ruft [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Wenn der Nachrichtenspeicher noch nicht geöffnet ist, MAPI lädt den Speicheranbieter DLL und ruft die DLL [MSProviderInit](msproviderinit.md) Einstiegspunkt. Wenn der Nachrichtenspeicher bereits geöffnet ist, MAPI überspringt die Schritte 2 und 3, und klicken Sie dann verwendet den vorhandenen [IMSProvider: IUnknown](imsprovideriunknown.md) Schnittstelle ist Schritt 4. 
    
3. **MSProviderInit** erstellt und gibt ein **IMSProvider** -Objekt zurück. 
    
4. MAPI-Aufrufen [IMSProvider::Logon](imsprovider-logon.md), übergeben die Clientanwendung Store Eintrags-ID an.
    
5. **IMSProvider::Logon** erstellt und gibt ein [IMSLogon: IUnknown](imslogoniunknown.md) Schnittstelle und eine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Schnittstelle und ruft dann die [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode auf seine [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle. Wenn der Client-Nachrichtenspeichers Eintrags-ID bezieht sich auf einen Nachrichtenspeicher, der bereits geöffnet ist, die Nachrichtenanbieter kann vorhandene **IMSLogon** und **IMsgStore** Schnittstellen zurückgeben und muss nicht den Aufruf von **AddRef** für die Unterstützung. 
    
6. Wenn der Client nicht das Flag MAPI_NO_MAIL festgelegt haben erteilt Wenn es angemeldet, und er hat die MDB_NO_MAIL nicht festgelegt, in Schritt 1, MAPI Eintrags-ID der Nachrichtenspeicher die MAPI-Warteschlange, damit die MAPI-Warteschlange mit dem Nachrichtenspeicher anmelden kann.
    
7. MAPI gibt die **IMsgStore** -Schnittstelle an den Client zurück. 
    
8. Die MAPI-Warteschlange ruft [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** gibt die gleichen **IMSLogon** und **IMsgStore** Schnittstellen aus Schritt 5 zurück. 
    
> [!NOTE]
> Wenn der Anmeldung Anruf an die Nachricht vom Anbieter fehlschlägt gespeichert werden, da ein falsches Kennwort angegeben wurde und der Nachricht Speicheranbieter eine Schnittstelle für das korrekte Kennwort Fragen kann nicht angezeigt werden, muss er MAPI_E_FAILONEPROVIDER aus der **IMSProvider::Logon zurückgeben. **Methode. Dadurch können Clients, den Benutzer zur Eingabe eines Kennworts anmelden bei der Nachricht Informationsdienst erneut anstelle von MAPI, um den Anbieter für die gesamte Sitzung fehlschlagen verursacht versuchen. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

