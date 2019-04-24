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
# <a name="loading-message-store-providers"></a><span data-ttu-id="8d8a4-103">Laden von Nachrichtenspeicher Anbietern</span><span class="sxs-lookup"><span data-stu-id="8d8a4-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="8d8a4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d8a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d8a4-105">Wenn eine Clientanwendung einen Nachrichtenspeicher öffnet, lädt MAPI die DLL des Nachrichtenspeicher Anbieters in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="8d8a4-106">Nach dem Laden der DLL durch MAPI erfolgt eine sehr spezifische Abfolge von Methoden aufrufen zwischen dem Nachrichtenspeicher Anbieter und MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="8d8a4-107">Diese Methodenaufruf Sequenz ermöglicht MAPI, [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)und [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Schnittstellen abzurufen, und ermöglicht es dem Nachrichtenspeicher Anbieter, ein MAPI-Unterstützungsobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="8d8a4-108">Nach der Anruffolge sollte der Nachrichtenspeicher Anbieter bereit sein, Anmeldungen von Clients zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="8d8a4-109">Die Aufrufsequenz, wenn eine Nachrichtenanbieter-DLL geladen wird, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8d8a4-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="8d8a4-110">Der Client ruft [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="8d8a4-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="8d8a4-111">Wenn der Nachrichtenspeicher noch nicht geöffnet ist, lädt MAPI die DLL des Speicheranbieters und ruft den [MSProviderInit](msproviderinit.md) -Einstiegspunkt der dll auf.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="8d8a4-112">Wenn der Nachrichtenspeicher bereits geöffnet ist, überspringt MAPI die Schritte 2 und 3 und verwendet dann die vorhandene [IMSProvider: IUnknown](imsprovideriunknown.md) -Schnittstelle zum Abschließen von Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="8d8a4-113">**MSProviderInit** erstellt ein **IMSProvider** -Objekt und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="8d8a4-114">MAPI ruft [IMSProvider:: LOGON](imsprovider-logon.md)auf und übergibt die ID des Nachrichtenspeicher Eintrags der Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="8d8a4-115">**IMSProvider:: Anmeldung** erstellt und gibt eine [IMSLogon: IUnknown](imslogoniunknown.md) -Schnittstelle und eine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Schnittstelle und ruft dann die [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode auf der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="8d8a4-116">Wenn der Nachrichtenspeicher Eintragsbezeichner des Clients auf einen bereits geöffneten Nachrichtenspeicher verweist, kann der Nachrichtenspeicher Anbieter vorhandene **IMSLogon** -und **IMsgStore** -Schnittstellen zurückgeben und muss **AddRef** nicht für sein Support-Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="8d8a4-117">Wenn der Client das MAPI_NO_MAIL-Flag nicht festgelegt hat, als er sich angemeldet hat und es die MDB_NO_MAIL in Schritt 1 nicht festgelegt hat, gibt MAPI dem MAPI-Spooler die Eintrags-ID des Nachrichtenspeichers, damit sich der MAPI-Spooler beim Nachrichtenspeicher anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="8d8a4-118">MAPI gibt die **IMsgStore** -Schnittstelle an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="8d8a4-119">Der MAPI-Warteschlangen Aufruf [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="8d8a4-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="8d8a4-120">**IMSProvider:: SpoolerLogon** gibt dieselben **IMSLogon** -und **IMsgStore** -Schnittstellen aus Schritt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8d8a4-121">Wenn der Anmelde Anruf beim Nachrichtenspeicher Anbieter fehlschlägt, weil ein falsches Kennwort angegeben wurde und der Nachrichtenspeicher Anbieter keine Schnittstelle anzeigen kann, um das richtige Kennwort zu befragen, sollte MAPI_E_FAILONEPROVIDER aus dem IMSProvider zurückgegeben werden \*\*:: Anmeldung \*\*-Methode.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="8d8a4-122">Auf diese Weise können Clients den Benutzer auffordern, ein Kennwort einzugeben, um sich erneut an dem Nachrichtenspeicher Anbieter anzumelden, statt zu vermeiden, dass der Anbieter für die gesamte Sitzung einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="8d8a4-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d8a4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d8a4-123">See also</span></span>



[<span data-ttu-id="8d8a4-124">Entwickeln eines MAPI-Nachrichtenspeicheranbieters</span><span class="sxs-lookup"><span data-stu-id="8d8a4-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

