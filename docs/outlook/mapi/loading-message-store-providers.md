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
ms.openlocfilehash: 96e2ca38391931508dd9f3f78f3ba69e6f8b9c15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792899"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="99620-103">Laden von Nachrichtenspeicheranbietern</span><span class="sxs-lookup"><span data-stu-id="99620-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="99620-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99620-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99620-105">Wenn eine Clientanwendung einen Nachrichtenspeicher geöffnet wird, wird MAPI der Nachricht Informationsdienst DLL in den Arbeitsspeicher geladen.</span><span class="sxs-lookup"><span data-stu-id="99620-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="99620-106">Nachdem MAPI die DLL-Datei geladen wurde, tritt eine ganz bestimmte Folge von-Methode aufrufen zwischen den Speicheranbieter Nachricht und MAPI.</span><span class="sxs-lookup"><span data-stu-id="99620-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="99620-107">Diese Methode Anruf Sequenz ermöglicht MAPI auf oberster Ebene abrufen [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), und [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Schnittstellen und ermöglicht es dem Anbieter Nachricht anmelden, um ein MAPI-Support-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="99620-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="99620-108">Nach der Sequenz Anruf sollte der Nachricht Informationsdienst zur Annahme von Anmeldungen von Clients bereit.</span><span class="sxs-lookup"><span data-stu-id="99620-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="99620-109">Die Anruf Sequenz verwendet, wenn eine Nachrichtenanbieter-DLL geladen wird, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="99620-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="99620-110">Der Client ruft [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="99620-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="99620-111">Wenn der Nachrichtenspeicher noch nicht geöffnet ist, MAPI lädt den Speicheranbieter DLL und ruft die DLL [MSProviderInit](msproviderinit.md) Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="99620-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="99620-112">Wenn der Nachrichtenspeicher bereits geöffnet ist, MAPI überspringt die Schritte 2 und 3, und klicken Sie dann verwendet den vorhandenen [IMSProvider: IUnknown](imsprovideriunknown.md) Schnittstelle ist Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="99620-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="99620-113">**MSProviderInit** erstellt und gibt ein **IMSProvider** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="99620-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="99620-114">MAPI-Aufrufen [IMSProvider::Logon](imsprovider-logon.md), übergeben die Clientanwendung Store Eintrags-ID an.</span><span class="sxs-lookup"><span data-stu-id="99620-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="99620-115">**IMSProvider::Logon** erstellt und gibt ein [IMSLogon: IUnknown](imslogoniunknown.md) Schnittstelle und eine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Schnittstelle und ruft dann die [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode auf seine [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="99620-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="99620-116">Wenn der Client-Nachrichtenspeichers Eintrags-ID bezieht sich auf einen Nachrichtenspeicher, der bereits geöffnet ist, die Nachrichtenanbieter kann vorhandene **IMSLogon** und **IMsgStore** Schnittstellen zurückgeben und muss nicht den Aufruf von **AddRef** für die Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="99620-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="99620-117">Wenn der Client nicht das Flag MAPI_NO_MAIL festgelegt haben erteilt Wenn es angemeldet, und er hat die MDB_NO_MAIL nicht festgelegt, in Schritt 1, MAPI Eintrags-ID der Nachrichtenspeicher die MAPI-Warteschlange, damit die MAPI-Warteschlange mit dem Nachrichtenspeicher anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="99620-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="99620-118">MAPI gibt die **IMsgStore** -Schnittstelle an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="99620-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="99620-119">Die MAPI-Warteschlange ruft [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="99620-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="99620-120">**IMSProvider::SpoolerLogon** gibt die gleichen **IMSLogon** und **IMsgStore** Schnittstellen aus Schritt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="99620-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="99620-121">Wenn der Anmeldung Anruf an die Nachricht vom Anbieter fehlschlägt gespeichert werden, da ein falsches Kennwort angegeben wurde und der Nachricht Speicheranbieter eine Schnittstelle für das korrekte Kennwort Fragen kann nicht angezeigt werden, muss er MAPI_E_FAILONEPROVIDER aus der **IMSProvider::Logon zurückgeben. **Methode.</span><span class="sxs-lookup"><span data-stu-id="99620-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="99620-122">Dadurch können Clients, den Benutzer zur Eingabe eines Kennworts anmelden bei der Nachricht Informationsdienst erneut anstelle von MAPI, um den Anbieter für die gesamte Sitzung fehlschlagen verursacht versuchen.</span><span class="sxs-lookup"><span data-stu-id="99620-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99620-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99620-123">See also</span></span>



[<span data-ttu-id="99620-124">Entwickeln eines Providers MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="99620-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

