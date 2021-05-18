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
# <a name="loading-message-store-providers"></a><span data-ttu-id="180f3-103">Laden von Nachrichten Store Anbietern</span><span class="sxs-lookup"><span data-stu-id="180f3-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="180f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="180f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="180f3-105">Wenn eine Clientanwendung einen Nachrichtenspeicher öffnet, lädt MAPI die DLL des Nachrichtenspeicheranbieters in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="180f3-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="180f3-106">Nachdem MAPI die DLL geladen hat, tritt eine sehr spezifische Abfolge von Methodenaufrufen zwischen dem Nachrichtenspeicheranbieter und MAPI auf.</span><span class="sxs-lookup"><span data-stu-id="180f3-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="180f3-107">Mit dieser Methodenaufrufsequenz kann MAPI IMSProvider auf oberster Ebene [erhalten: IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)und [IMsgStore : IMAPIProp-Schnittstellen](imsgstoreimapiprop.md) und ermöglicht dem Nachrichtenspeicheranbieter, ein MAPI-Supportobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="180f3-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="180f3-108">Nach der Anrufsequenz sollte der Nachrichtenspeicheranbieter bereit sein, Anmeldungen von Clients zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="180f3-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="180f3-109">Die Aufrufsequenz beim Laden einer Nachrichtenanbieter-DLL lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="180f3-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="180f3-110">Der Client ruft [IMAPISession::OpenMsgStore auf.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="180f3-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="180f3-111">Wenn der Nachrichtenspeicher noch nicht geöffnet ist, lädt MAPI die DLL des Speicheranbieters und ruft den [MSProviderInit-Einstiegspunkt](msproviderinit.md) der DLL auf.</span><span class="sxs-lookup"><span data-stu-id="180f3-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="180f3-112">Wenn der Nachrichtenspeicher bereits geöffnet ist, überspringt MAPI die Schritte 2 und 3 und verwendet dann die vorhandene [IMSProvider : IUnknown-Schnittstelle,](imsprovideriunknown.md) um Schritt 4 zu schließen.</span><span class="sxs-lookup"><span data-stu-id="180f3-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="180f3-113">**MSProviderInit** erstellt und gibt ein **IMSProvider-Objekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="180f3-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="180f3-114">MAPI ruft [IMSProvider::Logon auf](imsprovider-logon.md)und übertritt den Nachrichtenspeichereintragsbezeichner der Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="180f3-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="180f3-115">**IMSProvider::Logon** erstellt und gibt eine [IMSLogon : IUnknown-Schnittstelle](imslogoniunknown.md) und eine [IMsgStore : IMAPIProp-Schnittstelle](imsgstoreimapiprop.md) zurück und ruft dann die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) auf ihrer [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) auf.</span><span class="sxs-lookup"><span data-stu-id="180f3-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="180f3-116">Wenn der Nachrichtenspeichereintragsbezeichner des Clients auf einen bereits geöffneten Nachrichtenspeicher verweist, kann der Nachrichtenspeicheranbieter vorhandene **IMSLogon-** und **IMsgStore-Schnittstellen** zurückgeben und **muss AddRef** nicht für das Supportobjekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="180f3-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="180f3-117">Wenn der Client das MAPI_NO_MAIL-Flag bei der Anmeldung nicht festgelegt hat und die MDB_NO_MAIL in Schritt 1 nicht festgelegt hat, gibt MAPI dem MAPI-Spooler den Eintragsbezeichner des Nachrichtenspeichers, damit sich der MAPI-Spooler beim Nachrichtenspeicher anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="180f3-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="180f3-118">MAPI gibt die **IMsgStore-Schnittstelle** an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="180f3-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="180f3-119">Der MAPI-Spooler ruft [IMSProvider::SpoolerLogon auf.](imsprovider-spoolerlogon.md)</span><span class="sxs-lookup"><span data-stu-id="180f3-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="180f3-120">**IMSProvider::SpoolerLogon** gibt die gleichen **IMSLogon-** und **IMsgStore-Schnittstellen** aus Schritt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="180f3-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="180f3-121">Wenn beim Anmeldeaufruf beim Nachrichtenspeicheranbieter ein Fehler auftritt, weil ein falsches Kennwort angegeben wurde und der Nachrichtenspeicheranbieter keine Schnittstelle anzeigen kann, um nach dem richtigen Kennwort zu fragen, sollte MAPI_E_FAILONEPROVIDER von der **IMSProvider::Logon-Methode** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="180f3-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="180f3-122">Dadurch können Clients den Benutzer zur Eingabe eines Kennworts aufforderen, um die Anmeldung beim Nachrichtenspeicheranbieter erneut zu versuchen, anstatt zu verursachen, dass MAPI den Anbieter für die gesamte Sitzung ausfällt.</span><span class="sxs-lookup"><span data-stu-id="180f3-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="180f3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="180f3-123">See also</span></span>



[<span data-ttu-id="180f3-124">Entwickeln eines MAPI-Nachrichtenspeicheranbieters</span><span class="sxs-lookup"><span data-stu-id="180f3-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

