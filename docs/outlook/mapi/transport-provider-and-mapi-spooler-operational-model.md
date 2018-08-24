---
title: Transportanbieter und MAPI-Spooler-Betriebsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594033"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="e4c22-103">Transportanbieter und MAPI-Spooler-Betriebsmodell</span><span class="sxs-lookup"><span data-stu-id="e4c22-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="e4c22-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4c22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4c22-105">Transport-Anbieter Initialisierung, beim Starten, Verarbeitung, Herunterfahren und Deinitialization werden durch eine Reihe von Anrufe von der MAPI-Warteschlange an der Adressbuchhierarchie durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4c22-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="e4c22-106">Die Anrufe sind wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="e4c22-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="e4c22-107">Die MAPI-Warteschlange die [XPProviderInit](xpproviderinit.md) -Funktion, ein Support-Objekt übergibt, ruft der Provider-Objekt ab und überprüft, dass der Adressbuchhierarchie und MAPI-Warteschlange eine kompatible MAPI-Versionsnummern unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4c22-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="e4c22-108">Die MAPI-Warteschlange Ruft die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode von der [IXPProvider: IUnknown](ixpprovideriunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4c22-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="e4c22-109">Zwischen den MAPI-Warteschlange und der Adressbuchhierarchie mit den Anmeldeinformationen im aktuellen Abschnitt des Profils wird eine Sitzung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e4c22-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="e4c22-110">Der Transportdienst zurückgegeben ein Anmeldung-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e4c22-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="e4c22-111">Die [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufgerufen, die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e4c22-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="e4c22-112">Der Transportdienst gibt eine Liste der eindeutige Bezeichner (UIDs) und e-Mail-Adresstypen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e4c22-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="e4c22-113">Der Transportdienst die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aufgerufen, um eine Zeile in der Tabelle der MAPI-Status zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4c22-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="e4c22-114">Die MAPI-Warteschlange die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode aufgerufen, um die Nachrichtenübermittlung und Empfang von Nachrichten zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e4c22-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="e4c22-115">Wenn von der Adressbuchhierarchie bei der Rückkehr für den Anruf **TransportLogon** angefordert, ruft die MAPI-Warteschlange in regelmäßigen Abständen die [IXPLogon::Idle](ixplogon-idle.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e4c22-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="e4c22-116">Verarbeitung im Leerlauf ist nützlich, wenn der Adressbuchhierarchie muss Fragen Sie das zugrunde liegenden messaging-System für neue Nachrichten oder andere Aufgaben niedrige Priorität.</span><span class="sxs-lookup"><span data-stu-id="e4c22-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="e4c22-117">Die MAPI-Warteschlange und Adressbuchhierarchie Nachrichten senden und empfangen.</span><span class="sxs-lookup"><span data-stu-id="e4c22-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="e4c22-118">Weitere Informationen finden Sie unter [Nachricht Übermittlung](message-submission-model.md) und [Nachricht Empfang-Modell](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="e4c22-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="e4c22-119">Die MAPI-Warteschlange verarbeitet Transport Anfragen und ruft Support, Nachricht und Attachment-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e4c22-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="e4c22-120">Die MAPI-Warteschlange die **TransportNotify** -Methode aufgerufen, um die Nachrichtenübermittlung und Empfang von Nachrichten zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e4c22-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="e4c22-121">Die MAPI-Warteschlange-Freigaben für die Anmeldung und Anbieter-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e4c22-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="e4c22-122">Weitere Informationen finden Sie unter der [IXPProvider::Shutdown](ixpprovider-shutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e4c22-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

