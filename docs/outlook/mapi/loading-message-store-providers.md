---
title: Laden von Nachrichtenspeicher Anbietern
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
# <a name="loading-message-store-providers"></a>Laden von Nachrichtenspeicher Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung einen Nachrichtenspeicher öffnet, lädt MAPI die DLL des Nachrichtenspeicher Anbieters in den Arbeitsspeicher. Nach dem Laden der DLL durch MAPI erfolgt eine sehr spezifische Abfolge von Methoden aufrufen zwischen dem Nachrichtenspeicher Anbieter und MAPI. Diese Methodenaufruf Sequenz ermöglicht MAPI, [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)und [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Schnittstellen abzurufen, und ermöglicht es dem Nachrichtenspeicher Anbieter, ein MAPI-Unterstützungsobjekt abzurufen. Nach der Anruffolge sollte der Nachrichtenspeicher Anbieter bereit sein, Anmeldungen von Clients zu akzeptieren. 
  
Die Aufrufsequenz, wenn eine Nachrichtenanbieter-DLL geladen wird, lautet wie folgt:
  
1. Der Client ruft [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).
    
2. Wenn der Nachrichtenspeicher noch nicht geöffnet ist, lädt MAPI die DLL des Speicheranbieters und ruft den [MSProviderInit](msproviderinit.md) -Einstiegspunkt der dll auf. Wenn der Nachrichtenspeicher bereits geöffnet ist, überspringt MAPI die Schritte 2 und 3 und verwendet dann die vorhandene [IMSProvider: IUnknown](imsprovideriunknown.md) -Schnittstelle zum Abschließen von Schritt 4. 
    
3. **MSProviderInit** erstellt ein **IMSProvider** -Objekt und gibt es zurück. 
    
4. MAPI ruft [IMSProvider:: LOGON](imsprovider-logon.md)auf und übergibt die ID des Nachrichtenspeicher Eintrags der Clientanwendung.
    
5. **IMSProvider:: Anmeldung** erstellt und gibt eine [IMSLogon: IUnknown](imslogoniunknown.md) -Schnittstelle und eine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Schnittstelle und ruft dann die [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode auf der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle. Wenn der Nachrichtenspeicher Eintragsbezeichner des Clients auf einen bereits geöffneten Nachrichtenspeicher verweist, kann der Nachrichtenspeicher Anbieter vorhandene **IMSLogon** -und **IMsgStore** -Schnittstellen zurückgeben und muss **AddRef** nicht für sein Support-Objekt aufrufen. 
    
6. Wenn der Client das MAPI_NO_MAIL-Flag nicht festgelegt hat, als er sich angemeldet hat und es die MDB_NO_MAIL in Schritt 1 nicht festgelegt hat, gibt MAPI dem MAPI-Spooler die Eintrags-ID des Nachrichtenspeichers, damit sich der MAPI-Spooler beim Nachrichtenspeicher anmelden kann.
    
7. MAPI gibt die **IMsgStore** -Schnittstelle an den Client zurück. 
    
8. Der MAPI-Warteschlangen Aufruf [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider:: SpoolerLogon** gibt dieselben **IMSLogon** -und **IMsgStore** -Schnittstellen aus Schritt 5 zurück. 
    
> [!NOTE]
> Wenn der Anmelde Anruf beim Nachrichtenspeicher Anbieter fehlschlägt, weil ein falsches Kennwort angegeben wurde und der Nachrichtenspeicher Anbieter keine Schnittstelle anzeigen kann, um das richtige Kennwort zu befragen, sollte MAPI_E_FAILONEPROVIDER aus dem IMSProvider zurückgegeben werden **:: Anmeldung **-Methode. Auf diese Weise können Clients den Benutzer auffordern, ein Kennwort einzugeben, um sich erneut an dem Nachrichtenspeicher Anbieter anzumelden, statt zu vermeiden, dass der Anbieter für die gesamte Sitzung einen Fehler verursacht. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

